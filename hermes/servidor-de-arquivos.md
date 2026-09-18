# Servidor de arquivos do Hermes

Endereco publico onde os arquivos que o Hermes cria ficam acessiveis pelo navegador
(Mac mini ou celular), sem senha. O endereco e secreto: quem nao tem o link nao acha.

## Endereco

https://arq-2a94207c02.srv1416255.hstgr.cloud

Abrindo a raiz aparece a lista de todos os arquivos.
Para um arquivo especifico: o endereco acima + barra + nome do arquivo.
Exemplo: https://arq-2a94207c02.srv1416255.hstgr.cloud/dashboard_futurista_avancado.html

## Como funciona

- Container Docker `hermes-arquivos` (nginx), criado em 18/09/2026.
- Serve a pasta do servidor `/docker/hermes-agent-rxox/data/dashboards`,
  que e a mesma pasta que o Hermes enxerga como `/opt/data/dashboards`.
- Montada como somente-leitura: o servidor nao apaga nem altera nada.
- Roteado pelo Traefik, subdominio automatico do Hostinger (nao mexe em DNS).

## Regra para o Hermes

Todo arquivo que ele salvar em `/opt/data/dashboards/` vira link clicavel
trocando `/opt/data/dashboards/` por `https://arq-2a94207c02.srv1416255.hstgr.cloud/`.

## Cuidados

- Nao colocar ai arquivo com dado real de cliente, ocorrencia ou informacao pessoal.
  O endereco e secreto, mas e publico na internet para quem tiver o link.
- Se o Traefik der pau depois de mudar alguma etiqueta (label), reiniciar ele resolve:
  `docker restart traefik-wvkg-traefik-1`

## Como usar no dia a dia

Pedir normalmente no Telegram, por exemplo:
"Monte um dashboard com esses numeros e me manda o link."

Ele salva em /opt/data/dashboards/ e responde com o link pronto.
E so tocar no link: abre no navegador do Mac mini ou do celular.

Se quiser o visual futurista, pedir explicitamente:
"Use a skill design-futurista-3d, leia o SKILL.md inteiro e aplique todos os
efeitos: glassmorphism, profundidade 3D, brilho neon e animacao nos cards."
O "leia o SKILL.md inteiro" faz diferenca - sem isso ele usa so as cores.

## Se o link parar de abrir

Quase sempre e o Traefik. No terminal da VPS:

    docker restart traefik-wvkg-traefik-1

Os outros sites saem do ar por uns 10 segundos e voltam sozinhos.
Depois esperar 1 minuto e recarregar o link.

Para conferir se o servidor de arquivos esta de pe:

    docker ps | grep hermes-arquivos

## Historico

- 18/09/2026 - criado. Antes disso o Hermes mandava links quebrados e arquivos
  HTML soltos, que nao abriam no celular.

[[README|<- Hermes]]
