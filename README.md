# Konohaven guide

Guide for moving your Minecraft settings (`options.txt`, `config`, `journeymap`) to a new instance after an update.

The site is the `public/` folder. Cloudflare Workers serves it as static files.

## Deploying

1. Push this repo to GitHub.
2. In the Cloudflare dashboard go to **Workers & Pages → Create → Import a repository** and pick this repo.
3. Leave the build command empty and keep the deploy command as `npx wrangler deploy`.
4. Deploy. It'll be live at `konohaven-guide.<your-subdomain>.workers.dev`, and every push to `main` redeploys it.

To use your own domain, open the Worker → **Settings → Domains & Routes → Add**.

## Editing

- Page text: `public/index.html`
- Styling: `public/style.css`

To preview locally: `npx wrangler dev`, then open http://localhost:8787
