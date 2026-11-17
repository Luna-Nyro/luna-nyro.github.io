# luna-nyro.github.io

Source of <https://luna-nyro.github.io>, a portfolio of Luna-Nyro's open-source projects:

| Group | Projects |
|---|---|
| Desktop & theming | [Glaze](https://github.com/Luna-Nyro/glaze), [Welcome](https://github.com/Luna-Nyro/welcome) |
| Apps | [Tandem](https://github.com/Luna-Nyro/tandem), [Gaffer](https://github.com/Luna-Nyro/gaffer) |
| MacBook Pro on Linux | [autolight](https://github.com/Luna-Nyro/autolight), [brcm43602-fix](https://github.com/Luna-Nyro/brcm43602-fix) |

## How it's built

Plain static HTML and CSS: no build step, no JavaScript, no external requests (no web fonts, CDNs,
trackers or analytics). GitHub Pages serves the files as they are; `.nojekyll` turns off Jekyll
processing.

```
index.html          the page
404.html            not-found page (uses root-relative paths)
assets/style.css    all styles
assets/favicon.svg  icon
```

The look follows [Glaze](https://github.com/Luna-Nyro/glaze): Material 3 tonal colours from the
`#5b8def` seed and frosted-glass surfaces (`backdrop-filter`, with an opaque fallback). Dark is the
default; light mode follows `prefers-color-scheme`. Motion is turned off for `prefers-reduced-motion`.
The font stack prefers Google Sans Flex / Roboto Flex when installed locally and otherwise uses
the system font.

## Preview locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Updating a project

Each project is one `<article class="card">` in `index.html`. Descriptions are taken from the
project's own README; keep them in step when a project changes.
