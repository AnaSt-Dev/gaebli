# Gäbli — Landing Page

Static HTML/CSS recreation of the Gäbli landing page, rebuilt to move off Framer.

## Structure
- `index.html` — page markup and content
- `style.css` — all styling (no build step, no dependencies)

Images are currently linked directly from Framer's asset CDN (`framerusercontent.com`). Since those URLs are stable but not under your control, consider downloading them into an `/assets` folder in this repo and updating the `src` attributes before you fully retire Framer.

## Run locally
Just open `index.html` in a browser, or serve it:
```bash
npx serve .
```

## Deploy on GitHub Pages
1. Push this folder to a GitHub repo.
2. In the repo, go to **Settings → Pages**.
3. Set the source to the `main` branch, root folder.
4. Your site will be live at `https://<username>.github.io/<repo>/`.

## Custom domain (gaebli.ch)
If you want to keep using `www.gaebli.ch`, add a `CNAME` file containing just the domain, and point your DNS `A`/`CNAME` records to GitHub Pages per [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Note on fidelity
This was rebuilt from the live page's content plus reference screenshots (not Framer's compiled source, which isn't portable/extractable). Colors, the Inter typeface, the lavender/navy palette, and the bento-grid card layout are matched from the screenshots. Two things worth double-checking against the real site:
- The logo uses "Caveat" (a free Google Font) as a stand-in for the actual script wordmark — if you have the real logo as an SVG/PNG, swap it in for exact fidelity.
- The image-to-section pairing was inferred from the screenshots' visual layout, not Framer's internal DOM order, so double check each photo is attached to the section you want.
