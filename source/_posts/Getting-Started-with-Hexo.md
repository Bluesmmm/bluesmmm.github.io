---
title: Getting Started with Hexo
date: 2026-01-11 21:05:04
tags: [hexo, blogging, web-development]
categories: [Tutorial]
---

# Getting Started with Hexo

[Hexo](https://hexo.io/) is a fast, simple, and powerful blog framework powered by Node.js. In this post, I'll walk you through the basics of setting up and using Hexo for your own blog.

## Why Hexo?

Hexo is one of the most popular static site generators for blogs. Here's why many developers choose it:

- **Fast** - Generates static files in seconds
- **Simple** - Easy to install and use with just a few commands
- **Powerful** - Supports Markdown, plugins, and custom themes
- **Free Hosting** - Works perfectly with GitHub Pages

## Installation

First, you need to have [Node.js](https://nodejs.org/) installed. Then install Hexo CLI globally:

```bash
npm install -g hexo-cli
```

## Creating a New Blog

Initialize your blog with a single command:

```bash
hexo init my-blog
cd my-blog
npm install
```

## Basic Commands

Here are the essential Hexo commands you'll use:

### Create a New Post

```bash
hexo new "My First Post"
```

This creates a new Markdown file in `source/_posts/`.

### Start the Local Server

```bash
hexo server
# or simply
hexo s
```

Your blog will be available at `http://localhost:4000`.

### Generate Static Files

```bash
hexo generate
# or
hexo g
```

### Deploy to GitHub Pages

```bash
hexo deploy
# or
hexo d
```

## Writing Posts

Posts are written in Markdown and stored in `source/_posts/`. Each post starts with front matter:

```markdown
---
title: My First Post
date: 2026-01-11 21:00:00
tags: [hexo, markdown]
categories: [Tutorial]
---

# Your Content Here

This is my first blog post using Hexo!
```

## Themes

Hexo has a rich ecosystem of themes. One of the most popular is [NexT](https://theme-next.js.org/), which offers:

- Multiple schemes and layouts
- Dark mode support
- Integrated search
- Responsive design
- Many customization options

## Next Steps

Now that you have a basic Hexo blog running:

1. Choose and customize a theme
2. Configure your `_config.yml` file
3. Write your first posts
4. Set up deployment (GitHub Pages, Netlify, etc.)
5. Install useful plugins (search, sitemap, RSS feed)

Happy blogging!
