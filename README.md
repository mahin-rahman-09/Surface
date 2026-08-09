# Surface

A quit-smoking tracker: live smoke-free streak, money saved, cigarettes avoided,
a real health-recovery timeline, and a breathing tool for cravings. Installable
as an app on your phone or desktop, works offline.

## Push it to GitHub

From inside this folder:

```bash
git init
git add .
git commit -m "Surface: quit smoking tracker"
git branch -M main
git remote add origin https://github.com/<your-username>/surface.git
git push -u origin main
```

(Create the empty `surface` repo on GitHub first, or swap in whatever name you like —
just update the remote URL to match.)

## Turn on GitHub Pages

1. On GitHub, go to your repo → **Settings** → **Pages**.
2. Under "Build and deployment", set **Source** to "Deploy from a branch".
3. Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
4. Wait a minute or two — your app will be live at:
   `https://<your-username>.github.io/surface/`

## Install it on your phone

- **Android (Chrome):** open the link above → menu (⋮) → "Add to Home screen".
- **iPhone (Safari):** open the link above → Share button → "Add to Home Screen".

Once installed, it opens full-screen like a native app and keeps working without
a connection, since the service worker caches the app shell.

## A few things worth knowing

- **Your data stays on your device.** Streak, savings settings, and craving log
  are stored in the browser's local storage — nothing is sent anywhere, and
  there's no login. That also means the data won't sync between your phone and
  laptop unless you enter your quit date on both.
- **Clearing your browser's site data will erase your log.** If you want real
  backup/sync across devices later, that would mean adding a small backend —
  happy to help with that if it becomes worth it to you.
- **Updating the app:** any time you push changes to `main`, GitHub Pages
  redeploys automatically within a minute or two. Returning visitors get the
  update the next time the service worker checks for a new version (usually
  on their next open).

## File structure

```
index.html        the app
manifest.json      installability metadata (name, icons, colors)
sw.js               service worker for offline caching
icons/              app icons (192, 512, and iOS touch icon)
```
