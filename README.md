# The Evangelist’s Complete Toolkit: sales page

A one-page, mobile-first sales page for **The Evangelist’s Complete Toolkit**.
It is plain HTML and CSS, with no JavaScript and no external libraries.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The whole page (text, styles and icons) |
| `images/` | Your posters, exported in AVIF, WebP and JPEG at several sizes, plus `share-image.jpg` for link previews |
| `fonts/montserrat-800.woff2` | Heading font (Montserrat ExtraBold, Latin characters only), with its licence `OFL.txt` |

## Put the page online

Upload `index.html`, the `images` folder and the `fonts` folder together, keeping the same structure, to any static web host.
Examples: Hostinger File Manager (`public_html`), Netlify (drag and drop), or GitHub Pages.

## What to edit in `index.html`

- **Testimonials:** search for `HOW TO ADD A TESTIMONIAL`. Replace the text in `[brackets]` with a real testimonial (with the person’s permission), then remove ` is-empty` from that slot’s class.
- **Price (optional):** search for `PRICE (optional)`. Write your price and delete the word `hidden`. If you leave it, the page tells visitors they will see the price on the checkout page.
- **Link previews on WhatsApp and Facebook:** after the page is online, replace `images/share-image.jpg` in the `og:image` line with the full address, for example `https://your-domain.com/images/share-image.jpg`.
- **Links:** the checkout link (`https://xzjdbavw.mychariow.co/prd_3tmqn68n/checkout`) and the WhatsApp link (`https://wa.me/243823226790?...`) each appear several times. Use search and replace if they change.

## Why it loads fast

- Images come in three sizes and three formats; each phone downloads only the one it needs (AVIF for most phones). The posters below the header load only when the visitor scrolls near them.
- On a slow 4G connection, the first screen needs about 80 KB in 3 requests.
- The heading font is preloaded and limited to Latin characters (12 KB). If it arrives late, the phone’s own bold font is used, so the text never jumps.

## Credits

- Heading font: [Montserrat](https://github.com/JulietaUla/Montserrat), SIL Open Font License 1.1 (`fonts/OFL.txt`)
- Icons: [Lucide](https://lucide.dev) (ISC licence) and the WhatsApp glyph from [Simple Icons](https://simpleicons.org) (CC0)
- Scripture: Matthew 9:37 from the World English Bible (public domain)
