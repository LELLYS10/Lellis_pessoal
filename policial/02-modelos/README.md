# Modelos de Documento — BPMA

Modelos oficiais que o **Herminho** usa para gerar documentos em PDF.
Você manda os dados (e as fotos, quando for o caso) pelo Telegram, ele clona o
modelo, troca só os dados e devolve o PDF pronto, com a logo.

## Como pedir

Fala natural, com os dados. Exemplos:

> "Faz um memorial fotográfico. Protocolo 3108100055, hoje às 09h40, natureza
> transporte irregular de madeira sem DOF, guarnição ST Lellis e CB Teixeira,
> local BR-153 km 42, Xambioá. Envolvido João da Silva, CPF 111.222.333-44."
> *(e manda as fotos junto)*

> "Faz uma permuta: o ST Deusdete me substitui no serviço do dia 20/09, das 08h
> às 08h. Motivo viagem particular."

Se faltar algum dado obrigatório, ele pergunta antes de gerar.

## Os modelos

| Documento | Quando usar |
|---|---|
| **Memorial Fotográfico** | Registro de fotos da ocorrência |
| **Memorial Topográfico** | Área desmatada, coordenadas, carta-imagem |
| **Auto de Constatação** | Constatação de infração em campo |
| **Certidão de Correção** | Corrigir erro material em auto já lavrado |
| **Parte Diária** | Passagem de plantão |
| **Relatório Operacional** | Fechamento de operação |
| **Permuta de Serviço** | Troca de plantão |
| **Ofício** | Solicitação formal ao comando |

## O que tem em cada pasta

- **`originais/`** — os arquivos `.docx` e `.pdf` que serviram de base. Não são
  usados para gerar nada, ficam como referência do formato oficial.
- **`templates/`** — os modelos em HTML que o Herminho realmente usa. Os campos
  entre `[COLCHETES]` são o que ele substitui.
- **`brasao-pmto.png`** — o cabeçalho oficial (PMTO + Governo do Estado) que
  entra em todo documento.

## Consulta jurídica

O **Espelho de Autuações** (em `originais/`) tem os enquadramentos legais e as
faixas de multa por tipo de infração. Dá pra perguntar direto ao Herminho:
*"qual o enquadramento de impedir a ação da fiscalização?"*

## Onde o Herminho guarda a cópia de trabalho

Os templates também ficam na VPS, em `/opt/data/templates/`, que é de onde ele
lê na hora de gerar. **Se você editar um template aqui no Obsidian, avise —
precisa atualizar a cópia da VPS também**, senão ele continua usando a antiga.
