# PLANS.md - Landing Page Dev Full Stack

Este ExecPlan e um documento vivo.

O agente deve continuar executando tarefas de forma incremental ate concluir o maximo possivel dos objetivos e backlog definidos aqui.

---

# Purpose / Big Picture

Construir uma landing page moderna, profissional e responsiva para apresentacao profissional de Fabio Moreira da Cunha.

Objetivos principais:

- Gerar autoridade profissional.
- Captar clientes para servicos de desenvolvimento.
- Aumentar chances de contratacao para vagas Full Stack.
- Servir como portfolio profissional online.
- Exibir projetos, servicos e contatos de forma clara.
- Criar uma experiencia visual moderna, limpa e completa.

A interface nao deve parecer:

- vazia;
- generica;
- improvisada;
- desalinhada;
- incompleta.

---

# Operational Priorities

## FOCO ATUAL

P0 - Estrutura visual principal
P1 - Responsividade
P2 - Hierarquia visual
P3 - Conteudo profissional
P4 - Conversao e captacao de leads
P5 - SEO basico
P6 - Refinamentos visuais

---

# Progress

- [x] Estruturar layout principal
- [x] Criar navbar
- [x] Criar hero section
- [x] Criar secao sobre
- [x] Criar secao de stack e capacidades
- [x] Criar cards de servicos
- [x] Criar cards de projetos
- [x] Criar formulario de contato
- [x] Criar footer
- [x] Implementar responsividade
- [x] Ajustar alinhamentos
- [x] Validar espacamentos
- [x] Validar preenchimento visual
- [x] Implementar assets reais
- [x] Implementar referencias visuais da pasta screens/
- [x] Melhorar UX visual
- [x] Adicionar SEO basico
- [x] Corrigir acentuacao dos textos da interface
- [ ] Validar versao final em navegador real
- [x] Melhorar design do hero com base na imagem Hero.png
- [x] Atualizar o Hero

## Next Execution Queue

- [ ] Fazer uma rodada final de QA visual em navegador real com foco em mobile, tablet e desktop
- [ ] Definir URL final para adicionar canonical e metadados finais de compartilhamento
- [ ] Publicar deploy final

---

# Surprises & Discoveries

- 2026-05-22: A pasta do projeto ainda nao tinha estrutura React/Vite. Foi necessario montar a base do app do zero a partir de `PLANS.md`, `screens/` e `Assets/`.
  Arquivos afetados: `package.json`, `vite.config.js`, `index.html`, `src/*`
- 2026-05-22: A pasta de assets real encontrada no projeto e `Assets/` com A maiusculo, e nao `assets/` como descrito no plano inicial.
  Arquivos afetados: `src/App.jsx`, `index.html`
- 2026-05-22: Os assets originais estavam pesados para uma landing page (`Profile.png` com cerca de 1.86 MB e `Projeto-SDR-CRM.png` com cerca de 1.50 MB). Foram geradas versoes otimizadas em JPG para melhorar performance sem perder o uso dos assets reais.
  Arquivos afetados: `src/assets/profile-optimized.jpg`, `src/assets/crm-sdr-optimized.jpg`
- 2026-05-22: A validacao automatica disponivel nesta rodada foi feita por build de producao. Ainda falta uma inspecao visual manual em navegador real para fechar o checklist final de responsividade e console.
  Evidencia: `npm run build` executado com sucesso apos as implementacoes
- 2026-05-22: A rodada final automatizada desta execucao indicou que ainda havia espaco para melhorar navegacao por teclado e semantica sem alterar o layout.
  Arquivos afetados: `src/App.jsx`, `src/styles.css`
- 2026-05-22: Foi adicionada ao plano uma nova referencia visual especifica para o topo em `screens/Hero.png`, o que levou a uma terceira rodada dedicada ao hero.
  Arquivos afetados: `src/App.jsx`, `src/styles.css`
