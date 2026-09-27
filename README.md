# What They'll Need to Know — landing page

A static, responsive sales page (`index.html` + `assets/`) for the *What They'll Need to Know*
guide ($9.99) and the Complete Family Bundle ($17.99). No build step.

## Before going live

1. **Checkout links:** paste your two Lemon Squeezy checkout URLs into the `CHECKOUT` block
   near the bottom of `index.html`. Full steps, file delivery, and testing are in
   [`CHECKOUT-SETUP.md`](CHECKOUT-SETUP.md).
2. **Launch price (optional):** set or clear `LAUNCH.endsAt` in the same script.
3. **Wide label-pack image (optional):** save the horizontal promo as
   `assets/label-pack-wide.webp` and uncomment the `<source>` line in the bonus section.

## Files

- `index.html`: the landing page
- `thank-you.html`: post-purchase page (no download links; delivery is handled by Lemon Squeezy)
- `assets/`: covers and single-page previews rendered from the PDFs. The full product PDFs
  are intentionally **not** in this repository.
- `What-Theyll-Need-to-Know-landing-page.pdf`: a PDF snapshot of the page for review

## Deploy

Upload `index.html`, `thank-you.html`, and `assets/` to any static host (Netlify,
Cloudflare Pages, Vercel, GitHub Pages).
