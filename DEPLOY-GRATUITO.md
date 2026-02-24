# Publicação gratuita do site

Status atual deste projeto:
- Já está pronto para deploy automático no GitHub Pages.
- Workflow criado em `.github/workflows/deploy-pages.yml`.
- Arquivo `.nojekyll` criado para evitar conflitos de publicação estática.

Este projeto já está organizado com separação de conteúdo:
- `index.html`: página principal (apresentação + submenu Jogos)
- `pagamento.html`: tela de pagamento
- `jogo.html`: jogo de pinball
- `game.js`, `styles.css`, `audio-jogo.mp3`: arquivos de jogabilidade

## Deploy via GitHub Pages (única opção)
1. Crie um repositório no GitHub com o nome `pinball-patel-fin5`.
2. Envie os arquivos do projeto para a branch `main`.
3. Vá em **Settings** > **Pages** e selecione **GitHub Actions**.
4. O workflow `Deploy GitHub Pages` vai publicar automaticamente.
5. URL gratuita final:
   - `https://viniciusgit2.github.io/pinball-patel-fin5/`

## URL final
- `https://viniciusgit2.github.io/pinball-patel-fin5/`

## Observação importante
- O arquivo `dados-bancarios.json` está ignorado no Git (`.gitignore`), então não vai para o GitHub.
