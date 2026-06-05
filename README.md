# Marble — Deploy to GitHub Pages (private repo)

## Setup

1. Create a **new private repository** on GitHub (any name)

2. Upload all files in this folder to the repository root
   - Use the GitHub web UI: **Add file → Upload files**
   - Or push via git if preferred

3. Go to **Settings → Pages**
   - Source: **Deploy from a branch**
   - Branch: **main** → **/ (root)**
   - Click **Save**

4. Wait ~60 seconds. Your game is live at:
   `https://username.github.io/reponame`

Source code stays private. Only the running game is public.
HTTPS is automatic — tilt controls work immediately on iOS and Android.

## Updating

Re-upload `index.html` (or push to main). GitHub Pages redeploys automatically.
To force the service worker to pick up changes, increment the cache version
in `sw.js`: `const CACHE = 'marble-v2'`
