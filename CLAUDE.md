# CLAUDE.md — a module of the Interactive Pathology Teaching Platform

This repository is one module (a single `index.html`). The platform's decisions, the checklist for modules, the
deployment steps, the testing workflow and the lessons learned are in the platform repository:
`third-year-med/Interactive-pathology-platform` → `CLAUDE.md` and `docs/HANDBOOK.md` (rebuilds: `docs/REBUILD.md`).

- The course data in `index.html` is encrypted; the content key lives only in the user's Code.gs. Never commit a key or
  an unencrypted copy of the course.
- The `<script id="platform-nav">` block is maintained in the platform repo (`modules/platform-nav.js`) and written here
  with `tools/module-release.js refresh` — do not edit it by hand.
- A new build goes through the preview / compatibility check / go-live procedure (`docs/REBUILD.md`) and must keep the
  IDs of continuing topics, sections, questions, cases and images.
- Test changes on the real page with the platform repo's e2e tests before pushing.
