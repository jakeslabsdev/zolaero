# 🫧 Zolaero 

A minimalist, responsive **Frutiger Aero** theme for the Zola static site generator. 

Zolaero is designed for technical writers, researchers, and developers who want a clean, lightning-fast architecture wrapped in the nostalgic aesthetics of the mid-2000s. Think Apple's liquid glass meets Windows Aero: glossy transparencies, crisp white interfaces, subtle light-blue hatching, and deep, vibrant backgrounds.

## ✨ Features

* **Liquid Glass Viewport:** The central content card uses advanced CSS backdrop filters to create a frosted, glossy glass effect that highlights the background without sacrificing readability.
* **Technical Image Framing:** Images are automatically scaled, rounded, and wrapped in a subtle blue-hatched blueprint border.
* **Modular Configuration:** Easily customize the navigation menu, inject custom CSS, and manage metadata without touching the HTML templates.
* **SEO & OpenGraph Ready:** Automatically generates rich preview cards for Twitter, Discord, and Slack based on your frontmatter.

## 📥 Installation

The easiest way to install Zolaero is to add it as a Git submodule to your existing Zola site.

1. From your Zola site's root directory, run:
   ```bash
   git submodule add https://github.com/jakeslabsdev/zolaero themes/zolaero
   ```
2. Update your `config.toml` to use the theme:
   ```toml
   theme = "zolaero"
   ```

## ⚙️ Configuration

Zolaero handles custom navigation and metadata through the `[extra]` block in your `config.toml` file. Copy the following defaults into your configuration and adjust them to fit your site:

```toml
[extra]
# Author info for footer and SEO metadata
author_name = "Your Name"
author_github = "https://github.com/yourusername"
display_author = true

# Allow users to inject their own stylesheets (place files in your static/ folder)
custom_css = []

# Dynamic navigation menu mapped to your URLs
zolaero_menu = [
    { name = "/home/", url = "/" },
    { name = "/archive/", url = "/archive/" },
    { name = "/tags/", url = "/tags/" },
    { name = "/about/", url = "/about/" },
]

# Ensure recent posts show up on the homepage hero section
list_pages = true
```

## 📝 Writing Content

Zolaero automatically generates a Table of Contents for articles that contain headings. If you want to disable it on a specific post, add `toc = false` under `[extra]` in your markdown frontmatter:

```toml
+++
title = "My Technical Writeup"
date = 2026-11-17

[extra]
toc = false
+++
```

## 📜 License

Zolaero is open-source and licensed under the MIT License.
