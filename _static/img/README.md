# Twiga brand assets

The mark is a giraffe whose neck is the forecast interval: the solid neck is the median, and the two
tints widening from the head into the shoulders are the nested prediction intervals. The wordmark is
Poppins SemiBold and the tagline is Inter, the fonts of the documentation site; all text is converted to
outlines, so every file is self-contained and needs no font.

## Files

| File | Use |
|---|---|
| `twiga-logo-compact-light.svg`, `twiga-logo-compact.svg` | Navbar, hero and app headers: the mark and wordmark for a light or a dark background |
| `twiga-logo-light.svg`, `twiga-logo.svg` | Posters, slides, social cards: adds the tagline, so use it at 96 px tall or more |
| `twiga-mark-light.svg`, `twiga-mark.svg` | Avatars and square slots: the badge alone |
| `twiga-icon.svg` | Favicon and app icon: head and neck only on a charcoal disc, readable at 16 px on any tab |
| `twiga-mono-ink.svg`, `twiga-mono-white.svg` | One-colour print, stamps and embossing: the interval is drawn as two outlines instead of tints |

`twiga-logo.svg` and `twiga-logo-compact.svg` are the dark-background versions; the `-light` files are for
light backgrounds.

## Regenerate

`scripts/branding/make_logos.py` draws every file in this folder. Give it a directory holding
`Poppins-SemiBold.ttf` and `Inter-Regular.otf` (both SIL Open Font License) and run:

```bash
uv run python scripts/branding/make_logos.py --fonts ~/fonts --out docs_sphinx/_static/img
```

The badges and the favicon need no font, and a test checks that they match the files committed here.
The README logo is the badge served by the documentation site, `twiga-mark-light.svg`, so it works on
PyPI and in the private repository alike; it appears once the docs have deployed.

## Colour

The colours are the tokens of `docs_sphinx/_static/css/twiga.css`.

| Role | Light background | Dark background |
|---|---|---|
| Giraffe | `#0F718E` | `#00BFA5` |
| Wordmark | `#263238` | `#F5FAF9` |
| Tagline | `#455A64` | `#8AABB4` |
| Badge disc | `#FFFFFF` | `#1E2D32` |

Every pair has a contrast of at least 5.5:1 (giraffe 5.6 and 6.1, wordmark 13, tagline 7.2 and 5.8).

## Use

- **Clear space:** keep one quarter of the badge height free on every side.
- **Minimum size:** compact lockup 24 px tall, badge 20 px, favicon 16 px, full lockup with tagline 96 px.
- **Do not** recolour the giraffe, stretch the logo, place the light-background version on a dark
  surface (or the reverse), add effects, or redraw the wordmark in another font.
