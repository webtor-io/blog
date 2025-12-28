### Project Overview
This project is a multilingual blog powered by [Hugo](https://gohugo.io/). It supports English (EN) and Russian (RU) content.

### Build/Configuration Instructions
#### Prerequisites
- **Hugo**: Ensure you have Hugo installed (extended version is recommended). You can check your version with `hugo version`.

#### Building the Site
To build the site, run the following command in the project root:
```bash
hugo
```
The generated static files will be located in the `public/` directory.

#### Running Locally
To preview the site locally with live reloading:
```bash
hugo server
```

### Testing Information
#### Configuration and Running Tests
Since this is a static site generator project, "testing" primarily involves ensuring that the build process completes successfully and generates the expected files.

#### Automated Build Test
You can use a script to verify the build. Below is an example of a simple build verification script:

```bash
#!/bin/bash
set -e

# Clear public directory if it exists
if [ -d "public" ]; then
    rm -rf public
fi

# Run Hugo build
hugo

# Verify output
if [ -d "public" ] && ([ -f "public/en/index.html" ] || [ -f "public/ru/index.html" ]); then
    echo "Build verification SUCCESSFUL"
else
    echo "Build verification FAILED"
    exit 1
fi
```

#### Guidelines for New Tests
When adding new features or changing the theme structure, consider adding checks for:
- Specific expected files (e.g., RSS feeds, sitemaps).
- Presence of key CSS/JS bundles.
- Metadata in generated HTML (tags, series links).

### Additional Development Information
#### Content Organization
- Content is split by language: `content/en/` and `content/ru/`.
- Posts are typically organized in subdirectories: `content/en/post/<slug>/index.md`.

#### Front Matter Conventions
Each post should include the following front matter:
- `title`: Post title.
- `date`: Publication date in ISO 8601 format.
- `series`: (Optional) Group posts by series (e.g., "What's new").
- `translationKey`: **CRITICAL**. Use the same key for English and Russian versions of the same post to link them.
- `titleEmoji`: (Optional) An emoji to display next to the title.
- `aliases`: (Optional) URL redirects.

Example:
```yaml
---
title: "New Feature"
date: 2024-12-28T12:00:00+03:00
series: "Updates"
translationKey: "my-new-feature"
titleEmoji: ":rocket:"
---
```

#### Code Style
- Follow standard Markdown practices.
- Use `hugo server` to verify layout changes in real-time.
- The theme is located in `themes/hugo-theme-basic`. Avoid modifying it directly if possible; use layout overrides in the root `layouts/` directory if needed.
