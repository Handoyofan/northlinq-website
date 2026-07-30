# NorthLinq Website

Static mirror of the published NorthLinq site (built and hosted on [Framer](https://framer.com)), originally live at https://northlinq.framer.website/.

Each page's rendered HTML was captured as-is, so images, fonts, styles, and the Framer runtime scripts continue to load from Framer's public CDN (`framerusercontent.com`). Serve any folder here with a static file server and it will render identically to the original.

## Structure

```
index.html                                  /
about/index.html                            /about
blog/index.html                             /blog
contact/index.html                          /contact
blog/<slug>/index.html                      /blog/<slug>  (4 posts)
```

## Local preview

```
python3 -m http.server 8000
```

Then open http://localhost:8000/.
