# CoraCode Website - Agent Guide

## Overview

This is the source code for coracode.co.uk - the public website for CoraCode.

## Tech Stack

- **Static site** - Plain HTML/CSS/JS for simplicity
- **No framework** - Keep it lightweight, no build step needed
- **Hosting** - GitHub Pages or Cloudflare Pages (see Confluence)

## Project Structure

```
/
├── index.html          # Home page
├── projects.html       # Projects listing
├── skills.html        # OpenClaw skills
├── contact.html       # Contact page
├── css/
│   └── style.css      # Main stylesheet
├── js/
│   └── main.js       # JavaScript
├── assets/
│   ├── logo.svg      # C/C logo
│   └── images/       # Images
└── downloads/         # App downloads (future)
```

## Design Guidelines

- Keep it simple and professional
- Use the C/C logo in assets/logo.svg
- Colours: Dark theme (slate/navy), cyan accents
- Mobile-first responsive design
- No flashy animations - clean and professional

## Adding Content

### New Project
1. Create a new HTML page or add to projects.html
2. Add thumbnail to assets/images/
3. Update navigation

### New Skill
1. Add to skills.html
2. Link to ClawHub

## Deployment

See [Setup & Deployment Guide](https://davek.atlassian.net/wiki/spaces/CCW/pages/12943562) in Confluence.

**Important:** Site is hidden until we're ready to launch. Do not enable GitHub Pages without approval.

## Conventions

- Semantic HTML5
- CSS variables for colours
- BEM-ish class naming
- No external dependencies unless necessary

## Related

- Confluence: https://davek.atlassian.net/wiki/spaces/CCW
- Jira: https://davek.atlassian.net/browse/CCW
