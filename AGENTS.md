# CoraCode Website - Agent Guide

## Overview

Source code for coracode.co.uk — the public website for CoraCode.

## Tech Stack

- **Jekyll** — static site generator (built into GitHub Pages)
- **Custom CSS** — no external frameworks
- **No JavaScript** — plain HTML/CSS, fast loading

## Project Structure

```
/
├── _config.yml           # Jekyll config (site title, defaults)
├── _layouts/
│   └── default.html      # Base layout (wraps all pages)
├── _includes/
│   ├── header.html       # Navigation bar (shared)
│   └── footer.html       # Footer (shared)
├── index.html            # Homepage
├── projects.html         # Projects listing
├── skills.html           # OpenClaw skills
├── contact.html          # Contact page
├── assets/
│   └── css/
│       └── style.css     # Main stylesheet
└── AGENTS.md             # This file
```

## Adding Pages

1. Create `.html` file in root with frontmatter:
```yaml
---
title: Page Title
description: Short description for meta tag
---
```
2. Content goes after the `---` — it gets injected into the default layout.
3. Nav link: add to the `nav_items` list in `_includes/header.html`.

## Adding CSS

Just edit `assets/css/style.css`. No build step needed — Jekyll copies it as-is.

## Design Guidelines

- Dark theme (slate/navy), cyan accents (`#06b6d4`)
- System font stack — no external fonts
- Mobile-first responsive
- No flashy animations — clean and professional

## Workflow

### NEVER commit directly to main
All changes go through feature branches.

### Branch naming
`feature/CCW-<number>-<short-desc>`

### Local development
```bash
# Quick preview (no Jekyll, just files):
python3 -m http.server 8000
# Then visit http://localhost:8000

# Full Jekyll build (requires ruby):
bundle exec jekyll serve
```

### PR Process
1. Create branch, push
2. Open PR — **never review your own**
3. Reviewer pulls branch, tests locally
4. Merge after approval

## Deployment

- GitHub Pages builds from `main` branch
- Domain: coracode.co.uk (configured in repo Settings → Pages)
- **Never enable deployment without explicit user approval**

## Related

- Jira: https://davek.atlassian.net/browse/CCW
- Confluence: https://davek.atlassian.net/wiki/spaces/CCW
