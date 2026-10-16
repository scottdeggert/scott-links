# scott-links

Personal link cards for Scott Eggert (conference QR / NFC).

## Two branches, two sites

| Branch | Card | Hosting | Domain |
|--------|------|---------|--------|
| **`main`** | GoldenDoodle AI (`index.html` at repo root) | Netlify (existing project) | [scott.goldendoodleai.com](https://scott.goldendoodleai.com) |
| **`mktng-card`** | MKTNG (static assets in `public/`) | Cloudflare Worker **`scott-mktng-card`** | [scott.mktng.co](https://scott.mktng.co) |

Do not merge these branches — each branch is a separate deploy root with a different file set.

- **`main`**: GoldenDoodle card and `/mktng/` on Netlify. Do not change Netlify settings for that site.
- **`mktng-card`**: Self-contained MKTNG card in `public/`. Pushes run `.github/workflows/deploy-mktng.yml`, which runs `npx wrangler@4 deploy` using `wrangler.toml` (Worker name `scott-mktng-card`, assets from `./public`). Set GitHub secrets `CLOUDFLARE_API_TOKEN` and `CLOUDFLARE_ACCOUNT_ID` when ready.

## MKTNG card files (this branch)

| Path | Purpose |
|------|---------|
| `public/index.html` | MKTNG link card |
| `public/mktng-logo-white.png` | Header logo |
| `public/mktng-logo-all-white.png` | Visit MKTNG button icon |
| `public/scott.png` | Headshot |
| `public/goldendoodle-icon.png` | GoldenDoodle AI button |
| `public/scott-eggert-mktng.vcf` | Save My Contact |
| `public/fonts/` | Self-hosted Poppins and Plus Jakarta Sans |
| `wrangler.toml` | Worker + assets + `scott.mktng.co` route |

Static HTML/CSS only — no build step.

## Local preview (`mktng-card` branch)

```bash
cd public && python3 -m http.server 8765
# open http://localhost:8765/
```

Or preview with Wrangler (requires Cloudflare credentials):

```bash
npx wrangler@4 dev
```
