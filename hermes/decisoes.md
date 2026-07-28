---
titulo: Registro de Decisões — Hermes
status: vivo (adicionar novas decisões no topo)
atualizado_em: 2026-07-28
---

# Decisões tomadas

Decisões já fechadas com o Tom. **Não reabrir** — só revisitar se ele pedir explicitamente.

### Hermes Workspace em vez de n8n
Decidido em 28/07/2026, revertendo o plano inicial. Motivo: o Hermes Workspace (Nous Research), disponível com 1 clique no Docker Manager da Hostinger, já traz pronto tudo que teríamos que construir peça por peça no n8n — memória persistente que aprende, painel web, agendador, multi-canal, catálogo de habilidades. Para um usuário leigo, menos peças para manter. O n8n continua na VPS para automações do CredPlus e pode ser usado depois para automações pontuais.
Contrapartida aceita: a IA assistente não tem conexão direta com o Hermes Workspace (como tem com o n8n via MCP) — ajustes são feitos conversando com a própria Hermes, que se autoconfigura bem.

### Hermes separada do JARVIS/CredPlus
Tom não quer misturar vida pessoal e trabalho policial com o negócio CredPlus. Sistema separado, bot separado, dados separados. O assistente do CredPlus é o JARVIS (n8n, bot @Credpainel_bot).

### Um bot único, não dois separados por assunto
Cogitou-se separar "pessoal/financeiro" de "policial". Decisão: não. O motivo do Tom era só uma suposição de organização, sem necessidade real. A organização acontece por dentro.

### Canal: Telegram, não WhatsApp
Tom já tem bot de WhatsApp exclusivo do CredPlus. Um segundo exigiria número novo + aprovação da Meta (dias, custo), ou biblioteca não-oficial com risco de banimento. Telegram é gratuito, imediato e naturalmente separado.

### Vault fora do iCloud, sincronizado por Git
O vault estava em `~/Library/Mobile Documents/iCloud~md~obsidian/`, mas o Git não funcionava lá: o macOS bloqueia escrita do Terminal nessa pasta ("Operation not permitted"), e daria para resolver com Acesso Total ao Disco — permissão forte demais para o problema. Movido para `~/Lellis Pessoal`. Ganho extra: só um sistema de sincronização (Git em vez de iCloud+Git brigando), evitando arquivos duplicados, e com histórico versionado.

### Repositório GitHub privado, nunca público
Contém CPF de familiares, dados de menores de idade e, futuramente, ocorrências policiais. `github.com/LELLYS10/Lellis_pessoal` criado como Private.

### E-mail de serviço, sem migrar o principal
lellisflavio@gmail.com continua sendo o e-mail do Tom para tudo — toda a vida e o círculo de trabalho dele estão nele, e ele não quer mudar. Foi criado lellishermes@gmail.com apenas como conta de serviço da Hermes. Se necessário, a agenda do principal pode ser compartilhada com a conta de serviço, sem o Tom mudar nada na rotina.

### Base jurídica: apoio, nunca fonte final
A Hermes cruza lei + decreto para poupar o tempo do Tom, mas sempre mostrando a citação exata (lei, artigo, decreto). Como isso alimenta documento oficial, a conferência final é dele. IA pode errar número de artigo ou trabalhar com norma desatualizada.

### Documentação versionada neste vault
Estrutura em `.md`, em vault próprio separado do CENTRAL-CREDPLUS, com commit a cada mudança relevante, escrita de forma que qualquer IA consiga retomar o projeto sem depender de memória de conversa.
