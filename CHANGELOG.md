# Changelog — kiro-discussions

All notable changes to this repo are documented here, newest first.

## 2026.05.30

### What Changed

Created the **kiro-discussions** community space — a GitHub Discussions board
plus a one-pager landing site, matching the look of the other Kiro Pages sites
(kiro_repo, nemesis_repo). The board is where users post ideas & suggestions and
upvote what they want built next; the landing page funnels people into it and
sets the community tone.

### Technical Details

- One-pager `index.html` built from the shared Kiro web design system
  (`Kiro-HQ/web-shared/style.css` + the cascaded `KIRO:FOOTER` block via
  `propagate-web-shared.sh`). Reuses the existing shell: header with support
  pills + visitor-switchable accent swatches, hero, eyebrow/h2 sections, shared
  footer. No new CSS — only `pkg-grid`/`pkg-card`, `note`, and hero classes.
- Repo features trimmed to keep the surface focused: Issues, Wiki, and Projects
  disabled; Discussions kept on. Actions stays enabled — the GitHub Pages
  `pages-build-deployment` workflow needs it, so it can't be hidden on a repo
  that serves a Pages site.
- Branding assets (favicons, logo) copied from the shared set.

### Files Modified

- `index.html` (new)
- `README.md` (new)
- `css/style.css` (new — copied from `Kiro-HQ/web-shared/`)
- `assets/branding/*` (new — shared Kiro branding)
- `CHANGELOG.md`, `CLAUDE.md` (new — scaffold)
