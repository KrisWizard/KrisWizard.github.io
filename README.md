# Krister Prestøy: Portfolio

A static, single-page portfolio. Plain HTML/CSS with a few lines of JS and no build step.

```
index.html     page content
styles.css     all styling
script.js      mobile nav toggle + footer year
img/           project thumbnails (from ArtStation)
preview-*.png  local screenshots (you can delete these before publishing)
```

## Preview locally

```bash
cd portfolio
python3 -m http.server 8000
# open http://localhost:8000
```

## Publish to GitHub Pages

1. Create a new public repo on GitHub, for example `KrisWizard.github.io` (that gives you the URL `https://kriswizard.github.io`). Any other repo name works too and gets published at `https://kriswizard.github.io/<repo>/`.
2. Push the contents of this folder to the repo's root:
   ```bash
   cd portfolio
   git init && git add . && git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/KrisWizard/<repo>.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages → Build and deployment**, set **Source: Deploy from a branch**, pick **Branch: `main` / `(root)`**, and save.
4. Wait a minute or so, then open the URL GitHub shows. Every push to `main` redeploys the site.
5. Optional: to use a custom domain, add it under Settings → Pages and create the DNS records GitHub lists.

All asset paths are relative, so the site works at a user-site root and in a project sub-path.

## TODO

- [ ] **CV PDF**: add e.g. `cv/Krister-Prestoy-CV.pdf` and point the hero `CV` button (`href="#"`, `data-todo="cv"`) at it.
- [ ] **3D renders**: add Claptrap, Werewolf and Metal Gear REX renders to `img/` and replace the `.placeholder` divs in the 3D art section with `<img>` tags (include `width`/`height`, `loading="lazy"` and alt text).
- [ ] **Playable build link**: add a link to a playable Winds of Valor build (itch.io or similar) in the Featured section.
- [ ] Optional: point the project cards at dedicated pages or videos if you want them to go somewhere other than ArtStation.
- [ ] Optional: add an `og:image` (1200×630) for nicer link previews.
