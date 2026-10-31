# SHREYA'S JEE GRAND PRIX

A mobile-first, multi-screen JEE challenge PWA. Includes intro, garage, 30-checkpoint map, per-day mission screens, championship, trophy garage and player profile.

## Run locally
Serve this directory over HTTP (service workers and PWA installation require localhost or HTTPS):
```bash
python -m http.server 8000
```
Open http://localhost:8000.

## Deploy publicly (HTTPS required)
1. Create a new repository on GitHub.
2. Upload the contents of this folder to the repository root.
3. In GitHub, open **Settings → Pages**.
4. Choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
5. Wait for the Pages deployment. Open the generated `https://<username>.github.io/<repository>/` URL.
6. Visit the URL in Android Chrome. Tap **Install App** if offered, or Chrome ⋮ → **Install app** / **Add to Home screen**.

You can also deploy the folder to Netlify, Cloudflare Pages, or another static HTTPS host.

## Persistence and offline
Question counters, claimed level victories, XP, streak, and mock completions are saved in IndexedDB, with localStorage fallback. The service worker precaches the app shell on first successful visit. Google Fonts are an optional online enhancement; system fallbacks are included.

## Game rules
- 30 levels × 3 subjects × 50 questions = 4,500 questions.
- Levels unlock sequentially. A level victory can only be claimed at 150/150.
- Each claimed level awards 500 XP.
- Two manually checked mock tests award 250 XP each.
- Day 30 is marked as the Final Grand Prix Boss.
- Reset is behind a confirmation dialog.

## Important limitations
This source package is ready for HTTPS static hosting, but it has not been published to a public host from this environment. A public URL requires access to a hosting account or a repository where it can be deployed. Browser/device installation and offline behavior should be verified on the chosen host after deployment.
