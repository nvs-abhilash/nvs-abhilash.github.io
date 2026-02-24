# nvs-abhilash.github.io

Personal website and blog built with [Jekyll](https://jekyllrb.com/) and the [minima](https://github.com/jekyll/minima) theme, deployed via GitHub Pages.

## Local Development

```bash
bundle install
bundle exec jekyll serve
```

Open `http://localhost:4000`. Note: changes to `_config.yml` require restarting the server.

## Structure

- `_config.yml` — site settings, nav, social links, analytics
- `index.md` — home page
- `pages/` — static pages (research, OSS, patents, projects, posts)
- `_posts/` — blog posts (`YYYY-MM-DD-title.md`)
- `_includes/` — template overrides
- `_sass/minima/custom-styles.scss` — custom CSS
- `assets/` — static assets
