# ADAA Health Care Trading — Website

A complete, responsive redesign of the existing Brawn Medical Company website for the ADAA Health Care Trading brand. Built as a dependency-free static site: no build step, no framework and no third-party JavaScript.

## Pages

| File | Purpose |
| --- | --- |
| `index.html` | Home — brand story, five portfolios, standards and process |
| `products.html` | Portfolio detail for all five categories |
| `about.html` | About, mission, vision, values and audiences |
| `contact.html` | Contact details, enquiry form, map and FAQs |
| `privacy.html` | Plain-language privacy note |
| `404.html` | Friendly not-found page for static hosts |

## Run locally

Open `index.html` directly, or serve the folder for a closer production check:

```powershell
python -m http.server 8080
```

Then visit `http://127.0.0.1:8080`.

## Deploy

Upload the contents of this folder to any static host (Netlify, Vercel, Cloudflare Pages, GitHub Pages, cPanel, S3). There is no server-side code or build process.

Before launch:

1. **Confirm the email address.** The site currently uses `info@adaahealthcare.com` as the new-brand address. If that mailbox is not live yet, replace it across the HTML files and in `assets/js/main.js`.
2. **Verify the phone and office address.** Both were carried over from the current Brawn Medical Company site: `+974 7737 1964` and Office No. 2/B, Ground Floor, Building No. 76, Street No. 362, Area 34, Doha, Qatar.
3. **Connect the enquiry form.** It currently validates and composes a structured email in the visitor's mail app. To capture leads centrally, replace the submit handler in `assets/js/main.js` with your CRM or form endpoint (for example Formspree, Basin or a serverless function).
4. **Set absolute URLs.** Update `og:image` and add a canonical URL once the production domain is confirmed. Social crawlers prefer absolute image URLs.
5. **Review regulatory copy.** Product descriptions are intentionally category-level and do not name specific medicines, devices or manufacturers. Add only claims and product names that your licences and registrations support.
6. **Social links.** No social icons are included because the only available accounts belonged to the previous Brawn brand. Add the new ADAA profiles when ready.

## Editing

- **Design tokens:** colours, typography, spacing and radii live at the top of `assets/css/styles.css` under `:root`.
- **Fonts:** self-hosted Bodoni Moda and Manrope in `assets/fonts/` (SIL Open Font License). No Google Fonts request at runtime.
- **Logo:** supplied source `assets/images/adaa-logo.jpg`; transparent lockups `adaa-mark.png/webp`, `adaa-wordmark.png` and `adaa-logo-full.png/webp` are derived from it. Favicons and the Open Graph image are included.
- **Photography:** category and editorial photography is sourced from the existing Brawn Medical Company media library and optimised to WebP.
- **Contact form:** markup in `contact.html`; behaviour in `assets/js/main.js` under "Enquiry form".

## Accessibility and performance

- Semantic landmarks, a single `h1` per page, skip link and visible focus styles.
- Keyboard-accessible mobile navigation with focus return and Escape support.
- Labelled form fields and a real `role="status"` submission message.
- `prefers-reduced-motion` support for all reveals, marquees and decorative motion.
- Self-hosted fonts, compressed WebP imagery, lazy loading below the fold and a lightweight vanilla JS file.
- No tracking scripts or marketing cookies are installed.

## Notes

This is a front-end rebuild, not a deployment. The live site remains unchanged until the files are published to the existing host.
