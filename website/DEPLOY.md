# Deploy voice.refocus.co.in

Static site in this folder. No build step.

## Option A — Cloudflare Pages (recommended)

Your apex `refocus.co.in` is already on Cloudflare.

1. Cloudflare Dashboard → **Workers & Pages** → **Create** → **Pages**
2. Upload this `website` folder, **or** connect a Git repo and set:
   - Build command: *(none / empty)*
   - Output directory: `website` (or `/` if the repo root is this folder)
3. After the first deploy, open the project → **Custom domains**
4. Add: `voice.refocus.co.in`
5. Cloudflare will create the DNS record for you

Site URLs to use in Chrome Web Store:
- Homepage: `https://voice.refocus.co.in`
- Privacy policy: `https://voice.refocus.co.in/privacy.html`

## Option B — Manual DNS + any static host

1. Host the contents of `website/` (Netlify, GitHub Pages, S3, etc.)
2. In Cloudflare DNS for `refocus.co.in`, add:
   - Type: `CNAME`
   - Name: `voice`
   - Target: your host’s URL (e.g. `something.pages.dev`)
   - Proxy: ON (orange cloud) if using Cloudflare Pages/proxy

## After Chrome Web Store approval

Edit `index.html` and set the real listing URL on `#chromeLink`.

## Email

Privacy page uses `hello@refocus.co.in`. Create that mailbox (or change both `index.html` and `privacy.html` to an address you monitor).
