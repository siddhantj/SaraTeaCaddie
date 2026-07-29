# Sara's Tea Caddie — deploying to Vercel

A real multi-page static site. Every page is its own URL and its own file, with
normal `<a href>` navigation — no build step, no framework.

```
vercel-site/
  index.html         →  /                (Home)
  about.html         →  /about
  teas.html          →  /teas
  how-to-brew.html   →  /how-to-brew
  contact.html       →  /contact
```

Each file is fully self-contained (fonts, images and runtime inlined, ~1.7 MB),
so the site works offline and from any host.

## Option A — drag & drop
1. Go to https://vercel.com/new
2. "Deploy" → drag this whole `vercel-site` folder onto the drop zone.
3. Vercel serves clean URLs automatically (`/about`, `/teas`, …).

## Option B — Git + Vercel CLI
```bash
cd vercel-site
npx vercel            # preview deploy
npx vercel --prod     # production
```
Framework preset: **Other**. Build command: empty. Output directory: `.`

## Custom domain
Vercel project → Settings → Domains → add `teacaddie.com` and `www.teacaddie.com`,
then set the DNS records it shows you at the registrar.

## Still to do before launch
- **Contact form** is presentational: it shows the confirmation state but does
  not deliver email. Wire it to Formspree/Basin or a Vercel function — say the
  word and I'll add it.
- **Photography**: the tea and hero images are generated stand-ins. Drop Sara's
  real photos onto the image slots in the design, then re-export.
- **Email address**: the business card scans as `leacaddie.com`; the site uses
  `sara@teacaddie.com`. Please confirm.
