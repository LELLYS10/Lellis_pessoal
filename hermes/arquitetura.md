---
titulo: Arquitetura Técnica — Hermes
status: planejado (ainda não implementado)
atualizado_em: 2026-07-28
---

# Arquitetura da Hermes

## Visão geral

```
Telegram (bot dedicado, ainda sem token cadastrado)
   ↓
n8n (VPS Hostinger, mesma VPS do CredPlus — projeto n8n "Lellis Flavio Oliveira Santos", pessoal, separado do projeto do CredPlus)
   ↓
Agente de IA (LLM, mesmo padrão usado no JARVIS: OpenRouter GPT-4o via nó langchain.agent)
   ↓
Ferramentas (tools) do agente:
   - Supabase — PROJETO PRÓPRIO "Lellis.pessoal" (criado 28/07/2026, região/plano free, compute nano), totalmente separado do projeto Supabase do CredPlus. Tabelas: hermes_agenda, hermes_pagamentos, hermes_tarefas, hermes_ocorrencias
   - Google Calendar (agenda principal do Tom, compartilhada com a conta da Hermes — o Tom não muda nada na rotina dele)
   - Gmail (conta dedicada da Hermes: lellishermes@gmail.com — conta de serviço, o Tom não usa no dia a dia)
   - (futuro) Busca vetorial na biblioteca jurídica (leis/decretos/normas em PDF)
```

## Contas

- E-mail principal do Tom: lellisflavio@gmail.com — permanece intocado, é a vida dele (trabalho, círculo pessoal). Não migrar nada.
- E-mail da Hermes: lellishermes@gmail.com — conta de serviço, criada só pra Hermes ter Supabase, Gmail e Calendar próprios. O Tom não precisa acessar no dia a dia.
- Estratégia: compartilhar a agenda (e pastas do Drive, se preciso) do e-mail principal COM a conta da Hermes, pra ela trabalhar nos dados reais do Tom sem ele mudar nada.

## Banco de dados (Supabase)

Projeto "Lellis.pessoal", na conta lellishermes@gmail.com. Tabelas a criar (SQL já entregue ao Tom):

- `hermes_agenda` (id, titulo, descricao, data_hora, lembrete_enviado, criado_em)
- `hermes_pagamentos` (id, descricao, valor, vencimento, pago, pago_em, criado_em)
- `hermes_tarefas` (id, titulo, feito, criado_em)
- `hermes_ocorrencias` (id, titulo, texto, criado_em)

Acesso via HTTP Request Tool com a service_role key do projeto Lellis.pessoal (chave NÃO fica registrada nesta documentação — guardar só nas credenciais do n8n). Mesmo padrão técnico das ferramentas `credplus_*` do JARVIS, mas apontando pro projeto e tabelas da Hermes.

## Telegram

Bot próprio e exclusivo da Hermes (diferente do `@Credpainel_bot` do JARVIS). Trigger restrito ao chat_id do Tom, mesmo padrão de segurança usado no JARVIS Telegram (chatIds fixo, só o Tom opera).

## Personalidade

Humanizada, calorosa, natural — não "assistente executivo robótico" como o tom atual do JARVIS. Faz uma pergunta por vez, espera resposta, conversa como pessoa.

## Pendente de decisão/implementação

- Suporte a voz (Whisper STT + TTS), como o JARVIS Telegram tem — ainda não decidido se a Hermes vai ter isso desde o início ou depois.
- Upload e indexação de modelos de documentos em PDF (ofícios, procedimentos) — mecanismo ainda não definido.
- Biblioteca jurídica pesquisável (leis + decretos + normas) — ver `../policial/juridico/README.md`.
