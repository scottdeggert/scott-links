# scott-links

Personal link pages for Scott Eggert — virtual business cards for conference networking. Designed to be scanned via QR code or NFC tap.

**Live (GoldenDoodle AI):** [scott.goldendoodleai.com](https://scott.goldendoodleai.com)  
**Live (MKTNG):** [scott.goldendoodleai.com/mktng/](https://scott.goldendoodleai.com/mktng/)

## What's here

| Path | Purpose |
|---|---|
| `index.html` | GoldenDoodle AI card — Founder & CEO lead, trauma-informed AI positioning |
| `mktng/index.html` | MKTNG card — President of MKTNG lead, agency/comms positioning |
| `scott.png` | Headshot (shared) |
| `mktng-logo.png` | MKTNG logo (shared) |
| `scott-eggert.vcf` | vCard for GDAI card |
| `mktng/scott-eggert-mktng.vcf` | vCard for MKTNG card |

Static HTML/CSS only — no build step, no dependencies.

## Hosting

Static site on Netlify (free tier). Auto-deploys on push to `main`. Custom subdomain via CNAME record pointing `scott` → `scott-links.netlify.app`.

Folder routes (`/mktng/`) work out of the box on Netlify.

## Editing

Open in Cursor, edit the relevant `index.html`, push. No dependencies, no build process.

## GoldenDoodle AI card (`/`)

| Button | Destination |
|---|---|
| Try GoldenDoodle Free | goldendoodleai.com/founderoffer |
| Connect on LinkedIn | linkedin.com/in/scottdeggert |
| Free Dignity Audit | dignityaudit.com |
| Book a Conversation | calendly.com/scotteggert |
| My Marketing Agency | mktng.co |
| Save My Contact | Downloads scott-eggert.vcf |

Footer links to goldendoodleai.com. Discreet cross-link to MKTNG card.

## MKTNG card (`/mktng/`)

| Button | Destination |
|---|---|
| Visit MKTNG | mktng.co |
| Connect on LinkedIn | linkedin.com/in/scottdeggert |
| Book a Conversation | calendly.com/scotteggert |
| Save My Contact | Downloads scott-eggert-mktng.vcf |

Footer links to goldendoodleai.com. Discreet cross-link to GDAI card.

## Local preview

```bash
# From repo root — open either card in a browser
open index.html
open mktng/index.html
```
