# RECOMP.

Personal body recomposition tracker — nutrition, training, steps, and progress in one app.

## Features

- **Macro tracking** with AI-powered food search (Claude API), barcode scanning (Open Food Facts global DB), quick-add presets, and manual entry
- **Step counter** with 7,000 daily target, quick-add buttons, manual input, and Google Fit sync
- **Training programme** — 5-day upper body split with expandable exercise tutorials
- **Progress tracking** — daily score, predicted weight loss, weight chart, adherence stats
- **PWA** — installable to home screen, works offline (except AI search)

## Setup

This is a single `index.html` file hosted on GitHub Pages.

### Deploy

1. Push `index.html` to this repo
2. Go to Settings → Pages → Source: Deploy from branch → Branch: `main` → `/ (root)` → Save
3. Access at `https://mikeneilson83.github.io/recomp/`

### Google Fit (optional)

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a project (or use existing)
3. Enable the **Fitness API**
4. Go to Credentials → Create Credentials → OAuth 2.0 Client ID → Web application
5. Add `https://mikeneilson83.github.io` as an Authorized JavaScript origin
6. Copy the Client ID
7. In the app, tap "Connect Google Fit" and paste the Client ID when prompted

## Tech

- Pure HTML/CSS/JS — no build step, no dependencies
- localStorage for data persistence
- Claude API for AI food lookup (requires HTTPS)
- Open Food Facts API for barcode lookup
- Google Fit REST API for step sync (OAuth2 implicit flow)
