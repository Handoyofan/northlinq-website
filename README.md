# NorthLinq Website

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

```
python3 -m http.server 8000
```

Then open http://localhost:8000/.
