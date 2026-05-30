# Changelog — kiro-discussions

All notable changes to this repo are documented here, newest first.

## 2026.05.30

### What Changed

Created and launched the **kiro-discussions** community space — a GitHub
Discussions board plus a one-pager landing site, matching the look of the other
Kiro Pages sites (kiro_repo, nemesis_repo). The board is where users post ideas &
suggestions and upvote what they want built next; the landing page funnels people
into it and sets the community tone. Site is **live** at
https://kirodubes.github.io/kiro-discussions/.

### Technical Details

- One-pager `index.html` built from the shared Kiro web design system
  (`Kiro-HQ/web-shared/style.css` + the cascaded `KIRO:FOOTER` block via
  `propagate-web-shared.sh`, which now lists kiro-discussions as a third target).
  Reuses the existing shell: header with support pills + visitor-switchable accent
  swatches, hero, eyebrow/h2 sections, shared footer. No new CSS — only
  `pkg-grid`/`pkg-card`, `note`, and hero classes.
- Repo renamed `Discussions` → `kiro-discussions` (the auto-created name was
  capitalised; lowercase matches the sibling convention).
- GitHub Pages enabled (main / root). First build 404'd until Actions was
  re-enabled — Pages builds via the `pages-build-deployment` Actions workflow, so
  Actions can't be disabled on a Pages-serving repo.
- Repo features trimmed to keep the surface focused: Issues, Wiki, and Projects
  disabled; Discussions + Actions kept on. (Code / Security / Insights / Settings
  are structural GitHub tabs with no toggle — can't be hidden.)
- Pinned welcome discussion (#1) rewritten — title + body recast as a proper Kiro
  welcome (how it works, categories, house rules, respect-every-distro tone). Pin
  banner recolored from GitHub's default orange to a blue→violet gradient to match
  the Kiro accent palette.
- Discussion categories trimmed to **Ideas / Polls / Q&A / Show and tell /
  Announcements** (default **General** deleted) so the board matches the welcome
  post. Category management is web-UI only — GitHub exposes no API for it.
- Branding assets (favicons, logo) copied from the shared set.

### Files Modified

- `index.html` (new)
- `README.md` (new)
- `css/style.css` (new — copied from `Kiro-HQ/web-shared/`)
- `assets/branding/*` (new — shared Kiro branding)
- `CHANGELOG.md`, `CLAUDE.md` (new — scaffold)
