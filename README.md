# The Scarlet Wood — Utopia TTRPG Campaign Hub

A GitHub Pages site for the Utopia TTRPG campaign "The Scarlet Wood".

- Player-facing content is published at your GitHub Pages URL.
- GM notes live in the repo and are intentionally not published.

## Repository structure

```
/                      # Jekyll site root
├─ _config.yml         # Jekyll config
├─ index.md            # Home page
├─ players.md          # Lists all player-facing articles
├─ _player/            # Collection: published player articles (Markdown)
│  └─ 0001-welcome.md
├─ _gm/                # Collection: GM notes — not published
│  └─ 0001-session-0-notes.md
├─ assets/images/      # Images for articles (use relative URLs)
├─ content-templates/  # Markdown templates for new articles
├─ .github/workflows/pages.yml  # GitHub Pages build + deploy
├─ .markdownlint.json  # Linting rules for Markdown
├─ .prettierrc         # Prettier formatting config
└─ .editorconfig       # Editor defaults
```

## Public vs private content

- Player content lives in `_player/` (published). It becomes available under `/players/<slug>/`.
- GM content lives in `_gm/` (private). The `_gm` collection is configured with `output: false` and excluded from the build, so it will not be deployed.

Important: If this repository is public, GM files are visible to anyone browsing the repo on GitHub. To keep GM notes truly private:
- Make the repository private; or
- Move `_gm/` into a separate private repository (e.g., as a Git submodule), or
- Keep GM notes in a private storage solution (not published).

## Local development (optional)

If you have Ruby/Jekyll installed:

```powershell
# From the repository root
bundle install ; bundle exec jekyll serve --livereload
```

Then open http://127.0.0.1:4000/ in your browser.

> If you don't have Ruby tooling, you can skip local builds and rely on GitHub Pages to build on push.

## Deploying with GitHub Pages

This repo includes a GitHub Actions workflow at `.github/workflows/pages.yml`.

1. Push to the `main` branch.
2. In GitHub, go to Settings → Pages:
   - Set "Source" to "GitHub Actions".
3. The workflow will build the site and deploy it to GitHub Pages.

## Writing content

- Use the templates in `content-templates/` for new articles.
- Player article location: `_player/my-article.md`
- GM article location: `_gm/my-private-notes.md` (will not be published)

### Front matter examples

Player article:

```yaml
---
layout: page
title: The Old Mill
summary: Rumors swirl about the wheel that never stops.
---
```

GM article (private):

```yaml
---
layout: page
title: The Old Mill — GM Notes
published: false
---
```

### Images

- Put images under `assets/images/`.
- Reference with a relative URL in Markdown:
  `![]({{ "/assets/images/filename.png" | relative_url }})`

## Markdown conventions

- Wrap lines at ~100 columns (enforced by `.markdownlint.json` and `.prettierrc`).
- Use ATX-style headings (`#`, `##`, etc.).
- One H1 per file that matches the title.
- Prefer fenced code blocks (```), backticks for inline code.
- Use ordered lists for steps, unordered lists for points.

Happy gaming in the Scarlet Wood!
