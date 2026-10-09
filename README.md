# quoterg.github.io

GitHub user site for [Iron Log](https://github.com/Quoterg/iron-log), which lives at
https://quoterg.github.io/iron-log/.

Why this repo exists: the Android app (a Trusted Web Activity) can only open without a browser bar
if the site proves it owns the app, with a file at the **root** of the origin:
`https://quoterg.github.io/.well-known/assetlinks.json`. A project page (`/iron-log/`) can't serve
the root, so this user site does — for free, without moving the app (which would leave users' data
behind, since browser storage is per origin).

- `.nojekyll` — so GitHub Pages serves the `.well-known` folder (Jekyll skips dot-folders).
- `index.html` — forwards to the app.
- `.well-known/assetlinks.json` — added once the Android app has a signing key (see
  `android/README.md` in the iron-log repo).
