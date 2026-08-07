# NorthLinq Website

**🔗 Live site: https://handoyofan.github.io/northlinq-website/**

| Page | Link |
|---|---|
| Home | https://handoyofan.github.io/northlinq-website/ |
| About | https://handoyofan.github.io/northlinq-website/about |
| Blog | https://handoyofan.github.io/northlinq-website/blog |
| Contact | https://handoyofan.github.io/northlinq-website/contact |

Complete, self-contained copy of the NorthLinq website, organised into a conventional
static-site folder structure. Originally built on Framer and published at
https://northlinq.framer.website/

**No external dependencies.** Every image, font, stylesheet and script is stored in this
repository. Nothing loads from Framer's servers, so the site keeps working after the
Framer subscription is cancelled.

## Folder structure

```
index.html                  Home            →  /
about/index.html            About           →  /about
blog/index.html             Blog listing    →  /blog
contact/index.html          Contact         →  /contact
blog/<slug>/index.html      4 blog posts    →  /blog/<slug>

css/                        One stylesheet per page (extracted from the HTML)
js/                         Page scripts and the Framer runtime (ES modules)
js/data/                    Blog/CMS content data files
images/                     PNG / JPG / SVG images
fonts/                      WOFF2 webfonts

robots.txt, sitemap.xml     SEO files
```

## Local preview

A plain file server is required — opening `index.html` directly with `file://` will not
work, because the pages load JavaScript modules.

```
python3 -m http.server 8000
```

Then open http://localhost:8000/

## Hosting

**GitHub Pages** publishes this repository automatically from the `main` branch root.
Pushing to `main` redeploys the live site.

**Hostinger / any static host:** upload the *contents* of this repository into
`public_html` so that `index.html` sits at the top level (not inside a subfolder). No
database, PHP, or build step is needed — the cheapest shared-hosting plan is sufficient.

The `.nojekyll` file tells GitHub Pages to serve the files as-is rather than running them
through Jekyll. Keep it.

## Editing

There is no visual editor anymore; content is changed by editing the HTML files directly.
Page text lives in the `index.html` files, styling in `css/`.
