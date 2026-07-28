# KS Games website — publish to GitHub Pages

This folder is a ready-to-publish static site. It has no build step — GitHub
Pages serves these files directly.

## 1. Create the repo
1. Go to https://github.com/new
2. Repository name: **ksgames.github.io** (must match your GitHub username exactly,
   with `.github.io` at the end — that's what gives you the free
   `https://ksgames.github.io` domain instead of a `/repo-name` subpath).
3. Set it to **Public**. Don't add a README/gitignore (this folder already has one).
4. Click **Create repository**.

## 2. Upload these files
Easiest path (no git needed): on your new repo's page, click
**"uploading an existing file"**, drag in every file and the `articles/`
folder from this project, and commit directly to `main`.

Or, if you have git installed locally:
```bash
cd path/to/this/folder
git init
git add .
git commit -m "Launch KS Games site"
git branch -M main
git remote add origin https://github.com/ksgames/ksgames.github.io.git
git push -u origin main
```
(Replace `ksgames` in the URL with your actual GitHub username if it's different.)

## 3. Turn on Pages
1. In the repo, go to **Settings → Pages**.
2. Under "Build and deployment", Source: **Deploy from a branch**.
3. Branch: **main**, folder: **/ (root)**. Save.
4. Wait 1–2 minutes, then visit `https://ksgames.github.io` (or wherever
   GitHub shows the Pages URL — it can differ from your username if the repo
   name doesn't match it exactly).

## 4. Get it into Google
1. Go to https://search.google.com/search-console
2. Add the property `https://ksgames.github.io/` (URL prefix).
3. Verify ownership (the HTML-file or meta-tag method both work with GitHub Pages).
4. Once verified, open **Sitemaps** in the left menu and submit:
   `https://ksgames.github.io/sitemap.xml`
5. Use **URL Inspection** on your homepage and click "Request indexing" to
   speed up the first crawl.

Indexing itself isn't instant — expect anywhere from a few days to a couple
weeks for Google to crawl and start showing pages, especially on a brand new
domain with no existing backlinks.

## 5. What's in here
- `index.html` — homepage, showcases all three products + links to WIGD?!
- `articles/index.html` — blog index
- `articles/*.html` — three SEO articles, one per product, each linking to
  the matching Gumroad listing
- `style.css` — shared styling
- `robots.txt`, `sitemap.xml` — SEO plumbing

## 6. Easy next steps
- Swap `ksgames` in the sitemap/canonical URLs for your real GitHub username
  if it isn't `ksgames`.
- Add a couple more articles over time — search engines reward sites that
  keep publishing, not just a one-time batch.
- Consider a custom domain later (Settings → Pages → Custom domain) once the
  site has some traction — it's a one-line DNS change away.
