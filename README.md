# Datadog — Products by outcome (static site)

A self-contained two-page static website.

```
site/
├── index.html            # Products, grouped by outcome (home page)
├── business-value.html   # Business value calculator
├── README.md
└── assets/
    ├── colors_and_type.css
    └── datadog-icon.svg
```

## Run locally
Open `index.html` in a browser, or serve the folder:

```
cd site && python3 -m http.server 8000
# visit http://localhost:8000
```

## Publish
This is a plain static site — no build step. Upload the **contents of this
folder** to any static host and point the root at `index.html`:

- **Netlify** — drag the folder onto app.netlify.com/drop
- **Vercel** — `vercel deploy` from inside the folder
- **GitHub Pages** — commit the files, enable Pages on the branch
- **Cloudflare Pages / S3 + CloudFront** — upload as-is

The only external dependency is Google Fonts (loaded over HTTPS); everything
else is local.
