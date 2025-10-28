Glorya — Hub de Engajamento Humano

Site oficial da Glorya. Next.js (App Router) + TypeScript + Tailwind, CMS visual com Builder.io, deploy na Vercel.
Tema dark elegante (#0A0A0A) com acento #FF005E e Roboto.

📌 TL;DR (o que criar)

Páginas: Splash, Hub (mandala), Diagnóstico (modal/fallback), 4 LPs de Pilares, 2 Produtos (Pontos/Card), NR‑1, Cases (eventos), Clientes, Aprender, Sobre, Contato.

Componentes: Header (menu opção 2), Footer, Hero, Chips (para quem é), Cards de “O que entregamos”, Stepper (4 passos), Métricas (trio), Habilitadores, FAQ (4 itens), CTA.

Interações: Mandala (4 setores + centro com 2 CTAs), Diagnóstico lúdico (3–5 passos), links cruzados entre Pilares ↔ Produtos ↔ Cases/Clientes.

Visual: fundo #0A0A0A, texto #FFFFFF, secundário #B8B8B8, borda #1F1F1F, acento #FF005E, Roboto.

CTA primário em todo o site: Agendar diagnóstico (ou Falar com especialista em Produtos).

A11y: foco visível em #FF005E, TAB navega na mandala/cards, contraste AA.

🧱 Stack

Framework: Next.js 14+ (App Router) · TypeScript

Estilo: Tailwind CSS + fontes Google (Roboto)

CMS visual: Builder.io (Models: page, section)

Hospedagem: Vercel (Preview por PR + Produção)

Pacotes: pnpm

CI: GitHub Actions (typecheck + lint + build)

🗺️ Arquitetura de rotas
/                     -> Splash (portal)
/hub                  -> Hub (mandala)
/diagnostico          -> Diagnóstico (fallback/modal)
/engajar/pessoas      -> LP Pessoas & Cultura
/engajar/performance  -> LP Performance & Gamificação
/engajar/reconhecimento -> LP Reconhecimento & Incentivos
/engajar/eventos      -> LP Experiências & Eventos
/recompensar/pontos   -> Plataforma de Pontos
/recompensar/card     -> Glorya Card
/cuidar/nr1           -> NR-1 Check (pesquisa de riscos)
/provar               -> Cases (somente eventos, por enquanto)
/clientes             -> Logos + depoimentos curtos
/aprender             -> Guias + Calculadora de ROI
/sobre                -> Quem somos
/contato              -> Form multi-etapas (lead)


Navegação (opção 2 – verbos): Hub · Engajar (4 pilares) · Recompensar (Pontos, Card) · Cuidar (NR-1) · Provar (Cases) · Clientes · Aprender · Quem Somos · Fale Conosco · [CTA] Diagnóstico

🎨 Design System (tokens)

Cores

--bg: #0A0A0A (fundo)

--text: #FFFFFF (texto primário)

--text2: #B8B8B8 (texto secundário)

--line: #1F1F1F (linhas/bordas)

--accent: #FF005E (acento/CTA/foco)

Tipografia

Roboto — H1 56/64 700 | H2 36/44 700 | H3 24/32 600 | Body 16/26 400 | Small 14/22 400

Títulos em branco puro; parágrafos em #B8B8B8.

Componentes (estilo)

CTA primário: fundo #FF005E, texto #000, raio 12–16px

CTA secundário: borda #FF005E, fundo transparente, hover com rgba(255,0,94,.12)

Cards: fundo #0F0F0F, borda #1F1F1F, raio 16px, padding 20–24

Inputs: bg #111, borda #2A2A2A, foco #FF005E

Foco: outline 2px #FF005E + offset 2px (todos elementos interativos)

Grid/Spacing

12 colunas (max‑width 1200–1280px), gutter 24px

Escala 8px (16/24/32/48/64)

Responsivo

xs ≤480: 1 coluna, CTAs sticky

sm ≤768: 2 colunas

md ≤1024: 12 colunas

lg 1025–1280: 1200–1280px

🧩 Componentes (para Builder “section” ou React components)

Header: logo, menu (opção 2), CTA primário “Agendar diagnóstico”.

Footer: links mínimos (Privacidade/LGPD, Acessibilidade).

Hero: H1, sub 1 linha, CTA(s).

Chips de Persona: 3–4 opções clicáveis.

Cards “O que entregamos”: 3–6 bullets (1 linha cada).

Stepper 4 passos: Descobrir → Desenhar → Implantar → Mensurar.

Métricas (trio): 3 números grandes + rótulos.

Habilitadores: cards que linkam para Plataforma de Pontos / Glorya Card / NR‑1.

FAQ (acordeão): 4 perguntas.

Mandala (Hub): 4 setores clicáveis + centro com 2 botões (Diagnóstico, Clientes).

Diagnóstico (wizard): 3–5 passos (objetivo, área, estado, prazo/porte) + resultado.

Cards de Case: imagem P&B + 3 métricas + botão “Ver case”.

Grid de Logos (Clientes).

Calculadora de ROI (card com 3 inputs → resultado estimado).

Regra editorial: 1 frase por bloco; bullets sempre de 1 linha; sem emojis.

🧭 Esqueleto de conteúdo por página (copy mínima)
/ Splash

H1: Engajamento humano que vira resultado.

Sub: Programas de performance, reconhecimento e eventos — com pontos e cartão para acelerar o que importa.

Botões: Entrar no Hub (primário) · Fazer diagnóstico (secundário)

/hub Hub (mandala)

Título: Seu mapa de engajamento

Sub: Escolha um caminho ou faça o diagnóstico em 60s.

Mandala:

Pessoas & Cultura — Colocamos o sistema de pessoas em ordem.

Performance & Gamificação — Metas viram missões com dados.

Reconhecimento & Incentivos — Rituais e premiação justa.

Experiências & Eventos — Picos de conexão que impulsionam o próximo ciclo.

Centro: Agendar diagnóstico (primário) · Ver clientes (secundário)

Cards abaixo: Recompensar (Pontos, Card) · Cuidar (NR‑1 Check)

/diagnostico (fallback/modal)

Passos: Prioridade · Área · Estado (3 sliders) · Prazo & porte

Saída: 1 pilar recomendado + habilitadores (Pontos/Card/NR‑1)

CTA: Agendar diagnóstico · Ver página recomendada

LPs dos Pilares (todas com mesma anatomia)

/engajar/pessoas — Pessoas & Cultura

H1: Organize o sistema de pessoas para a cultura acontecer todo dia.

Sub: Rituais de liderança, performance e comunicação que sustentam o engajamento.

Para quem: RH/People · Lideranças · C‑Level

Cenários: Turnover alto · Falta de ritos · Ruído entre áreas

O que entregamos: Rituais de liderança · Gestão de performance · Comunicação interna

Como funciona: Descobrir → Desenhar → Implantar → Mensurar

Medimos: e‑NPS/clima · rituais ativos · turnover crítico

Habilitador: NR‑1 Check

CTA: Agendar diagnóstico · Ver clientes

/engajar/performance — Performance & Gamificação

H1: Transforme metas em jornadas que as pessoas querem cumprir.

Sub: Missões, quizzes, ranking e dashboards — com recompensa integrada.

Para quem: Vendas · Operações · Atendimento · T&D

Cenários: Meta em curto prazo · Onboarding · Produtividade/qualidade

O que entregamos: Missões/níveis · Quizzes · Ranking · Calendário 4–8 semanas

Como funciona …

Medimos: participação ativa · missões concluídas · % metas batidas

Habilitadores: Plataforma de Pontos (moeda) · Glorya Card (opcional)

CTA: Agendar diagnóstico · Ver clientes

/engajar/reconhecimento — Reconhecimento & Incentivos

H1: Comportamento certo, na frequência certa, com premiação justa.

Sub: Regras claras, rituais recorrentes e governança visível.

Para quem: RH/People · Vendas/Marketing · Operações

Cenários: Reconhecimento aleatório · Baixa motivação · Provar impacto

O que entregamos: Critérios · Rituais mensais · Relatórios/auditoria

Como funciona …

Medimos: % reconhecidos/mês · justiça percebida · uso das recompensas

Habilitadores: Plataforma de Pontos · Glorya Card

CTA: Agendar diagnóstico · Ver clientes

/engajar/eventos — Experiências & Eventos

H1: Picos de conexão que celebram e impulsionam o próximo ciclo.

Sub: Pré (qualificação) · Durante (reconhecimento) · Pós (missões).

Para quem: Presidência · RH · Marketing · Vendas/Canal

Cenários: Convenção · Viagem de incentivo · Datas especiais

O que entregamos: Teaser/qualificação · Cerimônia/reconhecimento · Missões pós

Como funciona …

Medimos: presença qualificada · NPS do evento · engajamento pós

Habilitadores: Plataforma de Pontos · Glorya Card

CTA: Agendar diagnóstico · Ver cases de eventos

Produtos

/recompensar/pontos — Plataforma de Pontos

H1: A moeda do engajamento — simples de gerir.

Quando usar: programas contínuos · campanhas 4–8 semanas · qualificação de eventos

Como funciona: earn/burn · níveis · catálogo · expiração · centros de custo

Governança: regras auditáveis · logs · relatórios por área

Onde usar: Performance · Reconhecimento · Eventos

CTA: Falar com especialista

/recompensar/card — Glorya Card

H1: Premiação instantânea e rastreável.

Quando usar: marcos · campanhas · evento‑rito

Fluxo: emitir → recarregar → usar (pag/saque/transfer) → acompanhar

Experiência do premiado: recebi · ativei · usei

Onde usar: Reconhecimento · Eventos (link para cases)

CTA: Falar com especialista

Cuidar

/cuidar/nr1 — NR‑1 Check

H1: NR‑1 sem mistério: pesquise, diagnostique, aja.

Como funciona: Pesquisa anônima → Heatmap → Plano de ação → Pulsos

Papéis & dados: RH/Liderança/CIPA · LGPD · relatórios para auditoria

Conecta com: Pessoas & Cultura

CTA: Quero rodar a pesquisa

Provar / Clientes / Aprender / Sobre / Contato

/provar — Cases (Eventos)

Lista: Contexto (1 linha) · O que fizemos (1) · 3 métricas · Ver case

Página do case: desafio → solução → pré/durante/pós → números → fotos → citação

CTA: Quero algo assim

/clientes

Mosaico de logos (mono) + 3–5 depoimentos curtíssimos

CTA: Fazer diagnóstico

/aprender

Cards de Guias, Checklists, Calculadora de ROI (3 inputs)

CTA: Baixar/Assistir · Quero validar com vocês

/sobre

Manifesto (1 parágrafo) · Método (4 passos) · Time (enxuto)

CTA: Fale com a Glorya

/contato

Form multi‑etapas: pilar → dor/objetivo → porte → prazo → contato

Sucesso: mensagem clara + link de agenda

🔗 Ligações entre páginas (essência)

Portal → Hub/Diagnóstico

Hub → Pilares / Recompensar (Pontos, Card) / Cuidar (NR‑1) / Provar / Clientes

Diagnóstico → 1 pilar recomendado + habilitadores + Contato

Pessoas & Cultura → NR‑1 + Clientes + Contato

Performance → Pontos (+Card) + Clientes + Contato

Reconhecimento → Pontos + Card + Clientes + Contato

Eventos → Pontos + Card + Cases + Contato

Produtos (Pontos/Card) ↔ Pilares correspondentes → Contato

📦 Estrutura de pastas (Next.js)
src/
  app/
    page.tsx                       # Splash
    hub/page.tsx                   # Hub (mandala)
    diagnostico/page.tsx
    engajar/
      pessoas/page.tsx
      performance/page.tsx
      reconhecimento/page.tsx
      eventos/page.tsx
    recompensar/
      pontos/page.tsx
      card/page.tsx
    cuidar/nr1/page.tsx
    provar/page.tsx
    clientes/page.tsx
    aprender/page.tsx
    sobre/page.tsx
    contato/page.tsx
    (site)/[...slug]/page.tsx      # páginas CMS do Builder (opcional)
  components/                      # hero, chips, cards, stepper, métricas, faq, mandala, wizard
  lib/builder.ts                   # init do Builder
  app/globals.css                  # estilos globais (tokens dark)
  ...

⚙️ Setup (local → GitHub → Vercel → Builder)
1) Local
nvm install --lts && nvm use --lts
corepack enable && corepack prepare pnpm@latest --activate

