# Mass Arena

Agar.io × Diep.io arena game. Eat orbs, shoot, evolve, fuse classes, fight bosses. Single-page HTML5 game, installable as a PWA, no build step.

## Publish on GitHub Pages

1. Create a new **public** repository on GitHub (e.g. `mass-arena`).
2. Upload every file in this folder (keep the `icons/` folder), or push with git:
   ```
   git init && git add . && git commit -m "Mass Arena"
   git branch -M main
   git remote add origin https://github.com/<you>/mass-arena.git
   git push -u origin main
   ```
3. In the repo go to **Settings → Pages**, set **Source: Deploy from a branch**, branch **main**, folder **/ (root)**, and Save.
4. After a minute the game is live at `https://<you>.github.io/mass-arena/`.

## Updating
Replace `index.html` and commit. The service worker is network-first, so players get the new version on their next load.

## Run locally
```
python3 -m http.server 8000
```
Then open http://localhost:8000 (the service worker needs http, not file://).

## Notes
- Progress is saved in each browser's localStorage, per site address.
- On phones, use "Add to Home Screen" for fullscreen play.
