# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is Jeff Liu's personal tech blog, built with **Hexo** static site generator and the **NexT** theme.

- **Live Site:** https://bluesmmm.github.io/
- **Repository:** https://github.com/Bluesmmm/bluesmmm.github.io.git

## Development Commands

### Local Development

Start the local development server:
```bash
hexo server
# or
hexo s
```
Site runs at `http://localhost:4000`

### Creating Content

Create a new blog post:
```bash
hexo new "Post Title"
```
Creates `source/_posts/Post-Title.md`

Create a new page:
```bash
hexo new page "page-name"
```
Creates `source/page-name/index.md`

### Build and Deploy

Generate static files:
```bash
hexo generate
# or
hexo g
```

Deploy to GitHub Pages (generates + deploys):
```bash
hexo deploy
# or
hexo d
```

Generate and deploy in one command:
```bash
hexo clean && hexo generate && hexo deploy
```

### Other Useful Commands

Clean generated files:
```bash
hexo clean
```

List all posts:
```bash
hexo list post
```

## Project Structure

```
.
├── _config.yml          # Hexo main configuration
├── source/
│   ├── _posts/         # Blog posts (Markdown files)
│   ├── about/          # About page
│   ├── categories/     # Category pages (auto-generated)
│   ├── tags/           # Tag pages (auto-generated)
│   └── _data/
│       └── next.yml    # NexT theme custom config (overrides theme defaults)
├── themes/
│   └── next/           # NexT theme (git submodule)
├── package.json        # Node.js dependencies
└── CLAUDE.md          # This file
```

## Configuration

### Main Config (`_config.yml`)

Key settings:
- Site title, author, description
- URL: `https://bluesmmm.github.io`
- Theme: `next`
- Deployment: configured for GitHub Pages (main branch)
- Post asset folder: enabled (`post_asset_folder: true`)

### Theme Config (`source/_data/next.yml`)

This overrides the default NexT theme configuration:
- Scheme: Gemini
- Dark mode: enabled
- Menu: home, archives, tags, categories, about
- Social links: GitHub, Email
- Local search: enabled
- FancyBox: enabled for image zooming
- Reading progress bar: enabled

## Writing Posts

Posts are written in Markdown with front matter:

```markdown
---
title: Your Post Title
date: 2026-01-11 21:00:00
tags: [tag1, tag2]
categories: [Category Name]
---

# Content here

Write your post content in Markdown.
```

### Front Matter Options

- `title`: Post title
- `date`: Publication date
- `tags`: Array of tags (creates tag pages automatically)
- `categories`: Array of categories
- `description`: Custom excerpt (optional)
- `toc`: Table of contents (override default)

## Theme Customization

The NexT theme is customized via `source/_data/next.yml`. When modifying theme settings:

1. Edit `source/_data/next.yml` (preferred - won't conflict with theme updates)
2. Or edit `themes/next/_config.yml` (will conflict on theme updates)

## Deployment

Deployment to GitHub Pages is configured in `_config.yml`:

```yaml
deploy:
  type: git
  repo: https://github.com/Bluesmmm/bluesmmm.github.io.git
  branch: main
```

To deploy:
```bash
hexo clean && hexo generate && hexo deploy
```

Note: Generated files in `public/` are committed to the repository and served by GitHub Pages.

## Installed Plugins

- `hexo-deployer-git` - Git deployment
- `hexo-generator-feed` - RSS/Atom feed generation
- `hexo-generator-sitemap` - Sitemap generation
- `hexo-generator-searchdb` - Local search functionality
- `hexo-generator-tag` - Tag page generation
- `hexo-generator-category` - Category page generation
- `hexo-generator-index` - Index page generation

## Adding Images

To add images to posts:

1. With post asset folders enabled, create a folder alongside your post:
   ```
   source/_posts/
   ├── my-post.md
   └── my-post/
       └── image.png
   ```

2. Reference using relative path:
   ```markdown
   {% asset_graph image.png %}
   ```
   Or standard Markdown:
   ```markdown
   ![Alt text](image.png)
   ```

## Theme Schemes

NexT supports 4 schemes. Edit `source/_data/next.yml` to change:
- `Muse` - Default, simple
- `Mist` - Compact, sidebar on top
- `Pisces` - Dual column
- `Gemini` - Dual column, improved layout (current)

## Common Tasks

### Change Theme Color/Scheme
Edit `source/_data/next.yml` and modify the `scheme` value.

### Add Social Links
Edit `source/_data/next.yml` under the `social:` section.

### Configure Analytics
Add your tracking ID to `source/_data/next.yml` under `google_analytics:`.

### Create a Tag Page
Tags are automatically generated when you use the `tags` front matter in posts.

### Create a Category Page
Categories are automatically generated when you use the `categories` front matter in posts.

## Resources

- [Hexo Documentation](https://hexo.io/docs/)
- [NexT Theme Documentation](https://theme-next.js.org/)
- [Markdown Guide](https://www.markdownguide.org/)
