---
titulo: Registro de Decisões — Hermes
status: vivo (adicionar novas decisões no topo)
atualizado_em: 2026-07-28
---

# Decisões tomadas

Cada entrada abaixo é uma decisão já fechada com o Tom. Não perguntar de novo — só revisitar se o Tom pedir explicitamente.

### Hermes separada do JARVIS/CredPlus
Motivo: Tom não quer misturar vida pessoal/trabalho policial com o negócio CredPlus de forma alguma. Workflow n8n novo, bot Telegram novo, tabelas Supabase novas (`hermes_*`), sem overlap.

### Um bot único (não dois bots separados por assunto)
Cogitou-se separar "Hermes pessoal/financeiro" de "Hermes policial" em dois bots. Decisão: **não** — motivo do Tom foi só uma suposição de organização, sem necessidade real de fronteira entre os dois assuntos (diferente da fronteira CredPlus, essa sim real e mantida). Organização interna já resolve via tabelas separadas.

### Canal: Telegram, não WhatsApp
Tom já tem um bot de WhatsApp exclusivo do CredPlus. Poderia criar um segundo, mas: API oficial da Meta exige número novo + aprovação (dias, às vezes custo); alternativa não-oficial (Baileys/whatsapp-web.js) arrisca banir o número. Telegram é gratuito, instantâneo, sem aprovação, e naturalmente já fica separado (bot diferente do `@Credpainel_bot`).

### Armazenamento pessoal: Supabase em PROJETO PRÓPRIO, não planilha
Tom pediu explicitamente algo gratuito e sem planilhas. Decisão inicial era criar tabelas `hermes_*` dentro do projeto Supabase do CredPlus; em 28/07/2026 o Tom foi além e criou um projeto Supabase separado ("Lellis.pessoal", conta lellishermes@gmail.com). Melhor assim: separação total do CredPlus, não só de tabelas.

### E-mail dedicado: lellishermes@gmail.com (conta de serviço)
Criado em 28/07/2026. O e-mail principal do Tom (lellisflavio@gmail.com) NÃO muda e NÃO migra — toda a vida e o círculo de trabalho dele estão nele. O e-mail da Hermes é conta de serviço: o Tom não precisa acessar no dia a dia. Para a Hermes trabalhar nos dados reais do Tom, compartilhar a agenda/Drive do principal com a conta da Hermes. Se algo chegar na caixa da Hermes que o Tom precise ver, ligar encaminhamento automático pro principal.

### Biblioteca jurídica: só como apoio, nunca fonte final
Tom quer que a Hermes cruze automaticamente lei de crime ambiental + decreto que tipifica a multa, pra ele não perder tempo lendo lei. Aceito, mas com resguardo: a Hermes sempre mostra a citação exata (lei/artigo) usada, porque isso vira base de documento oficial — a conferência final é sempre do Tom.

### Documentação do projeto neste vault Obsidian
Tom pediu estrutura de documentação em `.md`, separada em vault próprio (`Lellis Pessoal`, distinto do `CENTRAL-CREDPLUS`), com controle de versão via git, comitando a cada mudança relevante — pra qualquer IA conseguir entender o projeto lendo os arquivos, sem depender de memória de conversa.
