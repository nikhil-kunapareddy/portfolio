# CLAUDE.md

## Overview
Personal portfolio website for Sai Nikhil Kunapareddy. A static, hand-written HTML/CSS site with no build step or framework.

## Structure
- `index.html` — home page (Research, Experience, Education sections)
- `styles.css` — site styles
- `images/` — image assets
- `CNAME` — custom domain (www.sainikhil.com)

## Development
No build tooling. Edit the HTML/CSS directly and open `index.html` in a browser, or serve locally:

```
python3 -m http.server 8000
```

## Deployment
Hosted on GitHub Pages at the custom domain in `CNAME`. Pushing to `main` deploys. See `DEPLOY-GITHUB-PAGES.md` for details.

## Conventions
- Plain semantic HTML; section content lives in `<section>` blocks with `work-entry` / `edu-entry` classes.
- The "Projects" nav link points directly to the GitHub profile (no projects page).
- Keep styling in the existing CSS files rather than inline styles.
- `venv/` is git-ignored and unrelated to the site itself.
