# Florence — portfolio landing page

A single-file, static landing page for Florence's neurotechnology work — neural
interfaces, assistive design, and cognitive augmentation. Cel-cyberpunk theme,
project archive with official logos, and click-to-play project videos.

Everything lives in **`index.html`** (fonts load from Google Fonts; logos are
embedded inline; videos load from YouTube on click). No build step, no
dependencies.

## Host it on GitHub Pages

1. Create a new GitHub repository (e.g. `florence-site`) and push this folder to it
   (see "Push to GitHub" below).
2. In the repo: **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Set **Branch: `main`** and **Folder: `/ (root)`**, then **Save**.
5. Wait ~1 minute. Your site goes live at:
   `https://<your-username>.github.io/<repo-name>/`

The videos play inline once the page is served over `https://` (GitHub Pages).
On a local `file://` preview they open on YouTube instead — that's expected.

## Push to GitHub

From inside this folder:

```bash
git init
git add -A
git commit -m "Florence portfolio landing page"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

Then enable Pages as described above.

## Customize

- **Text / blurbs / links:** edit the matching `<article class="card">` block in `index.html`.
- **Logos:** each is a `data:` URI inside a `<span class="logo">`. Replace the `src`
  with your own image (or another `data:` URI).
- **Videos:** change the `data-vid` / `href` on each `<a class="playlink">` to a new
  YouTube video ID.
- **Colors:** tweak the CSS variables at the top of the `<style>` block
  (`--cyan`, `--mag`, `--yel`, ...).

## Contact

bebtechsolutions@gmail.com
