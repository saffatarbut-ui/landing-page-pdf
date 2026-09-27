# What They'll Need to Know — landing page

A static, responsive sales page (`index.html` + `assets/`) for the *What They'll Need to Know*
guide ($9.99) and the Complete Family Bundle ($17.99). No build step.

## Before going live

1. **Checkout links:** paste your two Lemon Squeezy checkout URLs into the `CHECKOUT` block
   near the bottom of `index.html`. Full steps, file delivery, and testing are in
   [`CHECKOUT-SETUP.md`](CHECKOUT-SETUP.md).
2. **Launch price (optional, off by default):** set `LAUNCH.endsAt` only to a real date you'll honor.
3. **Family photo:** save a properly licensed photo (adult child and parent at a table, landscape,
   about 1600 × 1200) as `assets/family-photo.jpg`. It appears automatically.
4. **Testimonials and "Why I Created This":** fill in `TESTIMONIALS` and `CREATOR` in the script
   at the bottom of `index.html`. Use real quotes only, with permission.
5. **Placeholders:** `SHOW_PLACEHOLDERS` is `false`, so visitors never see placeholder cards.
   Set it to `true` temporarily if you want to preview the empty photo/testimonial/creator slots.
6. **Horizontal label-pack image (desktop):** save it as `assets/label-pack-horizontal.jpg`
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
