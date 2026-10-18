# The Evangelist’s Complete Toolkit: sales page

A one-page, mobile-first sales page for **The Evangelist’s Complete Toolkit**.
It is plain HTML and CSS, with no JavaScript and no external libraries.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The whole page (text, styles and icons) |
| `images/` | Your posters, exported in AVIF, WebP and JPEG at several sizes, plus `share-image.jpg` for link previews |
| `fonts/montserrat-800.woff2` | Heading font (Montserrat ExtraBold, Latin characters only), with its licence `OFL.txt` |
| `.htaccess` | Hostinger server settings: file types, compression and caching |
| `deploy/evangelist-toolkit-site.zip` | The site files above in one zip, used to deploy on Hostinger |

## Where the page is online

**https://evangelist-toolkit.bookline.digital**, on Hostinger (account `u977986808`):

- It is its own website on the hosting plan, separate from the Node.js app on `bookline.digital`, so the two cannot interfere.
- DNS: an `A` record `evangelist-toolkit` → `92.113.24.54` in the `bookline.digital` zone.
- SSL is active, and visitors are redirected to HTTPS.

`.htaccess` gives the images and the font the right file types, compresses the page, lets phones keep images for 30 days and hides Git files and this README. It only works on Apache/LiteSpeed servers such as Hostinger.

## Update the live page

1. Edit the files, then rebuild `deploy/evangelist-toolkit-site.zip` with `index.html`, `.htaccess`, `images/` and `fonts/` at the root of the zip, and push.
2. In Hostinger, pull this repository into a temporary `_deploy` folder of the website (Git deployment).
3. Deploy `_deploy/deploy/evangelist-toolkit-site.zip` as a static site archive. This replaces the website's files with the zip's contents and removes `_deploy`.

By hand, you can instead upload the zip into the website's `public_html` with File Manager and use **Extract**, replacing the old files.

## What to edit in `index.html`

- **Price (optional):** search for `PRICE (optional)`. Write your price and delete the word `hidden`. If you leave it, the page tells visitors they will see the price on the checkout page.
- **Page address:** if the page moves to another address, update `og:url`, `og:image` and the `canonical` link at the top of the file, so link previews on WhatsApp and Facebook keep working.
- **Links:** the checkout link (`https://xzjdbavw.mychariow.co/prd_3tmqn68n/checkout`) appears several times, and the WhatsApp link (`https://wa.me/243823226790?...`) appears in the FAQ and the footer. Use search and replace if they change. The footer also links to the Bookline website (`https://bookline.digital`).

## Why it loads fast

- Images come in three sizes and three formats; each phone downloads only the one it needs (AVIF for most phones). The posters below the header load only when the visitor scrolls near them.
- On a slow 4G connection, the first screen needs about 80 KB in 3 requests.
- The heading font is preloaded and limited to Latin characters (12 KB). If it arrives late, the phone’s own bold font is used, so the text never jumps.

## Credits

- Heading font: [Montserrat](https://github.com/JulietaUla/Montserrat), SIL Open Font License 1.1 (`fonts/OFL.txt`)
- Icons: [Lucide](https://lucide.dev) (ISC licence)
- Scripture: Matthew 9:37 from the World English Bible (public domain)
