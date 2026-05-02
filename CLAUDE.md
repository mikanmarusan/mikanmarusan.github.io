# Project Instructions

## WHY — Purpose & Context

This repository contains the source for my personal portfolio site, published at
<https://mikanmarusan.net>. It exists to give a single, lightweight landing page
that introduces me, lists featured open-source projects, and links to my public
profiles. The site is intentionally hand-rolled — fast to load, simple to
maintain, no framework lock-in.

The repository is **public**. Anything committed here is world-readable.

## WHAT — Architecture & Key Decisions

- **Stack:** plain static HTML/CSS/JS. No build step. No package manager. No
  Jekyll (`_config.yml` is intentionally absent even though GitHub Pages
  defaults to Jekyll).
- **Files at repo root:**
  - `index.html` — single landing page (Home / About / Projects / Contact)
  - `styles.css` — site styles
  - `script.js` — small DOM enhancements (mobile nav, smooth scroll, fade-ins)
  - `terms.html`, `privacypolicy.html` — legal pages
  - `CNAME` — binds the custom domain `mikanmarusan.net`
- **Hosting:** GitHub Pages, user site, served from the `main` branch root.
- **Deployment trigger:** every push to `main` redeploys the live site within
  ~1 minute. Treat `main` as production.
- **Dependencies (runtime, loaded by `index.html`):** Google Fonts (Inter),
  cdnjs Font Awesome. No npm dependencies.
- The featured-project list lives in `index.html` only. Do not duplicate it in
  README.md or CLAUDE.md — they will drift.

## HOW — Development Workflow

- **Local preview:** open `index.html` directly in a browser, or run
  `python3 -m http.server 8000` from the repo root and visit
  `http://localhost:8000/`.
- **Branching:** create a feature branch before any change —
  `<type>/<kebab-case-description>` (Conventional Commits). Never commit
  directly to `main`.
- **Commits:** Conventional Commits format (`<type>(<scope>): <summary>`).
- **Deploy:** merge to `main` via PR; GitHub Pages republishes automatically.
  No separate build step.
- **Project-specific guardrails** live under `.claude/rules/`. Read every file
  in that directory before making changes.
