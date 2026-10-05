# TickTockFocus website

Source of [ticktockfocus.com](https://ticktockfocus.com): the landing page and privacy policy for the [TickTockFocus](https://chromewebstore.google.com/detail/nealkefeifpkmkbfcfbkffdgnlohjbae) Chrome extension. The extension itself lives in [mist941/tick-tock-focus](https://github.com/mist941/tick-tock-focus).

## Files

| Path | Purpose |
| --- | --- |
| `index.html` | Landing page |
| `privacy.html` | Privacy policy (linked from the Chrome Web Store listing, so keep this URL) |
| `404.html` | Not-found page, served by GitHub Pages |
| `assets/styles.css` | Shared styles: design tokens, light and dark themes, all components |
| `assets/icon-*.png` | Site icon, copied from the extension |
| `CNAME`, `.nojekyll` | GitHub Pages configuration |

## Run locally

```bash
python -m http.server
```

Then open http://localhost:8000. The local server doesn't use `404.html` for missing pages; GitHub Pages does.

## Rules

- No build step, no frameworks, no JavaScript.
- No external requests: no web fonts, CDNs, analytics or embeds. The privacy policy promises this.
- Describe only what the current extension release does. Check claims against the extension source before changing copy.
- The header and footer are repeated in every page; change them everywhere.
- To change the icon, replace the files in `assets/` and keep their names.

## Deployment

GitHub Pages serves the `main` branch from the repository root at https://ticktockfocus.com.

## License

[Apache 2.0](LICENSE)