pnpm create next-app@latest . \
  --ts --eslint --tailwind --app --src-dir --import-alias "@/*" --use-pnpm
echo "v20" > .nvmrc

pnpm add @builder.io/react

2) GitHub

Criar repositório Glorya → push do código.

Proteger main (PR + checks).

3) Vercel

Import Project do GitHub

Node 20 (opcional)

Environment Variables: NEXT_PUBLIC_BUILDER_API_KEY (depois de criar no Builder)

Deploy: Preview (PR) + Production (merge)

4) Builder.io

Space: Glorya Site

API Keys → copie a Public

.env.local (e Vercel):

NEXT_PUBLIC_BUILDER_API_KEY=xxxxxxxxxxxxxxxx


Models:

page (campos: title: text, url: urlPath)

section (para blocos reutilizáveis)

(Opcional) Webhooks: Builder “Publish” → Vercel Deploy Hook

5) Rota Builder “catch‑all” (opcional)

src/app/[(site)]/[...slug]/page.tsx deve buscar e renderizar page do Builder (exemplo incluído acima).

📊 Medição (GA4 – eventos recomendados)

view_hub, click_pilar {name}, view_solution {pillar},

view_product {name}, start_diagnostico, finish_diagnostico {route},

generate_lead, view_case {tipo}, calc_roi_submit.

