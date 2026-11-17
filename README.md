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

## Moving the domain

When ortuttnauer.com is ready to move from WordPress.com:

1. Add a file named `CNAME` containing `ortuttnauer.com` (or set it under Settings → Pages → Custom domain).
2. At the DNS provider, point the apex domain to GitHub Pages (A records `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`) and `www` as a CNAME to `ortutt.github.io`.
3. Once the certificate is issued, tick **Enforce HTTPS**.

The portrait and syllabus PDFs are still loaded from `ortuttnauer.wordpress.com/wp-content/uploads/…`. Copy them into `assets/` and update the links before closing the WordPress site.
