---
titulo: Hermes — Assistente Pessoal do Tom
status: em construção
atualizado_em: 2026-07-28
---

# Hermes

Secretária pessoal do Tom, via bot no Telegram, humanizada (não robótica), rodando na VPS do Tom (mesma VPS do CredPlus, mas em workflow n8n totalmente separado).

## Objetivo

Cuidar da vida pessoal e profissional (polícia ambiental) do Tom:

- Agenda e lembretes
- Controle de gastos e pagamentos pessoais (separado do CredPlus)
- Organização geral (tarefas, anotações)
- Registro e redação de ocorrências da polícia ambiental
- Redação de relatórios e ofícios a partir de modelos que o Tom vai fornecer em PDF
- (futuro) Base jurídica: cruzamento automático de leis de crimes ambientais + decretos que tipificam multas, quando o Tom mencionar um crime

## O que NÃO é

Não tem nenhuma conexão com o CredPlus. O assistente do CredPlus se chama **JARVIS**, é outro workflow, outro bot do Telegram (`@Credpainel_bot`), outro banco de dados. Ver `../hermes/decisoes.md` para o porquê dessa separação.

## Status atual

Ainda não construída no n8n. Ver `pendencias.md` para o que falta antes de montar o workflow.

Veja `arquitetura.md` para o desenho técnico e `decisoes.md` para o histórico de decisões.
