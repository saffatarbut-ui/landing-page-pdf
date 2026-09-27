# What They'll Need to Know — landing page

A single-file sales page (`index.html` + `assets/`) for the *What They'll Need to Know* guide ($9.99) and the Complete Family Bundle ($17.99).

## Connect checkout

Open `index.html`, scroll to the `<script>` at the bottom, and paste your payment links:

```js
var CHECKOUT = {
  guide: "https://…",   // $9.99  — What They'll Need to Know
  bundle: "https://…"   // $17.99 — Complete Family Bundle
};
```

Every "Buy" button uses these links. Until they're set, the buttons scroll to the pricing section and show a short "checkout isn't connected yet" note.

## Deploy

It's static HTML with no build step. Upload `index.html` and the `assets/` folder to any static host (GitHub Pages, Netlify, Cloudflare Pages, Vercel).

## Images

`assets/*.jpg` are page previews rendered from the four product PDFs.
