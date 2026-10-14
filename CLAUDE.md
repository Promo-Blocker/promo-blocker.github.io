# Project Workflow

This repo follows the global development workflow (issues for every task, milestones, docs updated in every PR, code review before merge). Repo-specific notes:

## First-time setup (after creating a repo from this template)

1. Fill in `README.md` (name, description, usage) and the license.
2. Create the standard labels:
   ```sh
   gh label create refactor --color D4C5F9 --description "Code restructuring with no behavior change" 2>/dev/null || true
   gh label create chore --color FEF2C0 --description "Maintenance, tooling, dependencies" 2>/dev/null || true
   ```
   (`bug`, `enhancement`, and `documentation` exist by default.)
3. Create a GitHub Project named after this repo and link it (`gh project create --owner <owner> --title "<repo>"`).
4. Create an initial milestone for the first body of work.

## Conventions

- Branches: `feat/<issue#>-slug`, `fix/<issue#>-slug`, `chore/<issue#>-slug`
- Commits and squash-merge titles: Conventional Commits (`feat:`, `fix:`, `chore:`, `docs:`, `refactor:`)
- Every PR updates `CHANGELOG.md` under `[Unreleased]` and links its issue with `Closes #N`
- `.claude/.code-reviewed` is the local code-review marker consumed by the merge-guard hook; it is gitignored and must never be committed or written without an actual `/code-review` run
