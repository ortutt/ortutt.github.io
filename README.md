# ortutt.github.io

Personal academic website of Or Tuttnauer — plain HTML and one stylesheet, no build step.

| Page | File |
| --- | --- |
| Home | `index.html` |
| About | `about/index.html` |
| Research | `research/index.html` |
| Teaching | `teaching/index.html` |
| CV | `cv/index.html` |
| Web Apps | `web-apps/index.html` |
| Contact | `contact/index.html` |
| Publications | served by the separate [`publications`](https://github.com/ortutt/publications) repo at `/publications/` |

Styles live in `assets/style.css` and match the `publications` page.

## Editing

Edit the HTML file for a page and commit. The navigation bar is repeated in every page's `<header>`; if you add a page, add its link in each file.

Research projects use native `<details>`/`<summary>` elements, so they collapse without any JavaScript:

```html
<details class="card">
  <summary>Project title</summary>
  <div class="prose">
    <p class="dates">Start – End</p>
    <p>Description…</p>
  </div>
</details>
```

## Domain

The site is served at **ortuttnauer.com** (set by the `CNAME` file). The domain is registered with WordPress.com and kept as a domain-only site there; its DNS records point to GitHub Pages:

- `A` records for the root domain: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- `CNAME` for `www` → `ortutt.github.io`
- `TXT` for `_atproto` (Bluesky handle verification) — keep this record

All images and syllabus PDFs live in `assets/` (syllabi in `assets/syllabi/`), so nothing depends on WordPress.
