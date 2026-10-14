# Project Workflow

This repo follows the global development workflow (issues for every task, milestones, docs updated in every PR, code review before merge). Repo-specific notes:

## What this is

A static GitHub Pages site for the Promo-Blocker org, served from the `main` branch root. It exists mainly to host the privacy policy URL that the Chrome Web Store listing for Promoted Post Hider for Reddit points at. Keep it to plain HTML and CSS with no scripts and no external assets, so the site itself has nothing to disclose.

## Conventions

- One directory per page with an `index.html` inside so URLs end in `/` (for example `privacy/index.html` serves `/privacy/`).
- Absolute paths for shared assets (`/styles.css`) so nested pages resolve them.
- Every page carries the Reddit non-affiliation sentence.
- The privacy policy effective date changes whenever the policy text changes.
- Branches: `feat/<issue#>-slug`, `fix/<issue#>-slug`, `chore/<issue#>-slug`
- Commits and squash-merge titles: Conventional Commits (`feat:`, `fix:`, `chore:`, `docs:`, `refactor:`)
- Every PR updates `CHANGELOG.md` under `[Unreleased]` and links its issue with `Closes #N`
- `.claude/.code-reviewed` is the local code-review marker consumed by the merge-guard hook; it is gitignored and must never be committed or written without an actual `/code-review` run
