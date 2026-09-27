# What They'll Need to Know — landing page

A static, responsive sales page (`index.html` + `assets/`) for the *What They'll Need to Know*
guide ($9.99) and the Complete Family Bundle ($17.99). No build step.

## Before going live

1. **Checkout links:** paste your two Lemon Squeezy checkout URLs into the `CHECKOUT` block
   near the bottom of `index.html`. Full steps, file delivery, and testing are in
   [`CHECKOUT-SETUP.md`](CHECKOUT-SETUP.md).
2. **Waitlist (until checkout is live):** while a checkout link is missing, both price buttons say
   "Join the waitlist" and an email form appears under the prices. Connect it by pasting your email
   tool's form address into `WAITLIST.action` (Formspree, Kit, Mailchimp, Buttondown…).
   `WAITLIST.earlyBird` currently promises an early-bird launch discount: create a real discount
   code in Lemon Squeezy and email it to the waitlist, or clear the line.
3. **Trust lines (real facts only):** `GUARANTEE` is set to "30-day refund, no questions asked." and
   shows under the prices. Honor it (refunds are issued from the Lemon Squeezy dashboard) or change it.
   `STAT` (e.g. a true "Used by N families") shows near the top and the prices. Both hidden while empty.
   Testimonials and `CREATOR` also feed the short proof line near the top and the prices.
4. **Launch price (optional, off by default):** set `LAUNCH.endsAt` only to a real date you'll honor.
5. **Family photo:** save a properly licensed photo (adult child and parent at a table, landscape,
   about 1600 × 1200) as `assets/family-photo.jpg`. It appears automatically.
6. **Testimonials and "Why I Created This":** fill in `TESTIMONIALS` and `CREATOR` in the script
   at the bottom of `index.html`. Use real quotes only, with permission.
7. **Placeholders:** `SHOW_PLACEHOLDERS` is `false`, so visitors never see placeholder cards.
   Set it to `true` temporarily if you want to preview the empty photo/testimonial/creator slots.
8. **Horizontal label-pack image (desktop):** save it as `assets/label-pack-horizontal.jpg`
   and uncomment the `<source>` line in the bonus section. Phones keep `label-pack-vertical.jpg`.

## Files

- `index.html`: the landing page
- `LAUNCH-EMAILS.md`: three ready-to-edit emails for the waitlist (launch day, reminder, last day)
- `thank-you.html`: post-purchase page (no download links; delivery is handled by Lemon Squeezy)
- `assets/`: covers and single-page previews rendered from the PDFs. The full product PDFs
  are intentionally **not** in this repository.
- `What-Theyll-Need-to-Know-landing-page.pdf`: a PDF snapshot of the page for review

## Deploy

Upload `index.html`, `thank-you.html`, and `assets/` to any static host (Netlify,
Cloudflare Pages, Vercel, GitHub Pages).
