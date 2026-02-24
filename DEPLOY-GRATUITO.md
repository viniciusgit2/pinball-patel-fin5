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

## Opção 1 (mais simples): Netlify grátis
1. Crie conta em https://app.netlify.com/
2. Clique em **Add new site** > **Deploy manually**
3. Arraste a pasta do projeto inteira (`pinball-patel-fin5`)
4. O site vai ficar em um domínio gratuito do tipo:
   - `https://nome-aleatorio.netlify.app`
5. Em **Site settings** > **Domain management**, altere para um nome disponível:
   - Exemplo: `https://viniciusgames.netlify.app`

## Opção 2: GitHub Pages grátis (recomendado agora)
1. Crie um repositório no GitHub com o nome `pinball-patel-fin5`.
2. Envie os arquivos do projeto para a branch `main`.
3. Vá em **Settings** > **Pages** e selecione **GitHub Actions**.
4. O workflow `Deploy GitHub Pages` vai publicar automaticamente.
5. URL gratuita final:
   - `https://viniciusgit2.github.io/pinball-patel-fin5/`

## Sobre domínio `.com.br`
Importante para “sem custos adicionais”:
- Domínio `.com.br` no Registro.br normalmente é pago (anual).
- Se quiser custo zero, use o domínio gratuito do GitHub Pages ou Netlify.

### Cenário A: Registro.br + Netlify (recomendado)
1. Publique o site no Netlify primeiro e confirme que está funcionando no endereço `*.netlify.app`.
2. No Netlify, vá em **Site settings** > **Domain management** > **Add custom domain**.
3. Adicione:
   - `viniciusgames.com.br`
   - `www.viniciusgames.com.br`
4. No Registro.br, em **DNS**, configure:
   - Tipo `CNAME` | Nome `www` | Valor: domínio Netlify do seu site (ex.: `viniciusgames.netlify.app`)
   - Tipo `A` | Nome `@` | Valor: IPs informados pelo Netlify para apex/root
5. Aguarde propagação DNS (até 24h).

### Cenário B: Registro.br + GitHub Pages
1. Publique no GitHub Pages e confirme que abre no endereço `https://viniciusgit2.github.io/pinball-patel-fin5/`.
2. No repositório, em **Settings** > **Pages**, adicione domínio customizado `www.viniciusgames.com.br`.
3. No Registro.br, em **DNS**, configure:
   - Tipo `CNAME` | Nome `www` | Valor: `viniciusgit2.github.io`
   - Tipo `A` | Nome `@` | Valor: `185.199.108.153`
   - Tipo `A` | Nome `@` | Valor: `185.199.109.153`
   - Tipo `A` | Nome `@` | Valor: `185.199.110.153`
   - Tipo `A` | Nome `@` | Valor: `185.199.111.153`
4. Aguarde propagação DNS (até 24h).

### 100% gratuito (sem pagar domínio)
Use uma destas URLs:
- Netlify: `https://viniciusgames.netlify.app` (se disponível)
- GitHub Pages: `https://viniciusgit2.github.io/pinball-patel-fin5/`

## Observação importante
- O arquivo `dados-bancarios.json` está ignorado no Git (`.gitignore`), então não vai para o GitHub.
