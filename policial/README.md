---
titulo: Trabalho Policial (Polícia Ambiental) do Tom
status: aguardando implementação
atualizado_em: 2026-07-28
---

# Polícia Ambiental

Tom atua na polícia ambiental no estado do Tocantins. A Hermes vai ajudar com:

- Registro de ocorrências (guardadas na tabela `hermes_ocorrencias` do Supabase)
- Redação de relatórios e ofícios formais, a partir de modelos em PDF que o Tom vai fornecer
- Cruzamento automático de leis de crimes ambientais com decretos que tipificam multas (ver `juridico/README.md`)

## Subpastas

- `01-legislacao/` — PDFs de leis, decretos e normas. Separar em `federal/`, `tocantins/`, `interministerial/` e `municipal/`.
- `02-modelos/` — modelos reutilizáveis de ocorrência, ofício, relatório, parte diária e mensagem de WhatsApp.
- `03-ocorrencias-restritas/` — casos reais, documentos com nomes, CPFs, endereços ou dados operacionais. Esta pasta não vai para o GitHub.
- `juridico/` — índice da biblioteca jurídica já iniciada.
- `modelos/` — índice anterior de modelos, mantido para não quebrar referências existentes.

## Importante

Tudo que a Hermes gerar aqui (citação de lei, valor de multa, texto de ofício) deve ser **conferido pelo Tom antes de qualquer uso oficial**. A Hermes acelera a pesquisa, mas não substitui a conferência humana em documento oficial.
