# NPM Site Analytics — Vercel deploy

A self-contained, password-protected snapshot of the dashboard, styled to match the reference report at media-tracker-two.vercel.app (itself based on northpointministries.org/update's branding): navy #0d1940 hero, cyan #22f0ff accents, light-gray cards, Rubik typeface, tighter spacing.

## Deploy to Vercel

**Easiest — drag and drop:**
1. Go to https://vercel.com/new
2. Drag the `npm-site-analytics` folder (just `index.html`) onto the page
3. Deploy — no build step needed, it's a single static file

**Or with the CLI**, from inside this folder:
```
npx vercel deploy --prod
```

## Password

The page is gated with the password `redeploy27`, checked in the browser.

**Important:** this is a basic deterrent, not real security — the password lives in the page's own JavaScript, so anyone who views the page source can read it and bypass the gate. It will stop casual visitors but not someone who goes looking. If you need actual access control, Vercel's own Password Protection feature (under Project Settings → Deployment Protection, available on Pro/Enterprise plans) enforces it server-side and is the real version of what you asked for.

## Refreshing the data

This is a static snapshot of the data as of the exports processed through 2026-10-25 (GA4 pages/channels/devices/geo across all four pages, Vimeo video stats through Oct 22). It is not connected to GA4 and won't update on its own. When you have a new export, send it back in the chat and ask for an updated file — I'll rebuild `index.html` with the new numbers.

The live, continuously-editable version of this same dashboard (where I can update data without re-exporting a file each time) is the Claude dashboard artifact from this conversation.
