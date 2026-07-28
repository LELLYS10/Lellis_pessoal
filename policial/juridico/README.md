---
titulo: Biblioteca Jurídica — Crimes Ambientais
status: iniciada, incompleta
atualizado_em: 2026-07-28
---

# Biblioteca Jurídica

Base de leis, decretos e normas que a Hermes vai usar pra cruzar automaticamente "crime mencionado" → "artigo da lei" → "decreto que tipifica a multa".

## Já confirmado (fonte oficial)

- **Lei nº 9.605/1998** — Lei de Crimes Ambientais (federal). Texto oficial: https://www.planalto.gov.br/ccivil_03/leis/l9605.htm
- **Decreto nº 6.514/2008** — Decreto federal que dispõe sobre infrações e sanções administrativas ambientais, e o processo administrativo, e define valores de multa. Texto oficial: https://www2.camara.leg.br/legin/fed/decret/2008/decreto-6514-22-julho-2008-578464-publicacaooriginal-101336-pe.html

## Pendente (Tom vai enviar)

- Decreto estadual do Tocantins que tipifica multas ambientais (busca na web não confirmou o número com certeza — precisa vir do Tom, que trabalha com isso direto)
- Normas municipais aplicáveis
- Normas interministeriais aplicáveis
- Outras leis/decretos que o Tom for enviando

## Como isso vai funcionar (planejado)

Quando o Tom mencionar um crime à Hermes, ela vai buscar nesta base o artigo correspondente e o decreto que define a multa daquele crime, e devolver os dois juntos com a citação exata (lei, artigo, decreto) — nunca só a conclusão sem a fonte, porque isso alimenta documento oficial. Mecanismo técnico de busca (indexação/vetor) ainda não implementado — ver `../../hermes/pendencias.md`.
