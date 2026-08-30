# Deployment

Arvel Scholar is a static Hugo site. Cloudflare Workers is optional.

## Build locally

```bash
hugo
```

## Cloudflare Workers

1. Install Node.js 20 or newer.
2. Run `npm install`.
3. Change `name` in `wrangler.jsonc` to an available Worker name.
4. Authenticate with `npx wrangler login`.
5. Verify with `npm run deploy:dry-run`.
6. Deploy with `npm run deploy`.

The Worker serves the files generated in `public/`. No secret is required by this template.

## Other hosting providers

Deploy the generated `public/` directory. Set `baseURL` in `config.yml` to the final site URL when your host requires absolute canonical URLs.

