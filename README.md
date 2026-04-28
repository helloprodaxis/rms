# RestoSuite — Landing Page

Single-page proposal/landing site for the Restaurant Management SaaS. Pure static HTML + Tailwind (CDN). No build step required.

## Quick local preview
```bash
npm install
npm run dev
```
Open http://localhost:3000

(You can also just double-click `index.html` to open it directly — no server needed.)

## Deploy to Vercel — first time

### Option A: GitHub → Vercel (recommended)
1. Push this folder to GitHub:
   ```bash
   git init
   git add index.html README.md vercel.json .gitignore
   git commit -m "Initial RestoSuite landing page"
   git branch -M main
   git remote add origin https://github.com/helloprodaxis/rms.git
   git push -u origin main
   ```
2. Go to https://vercel.com/new
3. Import the `helloprodaxis/rms` repo.
4. Framework preset: **Other** (Vercel auto-detects static HTML).
5. Click **Deploy** — done in ~30 seconds.
6. Vercel gives you a live URL like `https://rms-xxxx.vercel.app`. Share that link.

### Option B: Vercel CLI (one-shot)
```bash
npm i -g vercel
vercel --prod
```
Follow the prompts. First-time login is via browser.

## Push future changes
Any `git push` to `main` auto-redeploys on Vercel within seconds.

## Customising before going live
Open `index.html` and edit:
- **Brand name** — find/replace `RestoSuite` (appears in nav, footer, page title).
- **Phone** — find/replace `919999999999` (WhatsApp link) and `+91 99999 99999` (footer).
- **Email** — find/replace `hello@example.com`.
- **Domain charge note** — already shows "domain ~Rs. 500–999/year is paid by you directly" near pricing.
- **Colours** — edit the Tailwind config block at the top of `<head>` (`brand`, `gold`, `mint`, `cream`).

## What's in this repo
- `index.html` — the entire landing page (single file).
- `README.md` — this file.
- `vercel.json` — minimal Vercel config (clean URLs, no extension on /).
- `.gitignore` — ignore OS/editor noise.
- `CLIENT-PROPOSAL.md` — long-form proposal document for one-on-one client sharing (separate from the landing page).

## Custom domain
After Vercel deploys, in **Settings → Domains** add the customer's purchased domain (e.g. `restosuite.in`). Vercel will give you DNS records to point at it. SSL is auto-provisioned and free.
