# Repository Guidelines

## Project Structure & Module Organization
This repository is a lightweight GitHub profile presentation project.

- `README.md`: main profile content rendered on the GitHub profile page.
- `src/index.html`: static HTML prototype for a resume-style presentation.
- `images/`: local assets referenced by the profile, such as badges, headers, and icons.

Keep profile-facing content in `README.md`. Use `src/index.html` only for standalone experiments or alternate static layouts. Store new media in `images/` with descriptive filenames such as `profile-header.png`.

## Build, Test, and Development Commands
There is no build pipeline or package manager in this repository. Use simple local preview and git commands:

- `python3 -m http.server 8000`: serve the repo locally for quick checks.
- `open http://localhost:8000/src/index.html`: preview the static HTML page on macOS.
- `git status`: review working tree changes before committing.
- `git log --oneline -5`: inspect recent commit style.

Run the server from the repository root so image paths resolve correctly.

## Coding Style & Naming Conventions
Use Markdown for `README.md` and plain HTML for `src/index.html`.

- Indentation: 2 spaces in HTML.
- Filenames: use lowercase or clear PascalCase only when already established in `images/` (for example `GitHubHeader.png`).
- Prefer short sections, readable headings, and working links over decorative markup.
- Keep inline styles minimal; if `src/index.html` grows, move repeated styling into a dedicated stylesheet.

## Testing Guidelines
There is no automated test suite yet. Validate changes manually:

- open `README.md` in GitHub preview or a Markdown viewer
- load `src/index.html` through the local server
- verify all image paths and external links

Before submitting, check that new assets render correctly and that relative paths like `../images/...` still work.

## Commit & Pull Request Guidelines
Recent history uses short, imperative commit messages such as `Update README.md`. Follow that pattern:

- `Update README.md`
- `Add profile banner asset`
- `Fix broken image path in src/index.html`

Pull requests should include a concise summary, note any changed links or images, and attach a screenshot when modifying rendered profile content or layout.
