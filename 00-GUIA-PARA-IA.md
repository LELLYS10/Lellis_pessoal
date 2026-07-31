---
+titulo: Guia Rápido para IA — Lellis Pessoal
status: ativo
---

# Lellis Pessoal: comece aqui

Este é o cofre pessoal e profissional do Tom. Ele funciona no Obsidian e tem
cópia no GitHub privado. O CredPlus não faz parte deste projeto.

## Objetivo

Manter a vida pessoal, financeira e policial do Tom organizada para que ele e
a Hermes encontrem informações sem depender da memória de uma conversa.

## Leitura inicial

1. Leia este guia.
2. Leia `00-INDICE.md`.
3. Se o assunto for Hermes, leia `hermes/COMO-CONTINUAR.md`.
4. Leia apenas a pasta ligada ao pedido. Não carregue o cofre inteiro sem
   necessidade.

## Onde cada coisa fica

- `hermes/`: funcionamento, decisões e pendências da assistente pessoal.
- `policial/`: legislação, modelos e trabalho da Polícia Ambiental.
- `financeiro-pessoal/`: contas, cartões, dívidas, pagamentos e planejamento.
- `pessoal/`: agenda, lembretes, contatos, notas e documentos da família.

## Regra de tamanho

- Um arquivo Markdown deve ter, no máximo, 200 linhas.
- Se o conteúdo ultrapassar isso, crie uma subpasta e divida por assunto.
- Use nomes claros, em português e sem criar arquivos duplicados.
- Atualize o índice da pasta quando criar uma estrutura importante.

Exemplo:

```
policial/02-modelos/oficios/
  README.md
  modelo-oficio-fiscalizacao.md
  modelo-oficio-solicitacao.md
```

## Segurança

- Nunca grave senhas, tokens, chaves de API ou dados bancários em Markdown.
- Documentos familiares, ocorrências reais, extratos e comprovantes não sobem
  para o GitHub. Respeite o `.gitignore`.
- Nunca misture dados do CredPlus neste cofre.
- Antes de alterar ou apagar informação importante, explique ao Tom e preserve
  um backup quando necessário.

## Rotina obrigatória ao terminar uma mudança

1. Revise os arquivos modificados.
2. Atualize `CHANGELOG.md` quando a mudança for relevante.
3. Rode `git status`.
4. Adicione somente os arquivos da tarefa, nunca use `git add .` sem revisar.
5. Faça um commit curto em português.
6. Envie para `origin/main`.
7. Confirme que o `git status` ficou limpo.

## Como a Hermes usa este cofre

O clone de trabalho da Hermes pessoal fica na VPS em:

`/opt/data/workspace/Lellis_Pessoal`

Ela deve consultar primeiro os arquivos de índice e manter mudanças pequenas,
organizadas e versionadas.

## Estilo de trabalho

- Responder ao Tom somente em português do Brasil, com clareza.
- Uma decisão importante por vez, sem complicar.
- Não inventar leis, valores, datas ou informações ausentes.
- Em assunto policial, mostrar fonte e pedir conferência antes de uso oficial.
