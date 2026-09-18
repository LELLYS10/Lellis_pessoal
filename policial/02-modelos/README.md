# Modelos de Documento — BPMA

Modelos oficiais que o **Herminho** usa para gerar documentos em PDF.
Você manda os dados (e as fotos, quando for o caso) pelo Telegram, ele clona o
modelo, troca só os dados e devolve o PDF pronto, com a logo.

[[policial/README|<- Policial]] · [[Cerebro|Cerebro]]

Aqui entram modelos SEM dados reais, para a Hermes aprender o padrão de redação de cada tipo de documento (estrutura, campos, linguagem).

- `logo-bpma.png` — timbre oficial (brasão + texto), usar centralizado no topo de qualquer documento
- [[policial/02-modelos/memorial-fotografico/MODELO-MEMORIAL-FOTOGRAFICO|memorial-fotografico/]] — Memorial Fotográfico (.md + .pdf pronto, grade de 4 fotos)
- [[policial/02-modelos/memorial-topografico/MODELO-MEMORIAL-TOPOGRAFICO|memorial-topografico/]] — Memorial Topográfico
- [[policial/02-modelos/relatorio-operacional/MODELO-RELATORIO-OPERACIONAL|relatorio-operacional/]] — Relatório Operacional
- [[policial/02-modelos/auto-de-constatacao/MODELO-AUTO-DE-CONSTATACAO|auto-de-constatacao/]] — Auto de Constatação
- [[policial/02-modelos/certidao-correcao/README|certidao-correcao/]] — Certidão de correção de campo (.md genérico + exemplo em PDF pra CPF)
- [[policial/02-modelos/permuta-de-servico/MODELO-PERMUTA-DE-SERVICO|permuta-de-servico/]] — Solicitação de troca de serviço
- [[policial/02-modelos/oficio-parte/MODELO-OFICIO-PARTE|oficio-parte/]] — Ofício/parte administrativa do dia a dia

Antes de guardar um modelo, retire nomes, CPF, telefones, placas, endereços e números de processos reais — use marcadores tipo [NOME], [CPF], [PROTOCOLO].

Documentos reais (com dado real de ocorrência) NUNCA vão aqui — ficam em `policial/03-ocorrencias-restritas/`, que não sincroniza com o GitHub.

## Como pedir

Fala natural, com os dados. Exemplos:

> "Faz um memorial fotográfico. Protocolo 3108100055, hoje às 09h40, natureza
> transporte irregular de madeira sem DOF, guarnição ST Lellis e CB Teixeira,
> local BR-153 km 42, Xambioá. Envolvido João da Silva, CPF 111.222.333-44."
> *(e manda as fotos junto)*

> "Faz uma permuta: o ST Deusdete me substitui no serviço do dia 20/09, das 08h
> às 08h. Motivo viagem particular."

Se faltar algum dado obrigatório, ele pergunta antes de gerar.

### O relatório do WhatsApp é diferente

Esse não vira PDF — vem como **texto pronto pra copiar e colar no grupo**, com
os emojis e o negrito da corporação. Você dá o assunto solto e a equipe:

> "Relatório do dia pro WhatsApp. Operação Protetor dos Biomas, OS 053/2026 de
> 01 a 06/09. Local Fazenda Santa Rosa, Paranã-TO. Natureza porte ilegal de arma.
> Assunto: abordamos um cara de moto com espingarda sem registro, prendemos e
> levamos pra central de flagrantes de Arraias. Equipe: ST CIEL - 1 H, SGT
> MARTINS - 2 H."

**Ele escreve o histórico sozinho**, no estilo oficial. Vem dentro de um bloco
de código: toca uma vez pra copiar e cola no WhatsApp já formatado.

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
| **Relatório do dia (WhatsApp)** | Texto pronto pro grupo — **não é PDF** |

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
