# Vanguard Digital

Marketing website for Vanguard Digital — premium, high-converting websites for Irish businesses.

A single self-contained static page: `index.html` (hand-written CSS, no build step) plus optimized images in `assets/`.

## Local preview

Any static server works, e.g.:

```bash
npx serve .
# or
python -m http.server 8000
```

Then open the printed URL.

## Deploy to Vercel

This is a zero-config static site. Two options:

**A. GitHub-connected (recommended — auto-deploys on push)**
1. Push this folder to a new GitHub repo (see below).
2. Go to vercel.com → **Add New… → Project** → import the repo.
3. Framework preset: **Other**. Build command: _(none)_. Output directory: _(leave blank / `.`)_.
4. Deploy.

**B. Vercel CLI**
```bash
npm i -g vercel
vercel        # preview deploy
vercel --prod # production deploy
```

## Push to GitHub

```bash
git remote add origin https://github.com/<you>/vanguard-digital.git
git push -u origin main
```

## Before going live — checklist

- [ ] **Contact form:** in `index.html`, replace `YOUR_FORM_ID` (the `<form action>`) with your Formspree form ID from https://formspree.io.
- [ ] **Domain:** update the canonical and Open Graph URLs in `<head>` to your real domain.
- [ ] **Email:** replace the placeholder `hello@vanguarddigital.ie` with your real address.
- [ ] **OG image:** point `og:image` at an absolute URL (e.g. `https://yourdomain/assets/og.png`) so link previews work.

## Structure

```
index.html        # the whole site (markup + CSS + JS)
assets/
  hero.jpg        # hero (skyscraper)
  contact.jpg     # contact backdrop (interior)
  logo-cropped.png# hero logo lockup
  logo-mark.png   # navbar V mark
  logo.png        # full-resolution logo (source / OG)
vercel.json       # caching + security headers
```
