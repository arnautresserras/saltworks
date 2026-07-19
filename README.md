# saltworks-site

Landing page for **SaltWorks**, hosted on GitHub Pages. Static HTML/CSS — no build step.

## Structure

```
index.html            # the page
style.css             # tokens mirrored from the game's saltworks_theme.tres
fonts/                # bundled IBM Plex (SIL OFL 1.1), same set the game ships
.github/workflows/    # deploy-pages.yml — publishes on push to main
```

## Local preview

Any static server works, e.g.:

```bash
python -m http.server 8000   # then open http://localhost:8000
```

## Publishing

1. Push to GitHub (`main`).
2. Repo **Settings → Pages → Source: GitHub Actions** (one-time).
3. Every push to `main` redeploys via `.github/workflows/deploy-pages.yml`.

## Download links

The download buttons in `index.html` point at the **latest release** of the game repo
(`arnautresserras/saltworks`), using stable asset names produced by that repo's
`release.yml` workflow:

- `SaltWorks-Windows.zip`
- `SaltWorks-macOS.zip`

If you rename the game repo or its release assets, update the hrefs in `index.html`.

## Screenshots

Drop a PNG in `assets/` and replace the `.shot` placeholder block in `index.html`.
