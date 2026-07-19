# Teresa Hu — Portfolio

Editorial-style personal portfolio for Teresa (Chao-Yuan) Hu. Plain HTML/CSS/JS — no build step, no dependencies.

## Structure

| File | What it is |
|---|---|
| `index.html` | All content: hero, projects, experience, education, content studio, about, skills, contact |
| `styles.css` | All styling. Colors and fonts are defined once in `:root` at the top |
| `script.js` | Small enhancements: scroll reveals, marquee loop, mobile menu |
| `assets/` | Images (photos, project screenshots, logos) |

## How to update content

Everything lives in `index.html` — open it and search for the text you want to change.

- **Add an experience**: copy an existing `<article class="xp">…</article>` block inside `#experience` and edit the dates, title, role, and text. Move the `<span class="now">● Currently here</span>` badge to whichever entry is current.
- **Add a project**: copy a `<article class="project">…</article>` block inside `#work`. Alternate the `flip` class so images keep alternating sides. Drop new screenshots in `assets/` and update the `<img src>` and Drive link.
- **Update stats** (followers, views, etc.): search for `studio-stats` and the hero `stats` block.
- **Swap photos**: replace files in `assets/` keeping the same filenames, or update the `src` attributes.
- **Change colors/fonts**: edit the CSS variables at the top of `styles.css`.

## Preview locally

```bash
cd teresa-portfolio
python3 -m http.server 8741
# open http://localhost:8741
```

## Deploy to GitHub Pages

1. Create a repo (e.g. `teresa-portfolio` — or `<username>.github.io` to get the root URL).
2. Push this folder to the `main` branch.
3. On GitHub: Settings → Pages → Source: "Deploy from a branch" → Branch: `main`, folder `/ (root)` → Save.
4. Your site goes live at `https://<username>.github.io/teresa-portfolio/` in a minute or two.

To update the live site afterwards: commit and push — Pages redeploys automatically.
