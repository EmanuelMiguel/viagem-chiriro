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
- `googe-fonts.txt` — arquivo com informações/links das fontes (typo no nome: "googe").

Como abrir/desenvolver
- Abrir `index.html` diretamente no navegador (duplo clique) para ver o layout estático.
- Para servir via HTTP (recomendado), rode um servidor simples na raiz do projeto. Exemplo com Python 3:

```bash
python3 -m http.server 8000
# depois abra http://localhost:8000 no navegador
```

Sugestões rápidas
- Se quiser que eu adicione o import do `Roboto` (ou ajuste as fontes), posso atualizar `index.html` e `css/style.css`.
- Posso também otimizar paths de imagens (remover a barra inicial `/` se for necessário) ou compactar imagens para melhorar carregamento.

Créditos
- Fontes: Google Fonts (`Andada Pro`, `Archivo`).
- Conteúdo e identidade visual: projeto pessoal / assets locais.

---

Arquivo gerado automaticamente pelo assistente.
