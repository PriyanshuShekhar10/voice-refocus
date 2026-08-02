# Voice Refocus

Chrome extension that reduces distracting background noise and music so speech is easier to follow. Processing stays on your device.

**Site:** [voice.refocus.co.in](https://voice.refocus.co.in) *(deploy the `website/` folder)*

## Repo layout

| Path | Purpose |
| --- | --- |
| `website/` | Landing + privacy pages for `voice.refocus.co.in` |
| `refocus-publish/` | Chrome Web Store upload package (minified) |
| `scripts/build-publish.mjs` | Rebuild the store package |
| Root `*.js` / `popup.*` | Extension source used by the build |

## Load unpacked (dev)

1. `chrome://extensions` → Developer mode  
2. **Load unpacked** → select `refocus-publish/`

## Rebuild store zip

```bash
npm install
node scripts/build-publish.mjs
```

Creates `../refocus-chrome-store.zip`.

## Privacy

- Policy page: `website/privacy.html`  
- Contact: hello@refocus.co.in
