# Architecture

Project Links is a single static page. There is no server code, build step, package manager or workflow.

## Components

| Path | Role |
|---|---|
| `index.html` | The whole site: markup and styles for the list of project links. |
| `.github/assets/` | Banner, logo and screenshot used by the README. |
| `LICENSE`, `NOTICE` | Apache-2.0 licence and attribution notice. |

## Data flow

1. A visitor's browser loads `index.html` from GitHub Pages.
2. The page renders the list of public project sites. Each entry is a plain link that opens the project's own site in a new tab.
3. Nothing is fetched at runtime: no API, no analytics script, no account.

## Build and deploy

- **Build:** none. The files in the repository are the files that are served.
- **Deploy:** GitHub Pages serves the repository at `https://mjyoke1111.github.io/links/`. A merged change to the published branch goes live on the next Pages publish.
- **Checks before merging:** preview locally with `python3 -m http.server`, click every link, and keep secrets and personal data out of commits.
