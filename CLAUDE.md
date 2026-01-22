# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal portfolio website built with Jekyll and the Just the Docs theme. The site showcases writing, artworks, and game design work. It's deployed to GitHub Pages.

## Technology Stack

- **Generator**: Jekyll 4.3.3
- **Theme**: Just the Docs
- **Language**: Ruby 3.3.4
- **Deployment**: GitHub Pages
- **Content Management**: Decap CMS (configured in `.pages.yml`)

## Common Commands

### Local Development

Install dependencies:
```bash
bundle install
```

Build and serve the site locally:
```bash
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`

Build without serving:
```bash
bundle exec jekyll build
```

Build with drafts visible:
```bash
bundle exec jekyll serve --drafts
```

### Testing

CI runs automatically on push and pull request:
```bash
bundle exec jekyll build
```

This validates the site builds correctly. The build output goes to `_site/`.

## Directory Structure

- **`_posts/`** - Published blog posts (Markdown files with YAML frontmatter)
- **`_drafts/`** - Draft posts (not published until moved to `_posts`)
- **`pages/`** - Static pages (about, archive, categories, etc.)
- **`_layouts/`** - Page layout templates
- **`_includes/`** - Reusable template components
- **`_sass/`** - SCSS files, with `custom/` containing theme overrides
- **`assets/`** - CSS and other static assets
- **`images/`** - Image files used in layouts
- **`fonts/`** - Font files
- **`uploads/`** - Media files managed via Decap CMS

## Key Configuration Details

### Jekyll Config (`_config.yml`)

- **Permalink format**: `/:title/` (clean URLs based on post title)
- **Excerpt separator**: `<!--more-->` (used to define post previews)
- **Paginate**: 6 posts per page
- **Collections**:
  - `posts` - Blog posts with full output
  - `uploads` - Media files
  - `artworks` - Artwork collection with custom fields (title, year)
- **Plugins**: jekyll-default-layout, jekyll-sitemap, jekyll-feed, jekyll-seo-tag, jekyll-paginate, classifier-reborn (for content classification)
- **Search**: Enabled with indexing at heading level 2

### Decap CMS Config (`.pages.yml`)

Provides a UI for managing content. Key collections configured:
- **Drafts**: Draft posts in `_drafts/` with publish state, date, categories
- **Pages**: Static pages in `pages/` with nav order, splash image, layout selection
- **Posts**: Blog posts in `_posts/` with publication status, date, categories, splash images

## Content Publishing Workflow

1. Content can be created via Decap CMS or directly in Markdown
2. Posts in `_drafts/` won't publish even with `show_drafts: true` in config unless moved to `_posts/`
3. Post files must follow naming convention: `YYYY-MM-DD-slug.md`
4. All posts include YAML frontmatter (title, date, categories, etc.)
5. Posts can use the `<!--more-->` separator to define excerpt for previews
6. Pushed changes trigger automatic deployment via GitHub Actions

## Deployment

- **Pages workflow** (`.github/workflows/pages.yml`) - Builds and deploys to GitHub Pages on push to main
- **CI workflow** (`.github/workflows/ci.yml`) - Validates build on push and pull requests
- Site is served from the root of `lucashaley.github.io` repository

## Development Notes

- The theme uses "Just the Docs" which provides search and sidebar navigation
- SCSS customizations should go in `_sass/custom/` to avoid overwriting theme defaults
- The site includes Twitter, LinkedIn, and GitHub social metadata
- Markdown files use GFM (GitHub Flavored Markdown) with Rouge syntax highlighting
- The `lsi: true` setting enables latent semantic indexing for better search results
