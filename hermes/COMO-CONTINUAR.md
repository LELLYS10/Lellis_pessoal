---
titulo: Como Continuar — Guia de Retomada do Projeto Hermes
publico: qualquer IA assistente que precise retomar este projeto do zero
status: vivo — atualizar sempre que o estado mudar
atualizado_em: 2026-07-28
---

# Como Continuar

Este arquivo existe para que qualquer IA — inclusive uma sessão nova do Claude, sem memória da conversa original — consiga retomar o projeto sem o Tom precisar reexplicar nada.

## Resumo em uma frase

A Hermes é a assistente pessoal do Tom, já **instalada e funcionando** numa VPS Hostinger via Hermes Workspace (Nous Research), acessível por navegador, celular e Telegram. O que falta é ensinar a ela o conteúdo do trabalho dele (leis ambientais, modelos de documentos) e conectá-la a este vault.

## O QUE JÁ ESTÁ PRONTO (não refaça)

- Hermes Workspace instalado e rodando na VPS Hostinger (Docker Manager, projeto `hermes-workspace-uzp5`)
- Painel web acessível em `hermes-workspace-uzp5.srv1416255.hstgr.cloud` (senha do workspace está com o Tom)
- Funciona também no celular pelo Safari (pode ser adicionado à Tela de Início como app)
- Telegram conectado: bot **@Tomhenks78_Bot**, com acesso restrito só ao Tom
- Modelos de IA disponíveis via chave OpenRouter (Claude, GPT e outros — trocáveis no seletor do painel)
- A Hermes já recebeu a apresentação do Tom e os dados da família dele, na memória permanente dela
- Este vault está versionado no GitHub privado, com sync automático a cada 10 minutos

## O QUE FALTA — em ordem de prioridade

### 1. Base jurídica (prioridade do Tom)
O Tom quer que, ao mencionar um crime ambiental, a Hermes cruze automaticamente o artigo da lei com o decreto que tipifica a multa, e devolva os dois juntos **com a citação exata da fonte**.

Já levantado (fontes oficiais):
- Lei nº 9.605/1998 — Crimes Ambientais — https://www.planalto.gov.br/ccivil_03/leis/l9605.htm
- Decreto nº 6.514/2008 — infrações administrativas e valores de multa

Falta o Tom enviar: decreto estadual do Tocantins sobre multas ambientais (a busca na web não confirmou o número com segurança — **não invente, peça a ele**), normas municipais e interministeriais.

Como implementar: subir os PDFs para a Hermes (ela tem gerenciador de arquivos e catálogo de habilidades) e criar uma habilidade de consulta cruzada.

**Regra inegociável:** a Hermes sempre mostra lei e artigo de onde tirou a informação. Isso vira documento oficial de polícia — a conferência final é sempre do Tom.

### 2. Modelos de documentos
O Tom vai enviar PDFs de ofícios, relatórios e procedimentos que usa no trabalho. A Hermes precisa aprender a estrutura de cada um (formato, campos que mudam, linguagem formal) para gerar documentos novos no mesmo padrão. Guardar cópias em `policial/modelos/`.

### 3. Conectar a Hermes a este vault
Objetivo do Tom: usar o Obsidian como "segundo cérebro" da Hermes, já que a memória interna dela é limitada. O caminho: a Hermes clona `github.com/LELLYS10/Lellis_pessoal` na VPS, lê os arquivos e também escreve neles (commit + push). Assim Tom, Hermes e a IA assistente trabalham no mesmo cérebro.

Pendente: gerar um token de acesso do GitHub para a Hermes e configurar o clone na VPS.

### 4. Limpeza pendente
Existe um projeto Docker chamado `agente-hermes-rxox` rodando na VPS que é **redundante** — o Hermes Workspace já inclui o agente. Remover libera memória. Confirmar antes de remover.

Também sobraram pastas `.obsidian` órfãs dentro de `hermes/` e `financeiro-pessoal/`, e um arquivo vazio `financeiro-pessoal/lellis pessoal.md`, resultado de cofres abertos errado no início. Podem ser apagados.

### 5. Rotina de lembretes
O Tom pediu que aniversários e datas de falecimento da família sejam lembrados **15 dias, 5 dias e 1 dia antes**. Ele já passou essas datas para a Hermes. Falta confirmar se o agendador dela está de fato disparando esses lembretes.

## ARMADILHAS JÁ ENCONTRADAS (não repita)

- **Não tente SSH na VPS.** A porta 22 é bloqueada de fora. O acesso é pelo terminal web do Hostinger (hpanel.hostinger.com → VPS → Terminal), ou pedindo à própria Hermes, que tem terminal embutido e se auto-configura bem.
- **Não confunda token de bot com ID de usuário no Telegram.** O número antes dos dois pontos no token é o ID do *bot*. O ID do Tom é outro, obtido mandando mensagem direta ao @userinfobot. Essa confusão custou tempo.
- **Não coloque este vault no iCloud.** Já esteve lá e o Git não funcionava: o Terminal do macOS não tem permissão para escrever em `~/Library/Mobile Documents`, e dava "Operation not permitted". Foi movido para `~/Lellis Pessoal` justamente por isso.
- **Plano Max do Claude e ChatGPT Plus NÃO dão créditos de API.** São cobranças separadas. A Hermes consome API paga (OpenRouter). Para construir e programar, usar o Claude via Cowork/Claude Code, que já está no plano.
- **O Hermes Agent na Hostinger é gratuito.** O preço que aparece na página é da VPS ou de "hospedagem gerenciada", que o Tom não precisa — ele já tem VPS.

## COMO O TOM GOSTA DE TRABALHAR

Explicações em português claro, sem jargão. Uma pergunta de cada vez. Ele quer entender o porquê das coisas, não só receber instrução pronta. Prefere que a IA faça a parte técnica por ele quando possível, mas quer acompanhar na tela. Valoriza honestidade — inclusive "não sei" e "isso não é boa ideia".
