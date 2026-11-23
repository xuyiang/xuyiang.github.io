# Yiang Xu — Academic Homepage

A minimal, single-column academic homepage. Plain HTML, one stylesheet, one tiny
script. No build step, no framework, no tracking, no external requests.

```
index.html              # all content
assets/css/styles.css   # narrow one-column layout, light + dark
assets/js/site.js       # theme toggle + footer year
assets/docs/            # CV (PDF)
.nojekyll               # tell GitHub Pages to serve files as-is
```

## Run it locally

Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8000   # then visit http://localhost:8000
```

## Deploy on GitHub Pages (free)

1. Create a public repo. For the shortest URL, name it **`<your-username>.github.io`**
   (e.g. `yiangxu.github.io`) — the site then lives at `https://<your-username>.github.io/`.
   Any other name works too, at `https://<your-username>.github.io/<repo>/`.
2. Push this folder's contents to the repo root on `main`.

   ```bash
   git init
   git add .
   git commit -m "Academic homepage"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo>.git
   git push -u origin main
   ```

3. In the repo: **Settings → Pages → Source: Deploy from a branch**, choose
   `main` and `/ (root)`, then save.
4. Wait a minute or two; the URL appears on the same settings page.

HTTPS is automatic and free. GitHub Pages is free for public repos.

## Editing

Everything is in `index.html`, in reading order: intro, Publications, Research,
Experience, Education. Type and spacing are CSS custom properties at the top of
`assets/css/styles.css` — `--measure` controls the column width.

To add a publication, copy one `<article class="entry">` block. To add a row to
Experience or Education, copy one `<li>` inside `.rows`.
