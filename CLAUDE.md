# CLAUDE.md — kiro-discussions

## Project overview

The community **ideas & suggestions** space for Kiro: a GitHub Discussions board
(`kirodubes/kiro-discussions`) plus a one-pager landing site on GitHub Pages
(`kirodubes.github.io/kiro-discussions/`). See [README.md](./README.md) for the
user-facing description.

## Current state

- One-pager `index.html` built from the shared Kiro web design system. The CSS
  (`css/style.css`) and the `KIRO:FOOTER` block are **propagated** from
  `Kiro-HQ/web-shared/` via `propagate-web-shared.sh` — do not hand-edit them;
  edit the canonical source and re-propagate.
- Repo features: Discussions **on**; Issues / Wiki / Projects / Actions **off**
  to keep the surface focused on discussion + the landing page.
- Board categories: Ideas, Polls, Show & tell, Q&A (+ Announcements, maintainer
  posts). Category management is web-UI only — GitHub doesn't expose it via API.

## Patterns & decisions

- Sibling of `kiro_repo` / `nemesis_repo` — same shell, same shared CSS, same
  cascaded footer. Copy is community-facing, not technical: every CTA funnels to
  the Discussions board.
- Respect-every-distro tone is deliberate (Guidelines section) — never position
  Kiro above what a visitor runs.
- Funding footer in the README is managed by `Kiro-HQ/cascade-readme-footer.sh`
  (`KIRO-FUNDING-FOOTER` markers).

## Next steps

- Cross-link a "Discuss / Ideas" nav item from kiro-website and the sibling sites.
- Seed a pinned welcome post in the Ideas category once live.
