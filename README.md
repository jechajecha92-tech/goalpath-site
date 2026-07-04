# goalpath.site — Academic Website of Jecha S Jecha

Personal academic website for Jecha S Jecha, PhD student at Southwest
University (Chongqing, China) and Assistant Lecturer at Zanzibar University.
Built with native Jekyll and deployed on GitHub Pages at
[goalpath.site](https://goalpath.site).

## Stack

- **Jekyll** (GitHub Pages compatible — no custom plugins)
- **Liquid** templates, **Markdown** content, **SCSS** styling
- **Vanilla JavaScript** only where needed (mobile navigation, BibTeX/abstract
  toggles)
- No frameworks, no build tooling beyond Jekyll itself

## Architecture

### Content as data

Structured content lives in `_data/` so pages stay free of markup duplication:

| File | Purpose |
| --- | --- |
| `_data/navigation.yml` | Single source of truth for the site navigation |
| `_data/publications.yml` | Publications with type, DOI, PDF, BibTeX, abstract, dataset, and code links |
| `_data/projects.yml` | Research software and academic projects |
| `_data/teaching.yml` | Courses and supervision |
| `_data/news.yml` | News items shown on the home page |
| `_data/cv.yml` | CV sections rendered on the CV page |

Author profile, positions, research interests, and social/profile links are in
`_config.yml` under `author:` so they can be referenced from any template.

### Layouts and includes

- `_layouts/default.html` — HTML shell: head, skip link, header, footer
- `_layouts/page.html` — standard content page (title + prose)
- `_layouts/post.html` — blog post with metadata and JSON-LD article schema
- `_layouts/home.html` — home page composition
- `_includes/` — one component per file (`head.html`, `header.html`,
  `footer.html`, `seo.html`, `publication.html`, `post-card.html`,
  `profile-links.html`, …). Components are parameterized with Liquid
  `include` variables and never duplicated.

### Styling

SCSS is organized under `_sass/` and compiled by Jekyll from
`assets/css/main.scss`:

- `_variables.scss` — palette, typography scale, spacing, breakpoints
- `_base.scss` — reset, typography, focus states
- `_layout.scss` — header, footer, page grid
- `_components.scss` — buttons, cards, publication entries, tags, news list

The palette is neutral (near-black text on white, one restrained accent) and
type is set in a system font stack for zero font-loading cost.

### SEO

- Custom `_includes/seo.html`: canonical URL, Open Graph, Twitter Cards, and
  JSON-LD (`Person` with affiliations for the site, `ScholarlyArticle` for
  publications, `BlogPosting` for posts)
- Hand-rolled `sitemap.xml`, `feed.xml` (Atom), and `robots.txt` as Liquid
  templates — no plugin dependency

### Accessibility

Skip link, semantic landmarks (`header`/`nav`/`main`/`footer`), visible focus
states, ARIA labels on icon-only controls, keyboard-operable disclosure
buttons for abstracts/BibTeX, and WCAG AA color contrast.

## Local development

```sh
bundle install
bundle exec jekyll serve
# → http://localhost:4000
```

## Deployment

Pushing to `main` deploys via GitHub Pages. `CNAME` pins the custom domain
`goalpath.site`; configure DNS with an A/ALIAS record to GitHub Pages and
enable **Enforce HTTPS** in the repository settings.

## Updating content

- **Add a publication:** append an entry to `_data/publications.yml`.
- **Add a blog post:** create `_posts/YYYY-MM-DD-title.md` with `title`,
  `description`, and `tags` front matter.
- **Add a project / course / news item:** edit the matching `_data/*.yml`.
- **Update the CV:** edit `_data/cv.yml` and replace
  `assets/files/jecha-s-jecha-cv.pdf`.

## License

Code is MIT licensed (see `LICENSE`). Site content © Jecha S Jecha.
