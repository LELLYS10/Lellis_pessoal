---
name: design-futurista-3d
description: Cria e aprimora dashboards, páginas HTML e apresentações com cores fortes, estética moderna e futurista, profundidade visual e slides tridimensionais. Use quando o usuário pedir esses entregáveis com esse estilo ou invocar esta skill.
---

# Design Futurista 3D

## Objetivo e personalidade

Transforme o pedido do usuário em um entregável visual completo e utilizável. O gosto padrão é por cores fortes, contrastes marcantes, acabamento moderno e elementos tridimensionais. Produza o arquivo ou projeto solicitado, não apenas uma descrição do que poderia ser feito.

Use português brasileiro por padrão. Uma orientação específica do usuário sobre cores, marca, formato ou estilo prevalece sobre os padrões desta skill. Preserve textos, dados e identidade fornecidos; não altere o significado para caber no layout.

Esta skill fornece direção de design e execução. Utilize os recursos disponíveis no ambiente do agente; não presuma que bibliotecas, renderizadores, geradores de imagem ou ferramentas de apresentação estejam instalados.

## Decisões iniciais

- Identifique se o pedido é um dashboard, uma página HTML ou uma apresentação. Se forem vários, mantenha uma identidade comum e entregue os formatos pedidos.
- Aproveite as informações existentes. Pergunte somente quando faltar algo essencial, como a fonte de dados necessária para um painel real. Para escolhas visuais reversíveis, decida e avance.
- Sem formato definido, entregue páginas e dashboards em HTML responsivo; para slides, prefira uma apresentação HTML em 16:9 com navegação. Se o usuário pedir PowerPoint, entregue PPTX; se pedir PDF, gere o PDF.
- Em projetos existentes, siga a tecnologia e a estrutura do projeto. Para um arquivo independente, prefira HTML, CSS e JavaScript com recursos locais ou incorporados.
- Defina uma ideia visual ligada ao assunto. Não use o mesmo conjunto de cartões, gradientes e enfeites em todos os trabalhos.

## Direção de arte

### Cor forte com intenção

Escolha uma paleta principal e distribua a cor com hierarquia: fundo, superfícies, texto, cor protagonista e acento. Use cor forte em áreas relevantes, gráficos, títulos selecionados e ações principais. Evite diluir todo o resultado em cinza ou pastéis.

Paletas iniciais adaptáveis:

| Paleta | Fundo | Superfície | Protagonista | Acento | Texto |
| --- | --- | --- | --- | --- | --- |
| Neon orbital | #070B18 | #131D35 | #00E5FF | #FF3CAC | #F5F7FF |
| Plasma violeta | #10091F | #24133D | #A855F7 | #C8FF00 | #FAF7FF |
| Solar digital | #100B08 | #281A15 | #FF6B00 | #FFD600 | #FFF8F0 |
| Cobalto elétrico | #060D24 | #142449 | #2563FF | #00FFC2 | #F4F8FF |

Essas cores são pontos de partida, não combinações automaticamente aprovadas para qualquer tamanho de texto. Verifique contraste no uso real. Em botões neon, texto escuro costuma ser mais legível. Use fundos claros se o pedido ou a identidade exigir, preservando acentos vibrantes.

### Forma, tipografia e composição

- Crie um foco visual claro por tela ou slide. Combine títulos expressivos com texto de apoio curto e legível.
- Use tipografia de personalidade em títulos e uma fonte confortável para leitura; disponibilize alternativas locais quando fontes externas não puderem carregar.
- Varie a composição conforme a mensagem: destaque editorial, comparação, linha do tempo, painel de indicadores ou cena central. Não transforme toda informação em um cartão idêntico.
- Combine sombras, bordas luminosas discretas, camadas e gradientes bem posicionados. Vidro translúcido é opcional e exige fundo que mantenha o texto legível.
- Use ícones coerentes, ilustrações próprias, SVG ou recursos fornecidos. Não invente logos, fotos reais, depoimentos ou marcas de clientes.

## Profundidade e tridimensionalidade

Crie profundidade percebida com planos em primeiro e segundo plano, luz e sombra coerentes, sobreposição e perspectiva. Reserve o efeito mais expressivo para a capa, a cena principal ou um elemento de destaque.

Em HTML:

- Use `perspective`, `transform-style: preserve-3d`, `translateZ` e rotações moderadas quando contribuírem para a composição.
- Mantenha textos longos e controles em planos fáceis de ler. Não incline todo o conteúdo.
- Inclinação ao mover o cursor e paralaxe são opcionais: limite a amplitude, desative em telas de toque quando atrapalharem e respeite `prefers-reduced-motion`.
- Prefira CSS e SVG para profundidade leve. Use WebGL ou bibliotecas 3D somente quando a tarefa precisar de uma cena realmente tridimensional e houver recursos para executar e validar.
- Animações não podem bloquear ações, esconder informação ou causar movimento contínuo desnecessário.

Em PPTX e PDF:

- Traduza o estilo em camadas, formas editáveis, imagens com perspectiva, iluminação e sombras.
- Preserve textos editáveis no PPTX sempre que possível. Não transforme todos os slides em imagens apenas para conseguir um efeito.
- Diferencie aparência tridimensional de um objeto 3D manipulável. Não prometa interação ou animação que o formato de saída não suporta.

