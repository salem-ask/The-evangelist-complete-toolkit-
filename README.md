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

## Put the page online

The page is set up for **https://evangelist-toolkit.bookline.digital** (Hostinger).

1. In Hostinger hPanel, create the subdomain `evangelist-toolkit` for `bookline.digital`. Hostinger creates a folder for it (by default `public_html/evangelist-toolkit`).
2. Open File Manager, go into that folder and upload `index.html`, `.htaccess`, and the `images` and `fonts` folders, keeping the same structure. You can also upload them as one zip file and use **Extract**.
3. Check that SSL is active for the subdomain, then turn on **Force HTTPS**.

`.htaccess` gives the images and the font the right file types, compresses the page and lets phones keep images for 30 days. It only works on Apache/LiteSpeed servers such as Hostinger; on any other static host, upload the same files.

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
