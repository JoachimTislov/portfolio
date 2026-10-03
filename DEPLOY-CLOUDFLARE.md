# Cloudflare Workers deploy

Deploy this Vite site to Cloudflare Workers as static assets.

## One-time setup

1. Cloudflare dashboard: Workers & Pages -> Create Application, or just use API. Create an API token with the "Edit Cloudflare Workers" template.
2. Copy your Account ID (Workers & Pages overview, right sidebar).
3. GitHub repo Settings -> Secrets and variables -> Actions:
   - CLOUDFLARE_API_TOKEN
   - CLOUDFLARE_ACCOUNT_ID
4. Merge this branch into main. The workflow runs on every push to main.

Config lives in wrangler.jsonc. Build output is ./dist. Static asset serving on Workers is unmetered; only storage above 500 MB costs anything ($0.02/GB-month).
