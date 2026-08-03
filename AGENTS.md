# Repository Guidelines

## Project Structure & Module Organization

This is a GitBook-style documentation site for Whostler Services. Content lives in two directories:

- `overview/` — service descriptions, setup guides (e.g., `dedicated-webserver-setup.md`)
- `profile/` — company profile and marketing content (`README.md`)

Root files: `README.md` (main entry), `SUMMARY.md` (navigation), `LICENSE`.

## Build, Test, and Development Commands

No build step is required — this is plain Markdown for GitBook.

- **Preview locally**: `npx gitbook serve` (requires Node.js)
- **Validate links**: `npx markdown-link-check README.md overview/*.md profile/*.md`
- **Lint Markdown**: `npx markdownlint-cli '**/*.md'`

## Coding Style & Naming Conventions

- **Indentation**: 2 spaces for nested lists, 4 spaces for code blocks
- **Headings**: ATX style (`#`, `##`, `###`); one H1 per file
- **File names**: kebab-case (`dedicated-webserver-setup.md`)
- **Links**: relative paths; anchor links use lowercase with hyphens (`#web-server-development`)
- **Emphasis**: `**bold**` for service names, `*italic*` for secondary terms

## Testing Guidelines

- Run link checker before commits: `npx markdown-link-check ...`
- Run markdownlint: `npx markdownlint-cli '**/*.md'`
- No automated test suite; manual review in GitBook preview is the gate

## Commit & Pull Request Guidelines

**Commit messages** (from history):
- Feature work: `Update README.md` (descriptive but concise)
- Structural: `GITBOOK-<n>: <subject>` for navigation/summary changes

**Pull requests**:
- Link to related issue or ticket
- Include GitBook preview screenshots for visual changes
- Ensure `SUMMARY.md` reflects new/removed pages
- Run link checker and markdownlint locally first
