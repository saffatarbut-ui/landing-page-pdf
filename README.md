# What They'll Need to Know — landing page

A static, responsive sales page (`index.html` + `assets/`) for the *What They'll Need to Know*
guide ($12.99) and the Complete Family Bundle ($23.00). No build step.

## Before going live

1. **Checkout links:** paste your two Lemon Squeezy checkout URLs into the `CHECKOUT` block
   near the bottom of `index.html`. Full steps, file delivery, and testing are in
   [`CHECKOUT-SETUP.md`](CHECKOUT-SETUP.md).
2. **Pay buttons:** both price cards always show "Get the Guide — $12.99" and "Get the Complete
   Bundle — $23". Until the checkout links are set, clicking one shows "Checkout opens soon".
3. **Trust lines (real facts only):** `GUARANTEE` is empty, so no refund line is shown. If you ever
   adopt a refund policy, put its exact wording there and it appears under the prices.
4. **Launch price (optional, off by default):** set `LAUNCH.endsAt` only to a real date you'll honor.
5. **Testimonials and "Why I Created This":** add real quotes to `TESTIMONIALS` with a `placement` of
   `"hero"`, `"guide"` or `"bundle"` (one short quote near the top, one under each price card), and fill
   in `CREATOR`. Real quotes only, with permission. Empty slots stay hidden.
6. **Review mode:** `SHOW_PLACEHOLDERS = true` shows the three example quotes (`SAMPLE_TESTIMONIALS`),
   each labeled "Sample quote · replace before launch". Keep it `false` on the published page.
7. **Horizontal label-pack image (desktop):** save it as `assets/label-pack-horizontal.jpg`
   and uncomment the `<source>` line in the bonus section. Phones keep `label-pack-vertical.jpg`.

## Files

- `index.html`: the landing page
- `thank-you.html`: post-purchase page (no download links; delivery is handled by Lemon Squeezy)
- `assets/`: covers and single-page previews rendered from the PDFs. The full product PDFs
  are intentionally **not** in this repository.
- `What-Theyll-Need-to-Know-landing-page.pdf`: a PDF snapshot of the page for review

## Deploy

Upload `index.html`, `thank-you.html`, and `assets/` to any static host (Netlify,
Cloudflare Pages, Vercel, GitHub Pages).
