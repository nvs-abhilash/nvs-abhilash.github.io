# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a personal website and blog built with Jekyll, using the [minima](https://github.com/jekyll/minima) remote theme. It is deployed via GitHub Pages.

## Commands

```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll serve

# Build for production
bundle exec jekyll build

# Update dependencies
bundle update
```

The local server runs at `http://localhost:4000` by default. Note: changes to `_config.yml` require restarting the server.

## Architecture

- **`_config.yml`**: Central site config — title, theme, plugins, nav pages, social links, and analytics.
- **`index.md`**: Home page using the `home` layout; includes `social.html`.
- **`pages/`**: Static content pages (`research.md`, `oss.md`, `patents.md`, `projects.md`, `posts.md`). Each uses the `page` layout and has a `permalink`.
- **`_posts/`**: Blog posts in `YYYY-MM-DD-title.md` format.
- **`_includes/`**: Custom template overrides — `custom-head.html` (favicon, FontAwesome CDN) and `footer.html` (social links + site description).
- **`_sass/minima/custom-styles.scss`**: Custom CSS overrides for the minima theme (e.g., fixed navbar, page top margin).
- **`assets/`**: Static assets including profile picture.
- **`favicon/`**: Favicon files in multiple formats.

## Theme Customization

The site uses `remote_theme: jekyll/minima` with `skin: auto` (light/dark based on OS preference). Customizations are layered on top:
- Override theme layouts/includes by placing files with the same name in `_includes/` or `_layouts/`
- Add styles in `_sass/minima/custom-styles.scss` (automatically picked up by minima's SCSS pipeline)
- Social links are configured in `_config.yml` under `minima.social_links`

## Content Structure

- Nav order is controlled by `header_pages` in `_config.yml`
- New pages go in `pages/` with front matter: `layout: page`, `title`, `permalink`
- New blog posts go in `_posts/` with filename `YYYY-MM-DD-slug.md`
