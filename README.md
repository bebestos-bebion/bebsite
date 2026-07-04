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

## If the GitHub Pages deploy fails

The site is a plain static file, so failures are almost always a Pages *setting*,
not the HTML. Two reliable fixes:

**Option A — deploy via GitHub Actions (recommended).**
This repo includes `.github/workflows/deploy.yml`, which uploads the files
directly (no Jekyll). To use it:

1. Push this repo (including the `.github` folder).
2. Repo → **Settings → Pages → Build and deployment → Source: "GitHub Actions"**.
3. The "Deploy static site to Pages" workflow runs on every push to `main`.
   Watch it under the repo's **Actions** tab.

**Option B — deploy from a branch.**
Settings → Pages → Source: **Deploy from a branch** → **main / root**.
The `.nojekyll` file (already included) tells Pages to skip the Jekyll build.

**Common gotchas**
- The repo must be **public** (or you need GitHub Pro for private Pages).
- `index.html` must be at the **root** of the branch/folder you deploy — not
  inside a subfolder.
- If you first pushed with an auto-generated README, do a `git pull --rebase`
  (or force-push) so histories aren't out of sync.