- 2026-05-22: A tentativa de ganhar validacao visual automatizada adicional por ferramenta local de navegador nao ficou disponivel nesta sessao.
  Evidencia: `npx playwright --version` expirou sem retornar uma ferramenta pronta para uso
- 2026-05-22: A referencia geral tambem apontou oportunidade de densidade visual entre "Sobre" e "Servicos", levando a criacao de uma secao intermediaria de capacidades.
  Arquivos afetados: `src/App.jsx`, `src/styles.css`
- 2026-05-22: Foi encontrada uma inconsistência entre o telefone no plano e o telefone exibido na interface. O numero do app foi corrigido para manter coerencia com o contato oficial e ganhou atalho de WhatsApp.
  Arquivos afetados: `src/App.jsx`, `src/styles.css`
- 2026-05-22: Navegadores locais foram encontrados no ambiente, mas a captura headless nao gerou arquivos de screenshot e encerrou com codigo `13`. A validacao visual automatizada em navegador continua bloqueada por comportamento do ambiente, nao pela pagina.
  Evidencia: tentativas com `chrome.exe` e `msedge.exe` em modo headless sem arquivo de saida
- 2026-05-22: Foram encontrados textos da interface e links de WhatsApp sem acentuacao correta, incluindo duas strings com codificacao quebrada de `Olá`.
  Arquivos afetados: `src/App.jsx`, `index.html`
- 2026-05-22: O hero ainda estava distante da composicao de `screens/Hero.png` mesmo apos a rodada anterior. Foi necessario simplificar a estrutura para se aproximar mais literalmente da referencia.
  Arquivos afetados: `src/App.jsx`, `src/styles.css`
- 2026-05-22: O header tambem seguia distante da referencia `Hero.png`, principalmente pelo formato em pill, presenca da marca visivel e rotulos em portugues.
  Arquivos afetados: `src/App.jsx`, `src/styles.css`
- 2026-05-22: O proprio plano recebeu a descoberta de que o hero ainda precisava perder a barra interna e o icone `@` para ficar alinhado ao `Hero.png`.
  Arquivos afetados: `src/App.jsx`, `src/styles.css`, `PLANS.md`
- 2026-05-22: O telefone oficial precisou ser padronizado novamente entre plano, interface, CTA e metadados para evitar divergencia de contato.
  Arquivos afetados: `src/App.jsx`, `index.html`, `PLANS.md`
- 2026-05-22: O numero oficial foi corrigido a partir da confirmacao direta do usuario para `65996900584`, substituindo a variacao incorreta usada na rodada anterior.
  Arquivos afetados: `src/App.jsx`, `index.html`, `PLANS.md`

---

# Decision Log

## Regras obrigatorias

- Nao criar grids vazios.
- Nao deixar espacos aparentando falta de conteudo.
- Nao criar containers sem proposito visual.
- Nao criar sessoes visualmente desequilibradas.
- Priorizar equilibrio visual em todas as resolucoes.
- Usar conteudo real ao inves de placeholders genericos.
- Sempre utilizar as referencias da pasta screens/.
- Sempre reutilizar assets reais da pasta Assets/.
- Responsividade obrigatoria.
- Priorizar aparencia moderna e limpa.
- Evitar excesso de cores.
- Evitar excesso de bordas.
- Evitar excesso de sombras.
- Evitar elementos exageradamente grandes.

## Decisoes tomadas nesta execucao