♿ Acessibilidade

Foco visível (outline: 2px solid #FF005E) em todos os elementos interativos.

Alvos ≥ 44×44px; navegação por teclado na mandala e no wizard.

Contraste AA no tema dark; lang="pt-br"; semântica header/nav/main/section/footer.

🧪 CI/CD

GitHub Actions (.github/workflows/ci.yml):

pnpm install · pnpm typecheck · pnpm lint · pnpm build

Vercel:

Preview para cada PR

Produção em merges na main

🛠️ Troubleshooting (Vercel)

Error: No Next.js version detected → o repo precisa de package.json com next, react, react-dom e scripts build/start; ou ajustar Root Directory se o código estiver em subpasta.

404 de páginas do Builder → conferir urlPath no conteúdo, publicar (não Draft), e variável NEXT_PUBLIC_BUILDER_API_KEY.

📄 Licença

MIT (ajuste se preferir).

✅ Aceite / Critérios para “OK infra”

Preview Vercel abre Splash (/).

/hub renderiza mandala (mesmo que estática inicialmente).

Chave do Builder setada em Preview/Prod.

Uma página criada no Builder (/sobre) abre via rota [(site)]/[...slug].

Menus e CTAs seguem a navegação “opção 2” e cores/Roboto definidas.

Observação importante: o README não executa; ele orienta. Para que o Builder “puxe” páginas, garanta:

SDK inicializado com a API key

Rota que busca page pelo urlPath

Model page criado e conteúdo publicado

Deploy na Vercel com a variável configurada
