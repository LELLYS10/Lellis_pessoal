---
titulo: Financeiro Pessoal do Tom
status: aguardando implementação
atualizado_em: 2026-07-28
---

# Financeiro Pessoal

Área exclusiva da vida financeira do Tom. Não possui qualquer vínculo com CredPlus.

## Onde guardar cada assunto

- `contas-fixas/` — água, energia, celular, internet, aluguel e outras cobranças recorrentes.
- `cartoes/` — faturas, limites e vencimentos dos cartões.
- `dividas/` — parcelas, acordos e valores ainda em aberto.
- `pagamentos/` — registros mensais do que foi pago.
- `planejamento/` — metas, orçamento e previsões.

Extratos bancários e comprovantes brutos não entram no GitHub: devem ficar nas pastas ignoradas `extratos-brutos/` e `comprovantes-brutos/`, criadas quando forem necessárias.

Controle de gastos e pagamentos pessoais do Tom, gerenciado pela Hermes via Telegram. **Totalmente separado do financeiro do CredPlus** (que é gerenciado pelo JARVIS).

Dados guardados na tabela `hermes_pagamentos` do Supabase (ver `../hermes/arquitetura.md`).

Ainda sem uso — vai começar a ser alimentado quando a Hermes estiver ativa.
