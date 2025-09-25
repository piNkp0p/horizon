
# Telegram Slot Machine (GitHub Pages ready)

This is a single-file HTML build of your canvas slot machine. It’s optimized for mobile WebViews (Telegram) and full Chrome, with lava/cosmic effects preserved but throttled for performance.

## Deploy to GitHub Pages

1. **Create a new repo** on GitHub (public is fine), e.g. `telegram-slot`.
2. **Upload these files** (or commit/push):
   - `index.html`
   - `.nojekyll`
   - `README.md`
3. In the repo, go to **Settings → Pages**:
   - **Build and deployment** → Source: **Deploy from a branch**
   - Branch: `main` (or `master`) → `/root`
4. Your site will publish to a URL like:
   `https://<your-username>.github.io/<repo-name>/`

## Use as a Telegram Web App

1. Host URL is the GitHub Pages link above (HTTPS).
2. Go to **@BotFather** in Telegram:
   - `/mybots` → select your bot → **Bot Settings** → **Menu Button** → **Configure`**
   - Paste your URL and save.
3. Open your bot and press the Web App button.

## Notes

- The game caps device pixel ratio for performance and uses cached offscreens for lava.
- To adjust spin feel: edit `spinBaseDuration`, `cyclesBase` in `CONFIG`.
- To tune background/lava budgets: lower `cosmicBG.resolution`, `maxFPS`, or reduce ring thickness last arg in `drawLavaFrameCached(...)` call.
