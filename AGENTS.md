# CoraCode Website - Agent Guide

## Overview

This is the source code for coracode.co.uk - the public website for CoraCode.

## Project Plan

See the detailed **Project Plan** in Confluence for task ordering and dependencies:
https://davek.atlassian.net/wiki/spaces/CCW/pages/12812568

**Current phases:**
- Phase 1: Foundation (CSS, layout, header, footer)
- Phase 2: Core Pages (Home, Projects, Skills, Contact)
- Phase 3: Infrastructure (CI/CD, Pages, Preview)
- Phase 4: Launch (Domain, Go live)

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
Use the Jira task number: `feature/CCW-12-css-variables`

### 3. Preview/Test Changes Locally
Before creating a PR, test your changes:

**Option A: Open directly in browser**
```bash
# Just double-click index.html to open in browser
# Or use a simple server:
python3 -m http.server 8000
# Then visit http://localhost:8000
```

**Option B: Pull the branch and test**
```bash
# After pushing your branch
git fetch origin
git checkout origin/feature/CCW-12-css-variables
# Open index.html in browser to test
```

### 4. Create a Pull Request
```bash
git add .
git commit -m "feat: add CSS variables"
git push -u origin feature/CCW-12-css-variables
gh pr create --title "feat: add CSS variables" --body "Addresses CCW-12"
```

### 5. Review Process (REQUIRED)
- **NEVER review your own PRs**
- Request review in PR
- Reviewer: pull branch locally and test in browser
- Review the code diff in GitHub
- Address feedback
- Wait for approval before merging

### 6. Merge to main
- Only after approval
- Don't delete branch immediately (keep for reference)

### 7. Deployment
- Site deploys automatically from main (once enabled)
- **GitHub Pages currently disabled**
- **Never enable deployment without user approval**

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

- Jira: https://davek.atlassian.net/browse/CCW
- Confluence: https://davek.atlassian.net/wiki/spaces/CCW
- **Project Plan:** https://davek.atlassian.net/wiki/spaces/CCW/pages/12812568
