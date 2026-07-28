# Changelog — Lellis Pessoal

Histórico de mudanças no projeto, mais recente primeiro. Cada entrada corresponde a um commit git nesta pasta.

## 2026-07-28 (tarde)

- Criada a conta de serviço da Hermes: lellishermes@gmail.com. E-mail principal do Tom (lellisflavio@gmail.com) permanece intocado — nada migra, nada muda na rotina dele.
- Criado projeto Supabase PRÓPRIO da Hermes: "Lellis.pessoal" (plano free, compute nano, status saudável, sem migrações ainda). Mudança em relação ao plano anterior, que era usar tabelas dentro do projeto do CredPlus — agora a separação é total.
- Definida a estratégia de agenda: compartilhar o Google Calendar do e-mail principal com a conta da Hermes, pra ela trabalhar nos dados reais sem o Tom mudar nada.
- Vault Obsidian "Lellis Pessoal" aberto corretamente como cofre único (antes tinha sido aberto errado, como dois cofres separados a partir das subpastas). Lista de cofres limpa: só Lellis Pessoal e CENTRAL-CREDPLUS.
- Pendente: rodar o SQL das tabelas `hermes_*` dentro do projeto novo, e criar o bot do Telegram.

## 2026-07-28

- Estrutura inicial do vault criada (00-INDICE, hermes/, financeiro-pessoal/, policial/).
- Definido: Hermes será um workflow n8n novo e separado do JARVIS (que fica 100% dedicado ao CredPlus).
- Definido: Hermes será um bot único no Telegram (não dois bots separados) — organização interna por tabelas, não por bots separados.
- Definido: armazenamento de dados pessoais (agenda extra, pagamentos, tarefas, ocorrências) no Supabase, tabelas `hermes_agenda`, `hermes_pagamentos`, `hermes_tarefas`, `hermes_ocorrencias` (já criadas por Tom via SQL Editor).
- Definido: bot no Telegram (não WhatsApp, pra evitar risco de banimento de número e burocracia da API oficial da Meta).
- Iniciada a biblioteca jurídica: coletados os textos oficiais da Lei 9.605/1998 (Crimes Ambientais) e do Decreto 6.514/2008 (infrações administrativas e multas), fontes no Planalto/Câmara dos Deputados. Decreto estadual do Tocantins sobre multas ainda pendente — Tom vai enviar.
- Pendente: token do bot Telegram da Hermes, criação de e-mail dedicado, definição de qual pasta/local do Mac vai guardar os PDFs dos modelos de ofício/procedimento.
