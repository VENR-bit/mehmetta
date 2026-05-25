# MehMetta

Static landing page for **MehMetta** — a non-profit offering simple meditation
and relaxation exercises for refugees, free and without registration.

Inspired by [mehmetta.ch](https://mehmetta.ch). Single HTML file, no build step.

## Pages

- `index.html` — main site with calligraphic logo, multilingual hero
  (Deutsch, Arabisch, Paschtu, Türkisch, Tigrinya, Somali, Tibetisch),
  newsletter sign-up, language pill row, About, Contact, Thank-You and a
  Downloads placeholder. Includes a blurred twilight-desert background.
- `v1-simple.html` — minimal alternate layout (button stack, no hero
  paragraphs).

Internal navigation uses hash anchors (`#about`, `#contact`,
`#contact-done`, `#deutsch`, etc.) handled by inline JavaScript.

## Assets

```
assets/
├── mehmetta-logo.png   — transparent white calligraphic mark
└── desert-bg.jpg       — generated twilight desert (blurred at runtime)
```

Fonts are loaded from Google Fonts:
**Source Sans 3**, **Noto Sans Arabic**, **Noto Sans Ethiopic**,
**Noto Serif Tibetan**.

## Run locally

It's plain HTML — open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# → http://localhost:8000
```

## Deploy

### GitHub Pages

1. Push this folder to a repository (e.g. `mehmetta`).
2. **Settings → Pages → Source: Deploy from a branch → `main` / `(root)`**.
3. Your site will be live at `https://<user>.github.io/<repo>/`.

### Netlify / Vercel / Cloudflare Pages

Drag-and-drop the folder, or connect the repo. No build command, no output
directory — it's already static.

### Custom domain

Add a `CNAME` file in the project root containing the domain (e.g.
`mehmetta.example.org`) and configure DNS to point at the host's servers.

## Customising

- **Background photo** — swap `assets/desert-bg.jpg` with your own
  (≈1600×1000, JPEG/PNG). The CSS applies blur + tint automatically.
- **Logo** — replace `assets/mehmetta-logo.png` (white on transparent).
- **Copy / languages** — edit the corresponding sections directly inside
  `index.html`. All text lives in plain HTML, no framework.
- **Audio files** — drop MP3s into `assets/audio/` and link them from the
  `#deutsch` (and sibling) sections; replace the placeholder tiles.

## License

MIT — see `LICENSE`.
