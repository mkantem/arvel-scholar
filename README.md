# Arvel Scholar

Arvel Scholar is a bilingual academic website template built with [Hugo](https://gohugo.io/) and ready to deploy with [Cloudflare Workers static assets](https://developers.cloudflare.com/workers/static-assets/).

It provides sections for papers, projects, research questions, resources, and writing in English and French. The included content is fictional and is intended to be replaced.

## Theme lineage

Arvel Scholar combines original customization with ideas and code derived from:

- [PaperMod](https://github.com/adityatelange/hugo-PaperMod)
- [Pascal Michaillat's Hugo website template](https://github.com/pmichaillat/hugo-website)

Pascal Michaillat's template is itself based on PaperMod. The PaperMod license is preserved under `themes/PaperMod/LICENSE`.

## Features

- English and French content structure
- publication pages with citation metadata and external links
- dedicated projects, questions, resources, and writing sections
- built-in search and RSS
- light and dark modes
- responsive layouts
- social preview fallback, with post cover images taking priority
- optional deployment to Cloudflare Workers

## Requirements

- [Hugo Extended](https://gohugo.io/installation/) 0.146 or newer
- [Node.js](https://nodejs.org/) 20 or newer for Cloudflare deployment

## Start locally

```bash
git clone https://github.com/mkantem/arvel-scholar.git
cd arvel-scholar
hugo serve
```

Open the address printed by Hugo, normally `http://localhost:1313/`.

## Customize the template

1. Replace `Alex Scholar`, `alex@example.org`, and `https://example.org` in `config.yml`.
2. Update the biography in `content/en/about/` and `content/fr/about/`.
3. Replace the fictional examples under `content/en/` and `content/fr/`.
4. Replace `static/assets/social-preview.png` and `static/assets/favicon-books.png` with your branding.
5. Remove French from `config.yml` and `content/fr/` if you only need one language.

See [docs/customization.md](docs/customization.md) for the complete checklist and [docs/content-guide.md](docs/content-guide.md) for content examples.

## Build

```bash
hugo
```

The generated site is written to `public/` and is intentionally ignored by Git.

## Deploy to Cloudflare Workers

```bash
npm install
npm run deploy:dry-run
npm run deploy
```

Before deploying, change the Worker name in `wrangler.jsonc` and authenticate with `npx wrangler login`. See [docs/deployment.md](docs/deployment.md).

Cloudflare is optional: the generated `public/` directory can be hosted by any static hosting provider.

## Repository structure

```text
assets/css/       Hugo-processed styles
content/en/       English example content
content/fr/       French example content
data/             Optional structured data
layouts/          Arvel Scholar layout overrides
static/assets/    Favicons and social preview assets
themes/PaperMod/  Vendored upstream theme
config.yml        Site, languages, menus, and profile settings
wrangler.jsonc    Optional Cloudflare Workers deployment
```

## Security

Do not commit `.env`, `.dev.vars`, Cloudflare API tokens, or provider credentials. See [SECURITY.md](SECURITY.md) for private vulnerability reports.

## License

Arvel Scholar is released under the [MIT License](LICENSE). Third-party components retain their own copyright and license notices.

