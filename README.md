# rschhina.com

Plain static personal academic website. No build step, no framework — hand-written
HTML with one small stylesheet, in the style of minimal academic pages.

## Structure

- `index.html` — home: bio, working papers, works in progress, small business index
- `writing.html` — essays, anthologies, interview, Punjabi Substack
- `css/main.css` — the entire stylesheet
- `pdf/` — CV and paper drafts (linked from index)
- `img/raman.jpg` — profile photo

## Editing

To add a paper: add an `<li>` inside the relevant `<ul class="dash">` in `index.html`.
To update a draft: replace the PDF in `pdf/` keeping the same filename (links stay valid).

## Local preview

```bash
python3 -m http.server 8788
```

then open http://localhost:8788

## Deploy (GitHub Pages)

1. Push this repo to GitHub (e.g. `econ-raman/rschhina-website`).
2. Repo Settings → Pages → Source: `main` branch, root folder.
3. Add custom domain `rschhina.com` in the Pages settings (creates a `CNAME` file).
4. At the domain registrar, point an ALIAS/A record at GitHub Pages IPs and
   `www` CNAME at `<username>.github.io`, then enable Enforce HTTPS.
