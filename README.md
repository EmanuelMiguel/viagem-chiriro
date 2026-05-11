# Viagem de Chihiro — Projeto (Single Page)

## Descrição
- Projeto estático: uma página única (landing) inspirada em "A Viagem de Chihiro".

## O que foi usado
- HTML5: estrutura em `index.html`.
- CSS3: estilos em `css/style.css` (Flexbox, media queries para responsividade).
- Google Fonts: `Andada Pro` e `Archivo` (importadas via link em `index.html`).
- Imagens e ícones: arquivos em `images/` (logo.svg, image.svg, wallpaper.png, favicon.png, e a pasta `images/icones/`).
- SVG: ícones e ilustrações — uso de SVG inline no botão e imagens vetoriais externas.


Pontos importantes
- O botão `.botao` utiliza a fonte `Roboto` no `css/style.css`, porém o `Roboto` não está importado no `index.html`. Se desejar usá-la, adicione o import do Google Fonts ou atualize `css/style.css` para usar uma fonte já carregada.
- Paths de imagens usam raízes relativas e algumas referências começam com `/images/...`; ao servir por servidor local, confirme o comportamento do caminho (abrir pelo filesystem geralmente funciona, mas em servidores o `/` pode referir-se à raiz do host).

## Estrutura do projeto

- `index.html` — página principal.
- `css/style.css` — estilos principais.
- `images/` — imagens usadas pelo layout:
  - `image.svg` — ilustração principal.
  - `wallpaper.png` — imagem de fundo.
  - `logo.svg`, `favicon.png` — identidade visual.
  - `icones/` — ícones sociais (Google, Facebook, Twitter/X, Instagram).
- `docs/googe-fonts.txt` — arquivo com informações/links das fontes.

## Autor

- Iuri Code - @iuricode - Projeto do Figma

### Créditos
- Fontes: Google Fonts (`Andada Pro`, `Archivo`).
- Conteúdo e identidade visual: projeto pessoal / assets locais.

---

Arquivo gerado automaticamente pelo assistente.
