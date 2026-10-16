# scott-links

Personal link cards for Scott Eggert (conference QR / NFC).

## Two branches, two sites

| Branch | Card | Hosting | Domain |
|--------|------|---------|--------|
| **`main`** | GoldenDoodle AI (`index.html` at repo root) | Netlify (existing project) | [scott.goldendoodleai.com](https://scott.goldendoodleai.com) |
| **`mktng-card`** | MKTNG (`index.html` at repo root on this branch only) | Cloudflare Pages (`scott-mktng`) | Point your MKTNG custom domain at the `scott-mktng` Pages project |

Do not merge these branches — each branch is a separate deploy root with a different file set.

- **`main`**: GoldenDoodle card and `/mktng/` on Netlify. Do not change Netlify settings for that site.
- **`mktng-card`**: Self-contained MKTNG card only. Pushes run `.github/workflows/deploy-mktng.yml`, deploying the repository root with `npx wrangler@4 pages deploy . --project-name scott-mktng --branch main`. Set GitHub secrets `CLOUDFLARE_API_TOKEN` and `CLOUDFLARE_ACCOUNT_ID` when ready.

## MKTNG card files (this branch)

| File | Purpose |
|------|---------|
| `index.html` | MKTNG link card |
| `mktng-logo-white.png` | Header and Visit MKTNG button |
| `scott.png` | Headshot |
| `goldendoodle-icon.png` | GoldenDoodle AI button |
| `scott-eggert-mktng.vcf` | Save My Contact |
| `fonts/` | Self-hosted Poppins and Plus Jakarta Sans |

Static HTML/CSS only — no build step.

## Local preview (`mktng-card` branch)

```bash
python3 -m http.server 8765
# open http://localhost:8765/
```
