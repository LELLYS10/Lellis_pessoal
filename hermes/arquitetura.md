---
titulo: Arquitetura Técnica — Hermes
status: implementado e funcionando (28/07/2026)
atualizado_em: 2026-07-28
---

# Arquitetura da Hermes

> **Atenção:** o plano original era construir a Hermes no n8n. Isso foi **abandonado** em 28/07/2026 em favor do Hermes Workspace. Se você leu algo sobre n8n em versões antigas deste arquivo, está desatualizado.

## Visão geral

```
Tom conversa por:  navegador (painel web)  |  celular (Safari)  |  Telegram (@Tomhenks78_Bot)
                                    ↓
                    HERMES WORKSPACE (Nous Research)
                    container Docker na VPS Hostinger
                    projeto: hermes-workspace-uzp5
                                    ↓
        ┌───────────────────────────┼───────────────────────────┐
        ↓                           ↓                           ↓
   Modelos de IA              Memória própria            Gateway de mensagens
   (via OpenRouter:           (persistente,              (Telegram em modo
   Claude, GPT, etc.)         aprende com o uso)         polling, s6 supervisiona)
```

## Onde roda

VPS Hostinger (KVM 2, ~100GB disco), a mesma que hospeda o CredPlus e o n8n — mas em container separado, sem interferência. Instalado pelo Docker Manager do painel Hostinger (catálogo → "Espaço de trabalho Hermes").

Containers do projeto `hermes-workspace-uzp5`:
- agente Hermes (o cérebro)
- espaço de trabalho Hermes (interface web, porta interna 3000)

O Traefik (já existente na VPS) faz o roteamento e o domínio.

## Acesso

- Painel web: `hermes-workspace-uzp5.srv1416255.hstgr.cloud`
- Autenticação: senha do espaço de trabalho, definida na instalação (guardada pelo Tom; também consultável nas variáveis de ambiente do projeto no Docker Manager)
- Celular: mesmo endereço pelo Safari; pode virar ícone via "Adicionar à Tela de Início"
- Telegram: bot @Tomhenks78_Bot

## Telegram

Configurado por variáveis de ambiente em `~/.hermes/.env` dentro do container:
- `TELEGRAM_BOT_TOKEN` — token do BotFather
- `TELEGRAM_ALLOWED_USERS` — ID do Tom (sem isso, o gateway bloqueia todos por segurança)

O gateway é supervisionado pelo s6. Para recarregar configuração, o processo precisa ser reiniciado — a própria Hermes consegue fazer isso pelo terminal dela, ou reinicia-se o container pelo painel Hostinger.

## Modelos de IA

Chave OpenRouter configurada, dando acesso a Claude, GPT, Gemini e outros. Trocável no seletor do painel.

Estratégia recomendada ao Tom: modelo econômico (ex: GPT-4.1 Mini) para o dia a dia; modelo forte (Claude) para redigir ofícios, relatórios e consultar leis.

**Valores e chaves não ficam registrados nesta documentação** — apenas nas variáveis de ambiente do servidor.

## Recursos do Hermes Workspace

Chat multi-modelo, memória persistente que aprende, catálogo de mais de 100 habilidades, terminal embutido no navegador, agendador de tarefas, orquestração de sub-agentes, gerenciador de arquivos, interface responsiva.

## Documentação (este vault)

- Local: `/Users/lellisflaviooliveirasantos/Lellis Pessoal` (fora do iCloud)
- Repositório: github.com/LELLYS10/Lellis_pessoal (**privado**)
- Plugin Obsidian Git: auto commit-and-sync a cada 10 min, auto pull a cada 10 min
- O Tom usa Obsidian em dois Macs; a sincronização entre eles agora é feita pelo Git, não mais pelo iCloud

## Contas

- E-mail principal do Tom: lellisflavio@gmail.com — **não muda, não migra**
- E-mail de serviço da Hermes: lellishermes@gmail.com — usado para Supabase e serviços dela; o Tom não acessa no dia a dia
- GitHub: usuário LELLYS10

## Peças criadas mas ainda não usadas

- Projeto Supabase "Lellis.pessoal" (conta lellishermes@gmail.com) — criado quando o plano ainda era n8n. Como o Hermes Workspace tem armazenamento próprio, ficou sem uso por enquanto. Pode servir depois, se for preciso guardar dados estruturados fora dela.
