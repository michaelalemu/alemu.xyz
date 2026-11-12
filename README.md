# alemu.xyz

Personal link page for Michael Alemu. Static HTML, no build step, no dependencies.

Live: https://alemuxyz.vercel.app

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole page: markup, styles, fonts (Google Fonts) |
| `photo.jpg` | Hero photo at the top of the page |
| `og.jpg` | 1200×630 link-preview image for WhatsApp, LinkedIn, X, iMessage |

## Run locally

```bash
npx serve .
```

Then open http://localhost:3000. Opening `index.html` directly in a browser also works.

## Deploy

Vercel deploys `main` automatically. Merge to `main` and it's live within a minute.
Vercel settings: Framework preset **Other**, no build command, no output directory.

## Common edits

**Text and links.** Everything is in `index.html`:
- Name, job, city, languages: the `<ul class="facts">` block
- LinkedIn and Instagram: the `<nav class="links">` block

**Hero photo.** Replace `photo.jpg`. Any landscape image works; it is cropped to roughly 3:2 and shown in black and white.

**Link preview.** The `og:` and `twitter:` meta tags near the top of `index.html` control what chats show when the link is shared.
- `og:image` must be an absolute `https://` URL.
- Keep `og.jpg` at 1200×630 and under 300 KB, or WhatsApp may skip it.
- If the domain changes (e.g. to alemu.xyz), update `canonical`, `og:url`, `og:image`, `og:image:secure_url` and `twitter:image`.

Preview locally: `npx serve .` (or just open `index.html`).

Made by the super gangster @manojpandey