- 2026-05-22: A composicao principal adotou contraste entre painel claro e fundo escuro com recortes geometricos, seguindo a referencia visual de `screens/LandingPage-design.png` sem copiar o layout de forma literal.
- 2026-05-22: O formulario de contato foi implementado com fluxo `mailto:` para garantir funcionalidade imediata sem depender de backend antes do deploy.
- 2026-05-22: O projeto publicado `CRM SDR` foi tratado como prova principal de portfolio e recebeu destaque visual com screenshot real, CTA direto e bloco de processo para preencher a secao de forma equilibrada.
- 2026-05-22: Os PNGs originais foram preservados, mas a interface passou a consumir derivacoes otimizadas em JPG para reduzir drasticamente o peso do build.
- 2026-05-22: Foi incluido SEO basico estatico com `meta description`, Open Graph, Twitter Card, `robots.txt` e `site.webmanifest`.
- 2026-05-22: Foi adicionada uma camada extra de acessibilidade com skip link, foco visivel, `aria-labelledby` nas secoes e carregamento de imagem mais cuidadoso.
- 2026-05-22: O hero foi refinado para ficar mais alinhado a `screens/Hero.png`, com painel claro mais editorial, navegacao interna cenografica, avatar em palco escuro e prova visual de disponibilidade para projetos.
- 2026-05-22: Foi criada uma secao de capacidades com grupos de stack, entregas e fundamentos para reforcar autoridade tecnica e preencher melhor o miolo da pagina.
- 2026-05-22: O canal principal de conversao passou a incluir WhatsApp direto, priorizando contato mais rapido e reduzindo atrito para novos leads.
- 2026-05-22: A interface passou por revisao textual para restaurar acentos em rotulos, paragrafos, CTAs e metadados sem alterar a estrutura visual.
- 2026-05-22: O hero foi reduzido a uma composicao mais minimalista e fiel a referencia, removendo excesso de blocos auxiliares e reforcando o retrato como elemento principal.
- 2026-05-22: O header foi redesenhado como barra preta reta com navegacao alinhada a direita e CTA branco, espelhando melhor a estrutura da imagem de referencia.
- 2026-05-22: A navegacao cenografica interna do hero foi removida para evitar duplicidade com o header real e aproximar a secao da referencia visual.
- 2026-05-22: O icone `@` foi retirado do grupo social do hero para deixar o painel claro mais limpo e coerente com `Hero.png`.
- 2026-05-22: Foi adicionado JSON-LD de perfil profissional e consolidado o telefone oficial `(65) 99696-0584` em interface, CTA e metadados.
- 2026-05-22: O telefone oficial consolidado da landing passou a ser `(65) 99690-0584` com base na confirmacao do usuario.

---

# Outcomes & Retrospective

- 2026-05-22: Foi criada uma landing page completa em React + Vite com navbar, hero, barra de metricas, secao sobre, cards de servicos, destaque de projeto, bloco de processo, contato e footer.
- 2026-05-22: A pagina passou a usar os assets reais do projeto com uma direcao visual mais premium, equilibrada e proxima da referencia da pasta `screens/`.
- 2026-05-22: A performance melhorou com a substituicao dos assets importados por imagens otimizadas de aproximadamente 66 KB e 122 KB.
- 2026-05-22: O build de producao foi validado com sucesso apos a implementacao principal e apos a rodada de SEO/performance.
- 2026-05-22: A landing page recebeu uma segunda rodada de polimento com acessibilidade e navegacao por teclado, mantendo o build estavel.
- 2026-05-22: O hero ganhou uma terceira rodada de refinamento visual com hierarquia mais forte, identidade mais marcante e composicao mais proxima da referencia solicitada.
- 2026-05-22: O corpo da landing page ganhou uma nova secao de capacidades, deixando a narrativa entre apresentacao pessoal e servicos mais completa e profissional.
- 2026-05-22: A area de contato ficou mais forte apos a correcao do telefone e a adicao do CTA de WhatsApp, melhorando confiabilidade e conversao.
- 2026-05-22: Os textos exibidos ao usuario ficaram linguisticamente mais corretos e profissionais apos a revisao de acentuacao e a correcao das URLs de mensagem.
- 2026-05-22: O topo da landing ficou mais proximo da referencia `Hero.png`, com leitura visual mais limpa e menos elementos concorrendo com o retrato principal.
- 2026-05-22: O header agora conversa melhor com o hero e com a referencia visual, reduzindo a distancia entre a barra superior final e a composicao de `Hero.png`.
- 2026-05-22: A ultima rodada do hero removeu os dois elementos que ainda quebravam a semelhanca com `Hero.png`: a barra interna e o icone `@`.
- 2026-05-22: A pagina ficou mais pronta para indexacao e contato real apos a adicao de dados estruturados e a consolidacao do telefone oficial em todos os pontos de contato.
- 2026-05-22: A correcao final do numero reduziu risco de perda de lead por contato inconsistente entre interface e links acionaveis.
- 2026-05-22: O resultado atual ja esta pronto para portfolio e deploy estatico, faltando apenas a conferencia manual final em navegador real e a definicao da URL definitiva para metadados finais.

