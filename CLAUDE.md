# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Type
This is a GitHub Pages repository (mikanmarusan.github.io) for hosting a personal website or portfolio.

## Common Commands
Since this is a new repository, typical GitHub Pages workflows will include:

- `git add .` - Stage all changes
- `git commit -m "message"` - Commit changes
- `git push origin main` - Deploy changes to GitHub Pages

## Architecture Notes
- GitHub Pages serves content from the `main` branch root directory
- Static files (HTML, CSS, JS) should be placed in the root directory
- Common structure includes:
  - `index.html` - Main landing page
  - `assets/` or `css/`, `js/`, `images/` directories for static resources
  - `_config.yml` if using Jekyll (GitHub Pages' default static site generator)

## Development Considerations
- GitHub Pages has a build process that may take a few minutes to reflect changes
- Local testing can be done by opening HTML files directly in a browser or using a local server
- If using Jekyll, local development requires Ruby and the Jekyll gem