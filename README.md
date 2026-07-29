# Sara's Tea Caddie — static site

Five plain HTML pages. **No JavaScript, no framework, no build step** — the
browser paints them on first byte, so navigation is instant with no flash.

```
index.html         →  /
about.html         →  /about
teas.html          →  /teas
how-to-brew.html   →  /how-to-brew
contact.html       →  /contact
assets/*.jpg       →  tea and hero imagery
```

## Deploy
Drag this folder onto https://vercel.com/new (framework preset **Other**,
no build command, output directory `.`), or:

```bash
npx vercel --prod
```

## Custom domain
Vercel project → Settings → Domains → add `teacaddie.com` and `www.teacaddie.com`,
then set the DNS records it gives you at the registrar.

## Editing
- All styling is inline in each HTML file; the only stylesheet is a small block
  in `<head>` (font import, body reset, and the Teas dropdown hover).
- The Teas dropdown is pure CSS `:hover` — no script.
- Shared markup (header, footer) is duplicated per page by design. If you change
  the nav, change it in all five files — or ask me to regenerate them from the
  design file in the project.

## Still to do before launch
- **Contact form** posts nowhere: "Send to Sara" is currently a `mailto:` link.
  To capture submissions properly, wrap the fields in
  `<form action="https://formspree.io/f/YOUR_ID" method="POST">` (Formspree,
  Basin, or a Vercel function) and give each input a `name`. I can wire this up.
- **Photography**: the tea and hero images are generated stand-ins; three slots
  (Sara's portrait ×2, the brewing shot) show a labelled grey plate. Send real
  photos and I'll drop them in.
- **Email address**: the business card scans as `leacaddie.com`; the site uses
  `sara@teacaddie.com`. Please confirm which is correct.
