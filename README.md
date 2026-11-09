# fuerte

**A thorned typeface that grows as you type.**

![fuerte preview](docs/preview.png)

fuerte (Thornscript) is an interactive 3D script typeface. Each letter is traced from a hand-drawn alphabet and rendered as a living rose stem: it grows stroke by stroke, sprouts thorns, blooms into roses that wither and shed their petals, and leaves the thorned letters behind.

> My typeface is inspired by rose thorns and my parents' experience of being immigrants. It reflects their hopes for a better life, the challenges of making a home in a new country, and the strength to hold on to their identity.
>
> The bright rose represents the life they imagined before immigrating. As it withers, it reveals the hardships they faced while starting over. The rose fades, but the thorned letters remain, representing their cultural roots, protection, and resilience.
>
> A rose's thorns are often removed to make it fit an ideal. By keeping the thorns in my letters, I reflect the pressure immigrants face to change themselves to be accepted. My typeface is a reminder that building a life in a new country should not mean giving up who you are.

## Try it

Open `index.html` in a browser, or visit the GitHub Pages site once it's enabled (see below).

- **Type** to grow your own word (Enter clears it)
- **Drag** to spin, **double-tap** to reset the view
- **Tap a letter** to regrow from that point
- **Poster** opens a square preview with colour palettes and export to **PNG, GIF, SVG or MP4**
- **Share link** copies a URL that grows your word for whoever opens it

### URL parameters

| Parameter | Effect |
|---|---|
| `?t=hello` | Opens with the given text |
| `?edit=1` | Opens the full editor (sliders, word fixer, spacing and stroke correction tools) instead of the show view |

## Project structure

```
index.html        page markup and script loading
css/style.css     all styles
js/glyphs.js      glyph data traced from the alphabet sheet (stems, thorns, dots)
js/main.js        3D renderer, growth shaders, layout engine and correction editor
js/show.js        show mode: touch reactions, roses, palettes, poster view and exports
docs/preview.png  screenshot used in this README
```

No build step and no dependencies to install. [three.js r128](https://threejs.org/) and its OrbitControls are loaded from a CDN.

## Run locally

Opening `index.html` directly works. For a local server instead:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Publish with GitHub Pages

1. Push this folder to a new GitHub repository.
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. The site will be live at `https://<your-username>.github.io/<repo-name>/` after a minute or two.

## Editor notes

Corrections made in the editor (`?edit=1`) are stored in the browser's `localStorage`. Use **Correct spacing & strokes → Export all** to save them as JSON, and **Import** to load them elsewhere.

## License

Code is released under the [MIT License](LICENSE).
