# Picasso Boutique Travel — Astro Site

The Picasso Boutique Travel marketing site, rebuilt with [Astro](https://astro.build) from the original static HTML/CSS/JS.

## Project structure

```
/
├── public/               # static assets served as-is
│   ├── favicon.ico / .svg
│   ├── robots.txt
│   ├── sitemap.xml
│   ├── script.js         # mobile nav toggle + footer year
│   └── styles.css        # original site styles
├── src/
│   ├── layouts/
│   │   └── Layout.astro  # shared <head>, meta tags, global script
│   └── pages/
│       └── index.astro   # homepage (hero, journeys, destinations, enquiry form, footer)
├── astro.config.mjs
└── package.json
```

## Commands

Run from the project root in a terminal:

| Command             | Action                                       |
| :------------------- | :-------------------------------------------- |
| `npm install`         | Install dependencies                          |
| `npm run dev`         | Start local dev server at `localhost:4321`    |
| `npm run build`       | Build the production site to `./dist/`        |
| `npm run preview`     | Preview the production build locally          |

## Deployment

A GitHub Actions workflow (`.github/workflows/deploy.yml`) is included to build and deploy
the site to **GitHub Pages** automatically on every push to `main`. To enable it:

1. Push this repo to GitHub.
2. In the repo, go to **Settings → Pages** and set the source to **GitHub Actions**.
3. If using the custom domain `picassoboutiquetravel.com`, add a `public/CNAME` file
   containing the domain, and configure DNS with your registrar per
   [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

The site can also be deployed to any static host (Netlify, Vercel, Cloudflare Pages, etc.)
by running `npm run build` and serving the resulting `dist/` folder.

## Before launch

Carried over from the original site notes:

1. Replace `hello@picassoboutiquetravel.com` if a different enquiry email is preferred.
2. Connect the enquiry form to a form service/CRM for reliable submissions (it currently
   uses a `mailto:` fallback).
3. Add ABN, business address/phone, privacy policy, terms, and any required
   travel-industry/accreditation disclosures once confirmed.
4. Replace stock photography (currently Unsplash) with licensed brand photography if desired.
5. Ensure HTTPS/SSL is enabled at the hosting provider.
