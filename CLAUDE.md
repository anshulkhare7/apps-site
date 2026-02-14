# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repo hosts static web apps served via GitHub Pages at **apps.anshulkhare.com**. Each app lives in its own subfolder and is accessible at `apps.anshulkhare.com/<app-name>/`.

## Structure

```
apps-site/
├── CNAME                 # Custom domain config (do not modify)
├── index.html            # Landing page listing all apps
├── geronimo/             # Geronimo Stilton quiz app
│   └── index.html
└── <future-app>/         # Add new apps as subfolders
    └── ...
```

## Hosting & Deployment

- **Hosting:** GitHub Pages (static files, no build step)
- **Domain:** apps.anshulkhare.com (DNS via Cloudflare, CNAME → anshulkhare7.github.io)
- **SSL:** Cloudflare (proxied, SSL mode: Full)
- **Deploy:** Push to `main` branch — GitHub Pages deploys automatically

## Key Rules

- All apps are **static** (HTML/CSS/JS only, no server-side code)
- Do NOT modify the `CNAME` file — it controls the custom domain mapping
- When adding a new app, also add a link to the root `index.html` landing page
- Keep each app self-contained within its subfolder

## Adding a New App

1. Create a new subfolder: `<app-name>/`
2. Place the app's files inside it (entry point should be `index.html`)
3. Add a card/link to the root `index.html`
4. Push to `main` — it will be live at `apps.anshulkhare.com/<app-name>/`