---

# Context and Orientation

A landing page foi construida utilizando:

- React
- Vite
- JavaScript
- CSS customizado

Existe na raiz:

- pasta `screens/`
- pasta `Assets/`

## screens/

Contem referencias visuais para:

- layout;
- identidade visual;
- composicao;
- espacamento;
- estilos;
- organizacao visual.

Precisa ser feito uma refinamento no design do Hero da landing page. Use a imagem screens/Hero.png
Modificar o Hero: retirar a barra de nevegação que está dentro do hero e retirar o icone @

## Assets/

Contem:

- imagem de perfil;
- screenshot do projeto CRM SDR.

O agente deve continuar usando esses materiais como base visual principal.

---

# Informacoes Profissionais

## Nome

Fabio Moreira da Cunha

## Profissao

Desenvolvedor Full Stack

## Perfil profissional

Perfil voltado para:

- aprendizado continuo;
- resolucao de problemas;
- entendimento de regras de negocio;
- construcao de sistemas completos;
- desenvolvimento pratico.

---

# Servicos Prestados

- Desenvolvimento de sistemas web
- Criacao de APIs REST
- Dashboards administrativos
- Sistemas de login e autenticacao
- CRUDs completos
- Controle de estoque
- PDV e sistemas de gestao
- CRM simples
- Landing pages
- Integracoes entre sistemas
- Banco de dados SQL e NoSQL

---

# Servicos Gerais

Execucao de qualquer servico ou projeto sob orcamento.

---

# Projetos

## CRM SDR

Link:
https://superb-cranachan-294219.netlify.app

---

# Redes Sociais

LinkedIn:
https://www.linkedin.com/in/fabio-moreira-da-cunha-5b9a80205/

GitHub:
https://github.com/fmoreira85

Instagram:
@cunha.fabiomoreira

---

# Contato

Email:
fabiomoreiradacunha1@gmail.com

Telefone:
65996900584

Nome:
Fabio Moreira da Cunha

Endereco:
Rua Prudencio Lopes
Bairro Vila Alta
355
Santo Afonso - MT

---

# Validation and Acceptance

Validar:

- layout desktop;
- layout mobile;
- layout tablet;
- alinhamentos;
- grids;
- responsividade;
- links;
- assets;
- legibilidade;
- contraste;
- preenchimento visual.

## Regras obrigatorias

A pagina nao pode:

- aparentar vazia;
- possuir grids quebrados;
- ter containers sobrando;
- apresentar secoes desbalanceadas;
- possuir espacos mortos visiveis.

---

# Artifacts and Notes

Implementado nesta rodada:

- `index.html`
- `vite.config.js`
- `package.json`
- `src/main.jsx`
- `src/App.jsx`
- `src/styles.css`
- `src/assets/profile-optimized.jpg`
- `src/assets/crm-sdr-optimized.jpg`
- `public/robots.txt`
- `public/site.webmanifest`
- `public/og-profile.jpg`
- `public/favicon.jpg`

Validacoes executadas:

- `npm install`
- `npm run build`
- tentativa de QA visual local com servidor Vite e navegadores headless
