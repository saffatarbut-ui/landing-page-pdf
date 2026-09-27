# Checkout & delivery setup (Lemon Squeezy)

The landing page never touches card details or product files. Lemon Squeezy handles
payment, receipts, and file delivery. The page only needs **two public checkout links**.

## 1. Create the two products

In your Lemon Squeezy dashboard, under **Store → Products → New product**:

| Product | Price | Files to upload (Files section of the product) |
|---|---|---|
| What They'll Need to Know | $12.99 USD, single payment | `What They'll Need to Know.pdf` |
| Complete Family Bundle | $23.00 USD, single payment | `What They'll Need to Know.pdf`, `Starting the Conversation.pdf`, `What Happens Next.pdf`, `Family Document Label Pack.pdf` |

- Upload the PDFs **only** to Lemon Squeezy. Don't put them in this repository or on your web host,
  where anyone with the URL could download them.
- Don't add the promotional cover image as a page of the label-pack PDF.

**Prices must match the page:** $12.99 for the guide and $23.00 for the bundle. Check both in
Lemon Squeezy before pasting the links; the page and `index.html`'s product data use these prices.

## 2. Confirmation and receipts

In each product's settings:

- **Confirmation modal / thank-you:** keep Lemon Squeezy's confirmation (it shows the download
  buttons). Optionally set the button link to your `thank-you.html` URL, e.g.
  `https://yourdomain.com/thank-you.html`. That page has no files, so opening it grants nothing.
- **Receipt email:** leave it on. It includes the download links for the files you uploaded.
  Under **Settings → Emails** you can add your logo and a support address.

## 3. Paste the links into the page

For each product: **Share → Checkout URL** (looks like
`https://yourstore.lemonsqueezy.com/buy/xxxxxxxx-xxxx-…`). Paste them into `index.html`
near the bottom, in the `CHECKOUT` block:

```js
var CHECKOUT = {
  guide:  "https://yourstore.lemonsqueezy.com/buy/…",   // $12.99
  bundle: "https://yourstore.lemonsqueezy.com/buy/…"    // $23.00
};
```

Until a link is filled in, its button reads "Checkout opens soon · Join the waitlist" and leads
to the separate waitlist form under the prices. Once both links are set, the buttons read
"Get the Guide — $12.99" and "Get the Complete Bundle — $23" and open checkout, and the
waitlist disappears. Also change "PreOrder" to "InStock" in the product data at the top of
`index.html` when you go live.

**Never paste an API key** into the page. Checkout links are public and safe; API keys are secret.

## How the checkout opens

- **Desktop (mouse/trackpad, 768px and wider):** the page loads Lemon Squeezy's official
  `lemon.js` and opens the checkout as an overlay on top of the page.
- **Phones and tablets:** the button goes to Lemon Squeezy's full-screen hosted checkout in the
  same tab. This is the most reliable option on mobile.
- If `lemon.js` fails to load, desktop buttons fall back to the hosted checkout.

The checkout shows the product name, final price, email field, payment options, and the
purchase button. All of that comes from Lemon Squeezy.

## 4. Test before going live

1. Turn on **Test mode** in Lemon Squeezy and use the test-mode checkout URLs in `CHECKOUT`.
2. Buy each product with test card `4242 4242 4242 4242` (any future date, any CVC).
3. Check that:
   - the guide order delivers **one** file, and the bundle order delivers **four**;
   - the receipt email arrives with working download links;
   - the checkout works on your phone as well as your computer.
4. Switch to live mode, replace both URLs with the **live** checkout URLs, and publish.

## Launch price (optional)

`LAUNCH.endsAt` in `index.html` shows "Launch price through …" on the $12.99 card and hides
itself after that moment. Use a real date and raise the price afterward, or set it to `""`.
