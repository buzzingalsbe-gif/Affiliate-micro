# Release notes — v0.1.0

## Summary
Affiliate-micro v0.1.0 — a plug-and-play autonomous affiliate micro-bot for small sites and GitHub Pages. This initial release publishes the project as a lightweight, repo-driven affiliate assistant that runs via GitHub Actions and stores memory in the repo.

## Highlights
- Autonomous affiliate bot that runs on GitHub Actions (daily schedule).
- Easy setup for GitHub Pages (serve site from `main / site`).
- Configuration via `affiliates.json`.
- Uses an OpenRouter-compatible API key via secret `OPENAI_API_KEY`.
- Stores runtime memory in `memory.json` in the repo.

## What’s new in v0.1.0
- Initial public release:
  - Repo and Pages deployment instructions included.
  - Actions workflow to run the bot daily (7am ET).
  - Example configuration and basic documentation (README).

## Installation & setup
1. Clone the repo:
   ```bash
   git clone https://github.com/buzzingalsbe-gif/Affiliate-micro.git
   ```
2. Configure GitHub Pages:
   - Settings → Pages → Source: main / site
3. Add your OpenRouter/OpenAI key:
   - Settings → Secrets → New repository secret
   - Name: OPENAI_API_KEY, Value: <your OpenRouter key>
4. Edit `affiliates.json` with your real affiliate links and settings.
5. Actions → Enable workflows → Run workflow (workflows are scheduled daily at 7am ET).

## Quick start
- Enable the repository's workflows and Pages as above. The bot will run on the schedule configured in Actions and update the repo as designed.

## Known limitations
- No LICENSE file detected in the repository — consider adding a license (MIT, Apache-2.0, etc.).
- No UI included — API/repo-first approach.
- Intended for small sites; minimal rate-limiting/auth by default.

## Contributors
- @buzzingalsbe-gif (maintainer)

## Reporting bugs & contributing
- File bugs and feature requests at: https://github.com/buzzingalsbe-gif/Affiliate-micro/issues
- Contributions welcome — add a PR or open an issue for guidance.

## License
- No license file found in the repo. Please add a LICENSE file to make reuse terms clear.
