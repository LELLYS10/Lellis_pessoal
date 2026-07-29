# Changelog — Lellis Pessoal

Histórico de mudanças, mais recente primeiro.

## 2026-07-29 — ORGANIZAÇÃO DA VIDA PESSOAL E PROFISSIONAL

- Criada estrutura para legislação, modelos policiais, ocorrências restritas, contas pessoais, cartões, dívidas, agenda, contatos e notas.
- Definidas áreas que podem sincronizar com o GitHub privado e áreas que permanecem somente locais por conterem dados sensíveis.
- Nenhum arquivo pessoal, policial ou financeiro existente foi movido ou apagado nesta etapa.

## 2026-07-28 (noite) — HERMES NO AR

Dia em que a Hermes saiu do papel e entrou em funcionamento.

**Mudança de arquitetura.** O plano de construir a Hermes no n8n foi abandonado. Descobrimos que a Hostinger oferece o Hermes Workspace (Nous Research) com instalação de 1 clique no Docker Manager, trazendo pronto o que teríamos que construir peça por peça: memória persistente, painel web, agendador, multi-canal e catálogo de habilidades. Confirmado que é gratuito — o que se paga é a VPS, que o Tom já tem.

**Instalação.** Hermes Workspace instalado na VPS (projeto `hermes-workspace-uzp5`), rodando com dois containers e roteado pelo Traefik. Painel acessível em `hermes-workspace-uzp5.srv1416255.hstgr.cloud`, e também pelo Safari no iPhone.

**Telegram conectado.** Bot @Tomhenks78_Bot criado e ligado ao gateway, com acesso restrito só ao Tom. Houve uma confusão pelo caminho — o ID informado era o do próprio bot (o número antes dos dois pontos no token), não o do Tom. A própria Hermes detectou a inconsistência e corrigiu.

**Memória alimentada.** A Hermes recebeu a apresentação do Tom, as regras de como trabalhar com ele, e os dados da família, com a instrução de lembrar todas as datas 15, 5 e 1 dia antes.

**Vault versionado no GitHub.** Criado o repositório privado `github.com/LELLYS10/Lellis_pessoal`. O vault foi movido de dentro do iCloud para `~/Lellis Pessoal`, porque o macOS bloqueia a escrita do Git em pastas do iCloud Drive. Plugin Obsidian Git instalado, com commit-and-sync e pull automáticos a cada 10 minutos. Primeiro push com 33 arquivos concluído.

**Descoberta importante:** planos Claude Max e ChatGPT Plus não incluem créditos de API — são cobranças separadas. A Hermes consome API paga via OpenRouter; para construir e programar, o Tom usa o Claude pelo Cowork, que já está no plano dele.

**Documentação reescrita** para refletir a arquitetura real e permitir que qualquer IA retome o projeto sem contexto prévio (`hermes/COMO-CONTINUAR.md`).

## 2026-07-28 (tarde)

- Criada a conta de serviço lellishermes@gmail.com. E-mail principal do Tom permanece intocado.
- Criado projeto Supabase próprio "Lellis.pessoal" (acabou não sendo usado, com a mudança para o Hermes Workspace).
- Vault "Lellis Pessoal" aberto corretamente como cofre único no Obsidian.

## 2026-07-28 (manhã)

- Estrutura inicial do vault criada.
- Definições iniciais: Hermes separada do CredPlus, bot único, Telegram como canal, sem planilhas.
- Iniciada a biblioteca jurídica: Lei 9.605/1998 e Decreto 6.514/2008 (federais) confirmados em fonte oficial. Decreto estadual do Tocantins pendente de envio pelo Tom.
