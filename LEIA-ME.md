# TexelTools — guia rápido

Site estático com 3 ferramentas que rodam 100% no navegador:

| Arquivo | Página |
|---|---|
| `index.html` | Gerador de Normal Map + compressor |
| `sprite-sheet.html` | Empacotador de sprite sheet (PNG + JSON para Phaser/PixiJS) |
| `converter.html` | Conversor e compressor de imagens em lote (WebP/JPEG/PNG + ZIP) |
| `privacy.html` | Política de privacidade (exigida pelo AdSense) |
| `sitemap.xml`, `robots.txt` | SEO |
| `vercel.json` | URLs limpas (`/converter` em vez de `/converter.html`) |

## Antes de publicar: troque os marcadores

1. **`SEU-DOMINIO.com`** em `sitemap.xml` e `robots.txt` → seu domínio real.
2. **`CONTACT_EMAIL`** em `privacy.html` (aparece 2 vezes) → um e-mail de contato. Use um e-mail separado do pessoal, porque ele fica público.

## Deploy

1. Crie um repositório público no GitHub e envie **todos** os arquivos desta pasta (na raiz do repositório).
2. Na Vercel: *Add New Project* → escolha o repositório → *Deploy*.
3. Em *Settings → Domains*, conecte o seu domínio próprio.

## Google Search Console

1. Adicione a propriedade com o seu domínio.
2. Em *Sitemaps*, envie `https://SEU-DOMINIO.com/sitemap.xml`.

## AdSense (quando for a hora)

1. Cadastre o domínio próprio no AdSense.
2. Cole o script que o Google fornecer dentro do `<head>` das **4** páginas `.html`.
3. Crie um arquivo `ads.txt` na raiz com a linha que o AdSense mostrar (algo como `google.com, pub-XXXXXXXXXXXXXXXX, DIRECT, f08c47fec0942fa0`).
4. Para visitantes da Europa, Reino Unido e Brasil, ative a mensagem de consentimento de cookies em *Privacidade e mensagens* no próprio AdSense.

## Adicionar uma ferramenta nova

Copie uma página existente, troque título, descrição e conteúdo, adicione o link no `<nav>` de todas as páginas e uma linha nova no `sitemap.xml`.
