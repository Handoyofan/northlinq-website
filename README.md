# NorthLinq Website

**🔗 Live site: https://handoyofan.github.io/northlinq-website/**

| Page | Link |
|---|---|
| Home | https://handoyofan.github.io/northlinq-website/ |
| About | https://handoyofan.github.io/northlinq-website/about |
| Blog | https://handoyofan.github.io/northlinq-website/blog |
| Contact | https://handoyofan.github.io/northlinq-website/contact |

Static, fully self-hosted copy of the NorthLinq site, originally built and published on [Framer](https://framer.com) at https://northlinq.framer.website/.

Every page's rendered HTML was captured as-is. All images, fonts, and the Framer runtime JS/CSS have been downloaded into `_framer/` and every reference rewritten to point locally — the site has **zero runtime dependency on Framer's servers** and will keep working after the Framer account is cancelled. Any content edits now happen by hand-editing the HTML directly (there's no visual editor anymore).

## Structure

```
index.html                                  /
about/index.html                            /about
blog/index.html                             /blog
contact/index.html                          /contact
blog/<slug>/index.html                      /blog/<slug>  (4 posts)
_framer/                                    vendored images, fonts, and JS/CSS runtime
```

## Local preview

A plain file server is required — opening `index.html` via `file://` will not work,
because the pages load JavaScript modules.

```
python3 -m http.server 8000
```

Then open http://localhost:8000/.

## Hosting

The site is published automatically by GitHub Pages from the `main` branch root.
Pushing to `main` redeploys it.

It can equally be hosted anywhere that serves static files (Hostinger, Netlify, S3, …) —
upload the repository contents so `index.html` sits at the web root. No database, PHP, or
build step is required.

A version of this site reorganised into a conventional `css/ js/ images/ fonts/` folder
structure is kept separately as `northlinq-export` (see the export zip), which is the more
convenient starting point for a manual upload to shared hosting.
