# Viagem de Chihiro — Projeto (Single Page)

## Descrição
- Projeto estático: uma página única (landing) inspirada em "A Viagem de Chihiro".

## O que foi usado

### Linguagens e Tecnologias
- **HTML5**: estrutura semântica em `index.html` e `pages/trailer.html`.
- **CSS3**: estilos em `css/style.css` com Flexbox, Grid, e media queries para responsividade (breakpoints: 1440px, 768px, 500px, 390px).
- **Google Fonts**: fontes `Andada Pro` (serif) e `Archivo` (sans-serif) importadas via link preconectado em `index.html`.
- **SVG**: ilustrações vetoriais — logo, ícones sociais e elementos gráficos em `images/icones/`.
- **Imagens**: PNG e SVG para wallpaper, favicon e assets visuais.
- **Embedded Media**: iframe YouTube para reprodução de trailer em `pages/trailer.html`.

### Estrutura de Arquivos e Pastas

- **`index.html`** — página principal com layout da landing de "A Viagem de Chihiro".
- **`css/style.css`** — folha de estilos centralizada (244 linhas):
  - Reset universal (`* { margin: 0; padding: 0; box-sizing: border-box; }`).
  - Layout com Flexbox para header, main e conteúdo.
  - Tipografia: `Andada Pro` para títulos (h1-h6), `Arquivo` para parágrafos e botões.
  - Componentes: `.header`, `.nav-links`, `.conteudo`, `.descricao`, `.botoes`, `.botao` (primário e secundário).
  - Efeitos hover com transições de 0.5s.
  - Media queries responsivas.
- **`images/`** — recursos visuais:
  - `logo.svg` — logo do Studio Ghibli.
  - `image.svg` — ilustração principal (personagem/cena).
  - `wallpaper.png` — imagem de fundo (cover, 100vh).
  - `favicon.png` — ícone da aba.
  - **`icones/`** (subpasta com 6 ícones SVG):
    - `logo-google.svg`, `logo-facebook.svg`, `logo-twitter.svg`, `logo-instagram.svg` — redes sociais.
    - `Play.svg`, `movie.svg` — ícones adicionais (Play para botão, movie para outros elementos).
- **`pages/trailer.html`** — página adicional:
  - Reutiliza header (`..css/style.css`, `../images/`).
  - Contém iframe YouTube com embed do trailer oficial.
  - Links funcionais para redes sociais (`target="_blank"`).
  - Rodapé com crédito ao criador.
- **`docs/google-fonts.txt`** — documentação com links e imports do Google Fonts:
  - Preconnect URLs para otimização.
  - Link CSS com fontes Andada Pro e Archivo em múltiplos pesos.

## Pontos Importantes

- O CSS referencia a fonte `Roboto` em `.botao { font-family: 'Roboto', sans-serif; }`, porém esta não é importada no `index.html`. Atualmente, o navegador usa fallback para sans-serif genérico. Para usar `Roboto`, adicione o import via Google Fonts ou atualize a fonte para `Archivo` (já carregada).
- Paths de imagens no `index.html` usam `/images/...` (caminho absoluto desde a raiz). No `pages/trailer.html`, usam `../images/...` (relativo). Ambos funcionam, mas confirme o comportamento em servidor HTTP.
- A página `pages/trailer.html` vincula corretamente aos links sociais oficiais do Studio Ghibli (USA) com `target="_blank"`.

## Como Abrir/Desenvolver

- **Abrir localmente**: duplo clique em `index.html` para visualizar no navegador (funciona diretamente do filesystem).
- **Servir via HTTP** (recomendado para melhor comportamento de paths): utilize um servidor simples. Exemplos:

```bash
# Python 3
python3 -m http.server 8000

# Node.js (com http-server)
npx http-server
```

Depois acesse `http://localhost:8000` (ou a porta configurada).

- **Acessar trailer**: navegue para `http://localhost:8000/pages/trailer.html` ou clique no botão "ASSISTA O TRAILER" se implementado em `index.html`.

## Componentes e Funcionalidades

### Paleta de Cores
- **Branco/Off-white**: `#fff`, `#f8f8f8` — textos, backgrounds em hover.
- **Preto**: `#0B0A0A` — textos secundários, contraste.
- **Rosa Ghibli**: `#F1A5B1` — cor primária, botões, links hover, bordas.
- **Transparência**: `rgba(248, 248, 248, 0.31)` — efeito glassmorphism nos links de redes.

### Tipografia Detalhada
- **Headings (h1-h6)**: `Andada Pro` (serif, weights 400-840).
- **Body/Paragraphs**: `Archivo` (sans-serif, weights 100-900).
- **Botões**: `Roboto` (fallback para sans-serif genérico, não importada).
- **Tamanhos principais**:
  - Título (h2): 64px (desktop) → 40px (mobile).
  - Autor (h3): 20px.
  - Parágrafo: 24px (desktop) → 16px (mobile).
  - Botão: 18px, weight 700.

### index.html
- **Header**: logo + links para redes sociais com hover effect.
- **Seção principal (`.conteudo`)**:
  - `.descricao`: título "A VIAGEM DE CHIHIRO", autor "HAYAO MIYAZAKI", sinopse.
  - `.botoes`: 2 botões (primário com ícone play, secundário com borda).
  - `.ilustracao`: background SVG alinhado à direita.

### CSS Responsividade
- **1440px e abaixo**: conteudo em coluna, ilustração acima do texto.
- **768px e abaixo**: fonte menor, botões em coluna, layout mais compacto.
- **500px e abaixo**: nav links desaparecem, header centralizada.
- **390px e abaixo**: header reduzido, logo redimensionada.

### pages/trailer.html
- **Estrutura similar** ao `index.html` (reutiliza CSS e assets).
- **Player**: iframe YouTube com embed responsivo do trailer oficial.
- **Rodapé**: crédito "Created by Emanuel Miguel".

## Como Contribuir / Próximos Passos

- Adicionar funcionalidade aos botões (links para assister, trailer, etc.).
- Otimizar imagens para reduzir tamanho da página.
- Melhorar acessibilidade (ARIA labels, contrast ratios).
- Adicionar animações CSS mais sofisticadas.
- Implementar versão dark mode se desejado.

## Autor

- Iuri Code - @iuricode - Projeto do Figma

### Créditos
- Fontes: Google Fonts (`Andada Pro`, `Archivo`).
- Conteúdo e identidade visual: projeto pessoal / assets locais.

---

Arquivo gerado automaticamente pelo assistente.
