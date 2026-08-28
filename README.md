# Simon Lab website

Static site for the Computational Biology group of Lukas "Miko" Simon, PhD
(Therapeutic Innovation Center, Baylor College of Medicine).

Two files do the work: `index.html` and `style.css`. No build step, no
dependencies, no JavaScript.

## Deploy to GitHub Pages

```bash
git init && git add . && git commit -m "Simon Lab website"
git branch -M main
git remote add origin git@github.com:<user>/<repo>.git
git push -u origin main
```

Then in the repo: **Settings → Pages → Source: Deploy from a branch →
`main` / `/ (root)`**. The site appears at `https://<user>.github.io/<repo>/`
within a minute or two. For a custom domain, add a `CNAME` file containing the
domain and point a DNS CNAME record at `<user>.github.io`.

## Editing

- **Publications** — `<li>` blocks under `#publications`, newest first, grouped
  by `<h3 class="year">`. Each entry carries a PubMed link and a DOI link. Add
  `<span class="tag hl">Highlight</span>` after the title to flag a key paper,
  or `<span class="tag">Preprint</span>` for a preprint. The current list was
  generated from PubMed metadata for `Simon LM[Author]`; a paper by the
  unrelated author Lisa M. Simon was excluded by hand, so check affiliations
  before bulk-adding from a search.
- **People** — copy the `article.card.person` block, change the initials in
  `.avatar`, the name, role and blurb. There is a comment marking the spot.
- **Photos** — drop files in the repo and replace `.avatar` with
  `<img class="avatar" src="people/name.jpg" alt="">`.
- **Colors** — the CSS variables at the top of `style.css`. Dark mode mirrors
  them in the `prefers-color-scheme` block; change both.
