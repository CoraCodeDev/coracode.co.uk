# CoraCode Website - Agent Guide

## Overview

This is the source code for coracode.co.uk - the public website for CoraCode.

## Tech Stack

- **Static site** - Plain HTML/CSS/JS for simplicity
- **No framework** - Keep it lightweight, no build step needed
- **Hosting** - GitHub Pages (see Confluence)

## Project Structure

```
/
├── index.html          # Home page
├── projects.html       # Projects listing
├── skills.html         # OpenClaw skills
├── contact.html        # Contact page
├── blog.html          # Blog/updates
├── css/
│   └── style.css      # Main stylesheet
├── js/
│   └── main.js        # JavaScript
├── posts/              # Blog posts (markdown)
├── assets/
│   ├── logo.svg       # C/C logo
│   └── images/        # Images
└── downloads/         # App downloads
```

## Design Guidelines

- Keep it simple and professional
- Use the C/C logo in assets/logo.svg
- Dark theme (slate/navy), cyan accents
- Mobile-first responsive design
- No flashy animations - clean and professional

---

## Workflow & Review Process

### 1. NEVER commit directly to main
All changes must go through a feature branch.

### 2. Create a branch for each task
```bash
git checkout -b feature/CCW-4-home-page
```

### 3. Work on your changes
- Test locally by opening index.html in browser
- Or run a simple server: `python -m http.server`

### 4. Create a Pull Request
```bash
git add .
git commit -m "feat: add home page content"
git push -u origin feature/CCW-4-home-page
gh pr create --title "feat: add home page content" --body "Addresses CCW-4"
```

### 5. Review Process (REQUIRED)
- **NEVER review your own PRs**
- Ask for review (you or user can review)
- Address feedback
- Wait for approval before merging

### 6. Merge to main
- Only after approval
- Don't delete branch immediately (keep for reference)

### 7. Deployment
- Site deploys automatically from main
- BUT: GitHub Pages is currently disabled
- **Don't enable without user approval**

---

## Adding Content

### New Page
1. Create HTML file in root
2. Add navigation to all pages
3. Update css/style.css if needed

### New Project
1. Add to projects.html
2. Add thumbnail to assets/images/
3. Optionally create dedicated page

### New Blog Post
1. Add markdown file to posts/
2. Include frontmatter:
```yaml
---
title: "Post Title"
date: 2026-03-23
description: "Short description"
---
```
3. Add to blog.html (or auto-generate list)

---

## Deployment

**IMPORTANT:** Site is hidden until launch.

- GitHub Pages disabled in repo settings
- Domain not configured yet
- See [Setup & Deployment Guide](https://davek.atlassian.net/wiki/spaces/CCW/pages/12943562) in Confluence

**Never enable deployment without explicit user approval.**

---

## Conventions

- Semantic HTML5
- CSS variables for colours (see css/style.css)
- BEM-ish class naming
- No external dependencies unless necessary
- All lowercase filenames

---

## Related

- Confluence: https://davek.atlassian.net/wiki/spaces/CCW
- Jira: https://davek.atlassian.net/browse/CCW
