# Deploy voice.refocus.co.in on Vercel

Static site. No build step.

## 1) Deploy from GitHub (easiest)

1. Go to [vercel.com/new](https://vercel.com/new)
2. Import `PriyanshuShekhar10/voice-refocus`
3. Settings:
   - **Framework Preset:** Other
   - **Root Directory:** `website`  
     *(or leave root and use the repo-level `vercel.json` that points at `website`)*
   - **Build Command:** leave empty
   - **Output Directory:** leave empty if Root Directory is `website`
4. Deploy

## 2) Custom domain

1. Vercel project → **Settings → Domains** → add `voice.refocus.co.in`
2. In Cloudflare DNS for `refocus.co.in`, add what Vercel shows, usually:
   - Type: `CNAME`
   - Name: `voice`
   - Target: `cname.vercel-dns.com` (or the exact target Vercel gives)
   - Proxy status: **DNS only** (grey cloud) — recommended for Vercel

## Store URLs

- Homepage: `https://voice.refocus.co.in`
- Privacy: `https://voice.refocus.co.in/privacy` (clean URL) or `/privacy.html`

## After Chrome approval

Set the real Chrome Web Store link on the “Add to Chrome” button in `index.html`.

## Contact

`hello@refocus.co.in`