## Modo dashboard

1. Entenda a pergunta que o painel deve responder, o público, o período e os indicadores disponíveis.
2. Dê destaque aos números que orientam decisões. Mostre unidade, período, fonte e critério de comparação quando conhecidos.
3. Escolha gráficos adequados: linhas para evolução, barras para comparação e tabelas para detalhe. Use a mesma cor para a mesma categoria em todo o painel.
4. Aplique profundidade aos contêineres e à composição, mantendo os gráficos quantitativos em 2D para não distorcer a percepção dos valores.
5. Faça filtros e seletores atualizarem os componentes relevantes. Botões precisam executar ações reais ou indicar claramente sua indisponibilidade.
6. Inclua estados de carregamento, vazio e erro quando existir busca de dados. Não simule atualização em tempo real sem uma fonte conectada.
7. Sem dados reais, use exemplos somente como demonstração e identifique-os visivelmente como “Dados demonstrativos”. Não apresente métricas inventadas como resultados do usuário.
8. Em telas menores, reorganize indicadores e gráficos; tabelas largas podem ter rolagem dentro do próprio contêiner.

## Modo HTML e site

- Entregue uma página funcional com estrutura semântica, boa hierarquia de conteúdo e navegação coerente.
- Use a primeira dobra para explicar a proposta e destacar a ação principal. O visual futurista deve apoiar o conteúdo.
- Faça links, menu, abas, modais e demais interações funcionarem quando estiverem presentes. Formulário sem serviço de envio deve ser identificado como demonstração, sem mensagem falsa de envio bem-sucedido.
- Use variáveis CSS para cores, tipografia, espaçamentos e elevação, facilitando ajustes posteriores.
- Para entregas independentes, procure permitir abertura local sem configuração. Informe quando houver necessidade de servidor ou conexão externa.
- Preserve desempenho: evite vídeos pesados automáticos, excesso de partículas e bibliotecas grandes para efeitos simples.

## Modo slides

- Construa uma narrativa a partir do objetivo: contexto, mensagem principal, evidências e próximo passo, adaptando a sequência ao conteúdo real.
- Use uma ideia principal por slide, títulos que comuniquem a mensagem e texto conciso. Não force uma quantidade fixa de slides.
- Faça uma capa expressiva com profundidade e cores fortes. Alterne slides de impacto com slides de conteúdo para manter o ritmo.
- Use cenas em camadas, objetos isométricos, perspectivas e iluminação para o aspecto tridimensional. Não use efeitos que reduzam a leitura de tabelas ou gráficos.
- Em apresentação HTML, ofereça anterior/próximo, navegação por teclado e indicação de progresso. Para conteúdo que exceder a altura, preserve o acesso sem cortar texto.
- Prepare estilo de impressão para que cada slide vire uma página e os controles não apareçam. PDF deve preservar fundos, proporções e conteúdo.
- Em PPTX, verifique fontes, elementos fora da área, sobreposições e diferenças de renderização. Preserve editabilidade dos componentes principais.

## Acessibilidade e acabamento

- Busque contraste mínimo de 4,5:1 em texto comum e 3:1 em texto grande. Nunca dependa apenas da cor para explicar estados ou categorias.
- Inclua foco visível, nomes claros de controles e operação por teclado. Evite efeitos com flashes.
- Em telas de toque, use alvos confortáveis, próximos de 44 × 44 px quando possível.
- Respeite redução de movimento e mantenha o conteúdo utilizável sem animação.
- Adapte moeda, datas e números ao contexto; para conteúdo brasileiro, use formatos como R$ 1.234,56 e DD/MM/AAAA.

## Execução e verificação

Implemente o entregável e revise o resultado antes de concluir:

- Em HTML, confira uma largura de celular e uma de computador, legibilidade, transbordamentos, recursos ausentes e interações principais.
- Em dashboards, confronte totais e cálculos com a fonte, além de testar pelo menos uma alteração relevante de filtro.
- Em slides, renderize ou visualize todas as páginas quando houver ferramenta disponível. Confira cortes, colisões, alinhamento e consistência.
- Verifique os recursos disponíveis antes de escolher dependências. Se algo essencial não puder ser gerado, explique a limitação e entregue uma alternativa útil, identificando seu formato corretamente.
- Não declare que testou visualmente, exportou, conectou dados ou validou interações sem ter realizado essas verificações.
- Salve os arquivos no destino pedido. Entregue o arquivo ou link acessível, uma descrição curta e apenas as instruções necessárias para abrir ou usar. Publicação externa depende do pedido do usuário.

## Exemplos de pedidos atendidos

- “Crie um dashboard financeiro futurista em HTML, com azul elétrico e verde neon, usando esta planilha.”
- “Monte uma apresentação com visual tridimensional sobre minha empresa, usando roxo intenso e laranja.”
- “Transforme esta página em um site moderno de cores fortes e efeitos de profundidade, mantendo os textos.”
- “Crie slides em PowerPoint com capa 3D e gráficos editáveis a partir destes dados.”
