# Classic Serif Personal Homepage — Design Spec

**Date:** 2026-07-13
**Owner:** Xiangwen (Wayne) Yang
**Repo:** `chnyangs/chnyangs.github.io` (GitHub Pages, Jekyll)
**Status:** Approved (in-chat) — implementation on branch `classic-serif-redesign`

## Goal

Redesign the personal GitHub Pages site into a **classic serif document** aesthetic —
timeless, formal, understated, like a finely typeset printed CV / journal article.
Replace the current bare README-as-homepage and the flashy purple-gradient publications
page with a consistent, restrained serif design.

## Locked decisions

| Decision | Choice |
|----------|--------|
| Visual style | Classic serif document (EB Garamond, fallback `Georgia, "Times New Roman", serif`) |
| Structure | Home page (`index.html`) + separate Publications page (`publication/overview.md`), both restyled consistently |
| Palette | Ivory background `#FBF7EF` · body text `#1a1a1a` · maroon links `#7B1E1E` · hairline rules `#E4D8C8` |
| Color mode | Light only (no dark mode) |
| Local preview | Add `Gemfile` (github-pages gem + webrick) so `bundle exec jekyll serve` works |

## Architecture

Jekyll / GitHub Pages. Files:

- **`_layouts/default.html`** — shared classic-serif base layout. Centered single column
  (max-width ≈ 760px), header photo/identity block, minimal top nav (Home · Publications),
  footer. Links one shared stylesheet. Renders `{{ content }}`.
- **`assets/css/main.css`** — all styling in one shared file (DRY). No per-page inline
  `<style>` blocks (removes the duplicated-CSS smell of the current pages).
- **`index.html`** — homepage, `layout: default`. Sections in order:
  Header (photo + name + title + location + contact links: email · LinkedIn · Scholar · GitHub)
  → About (Summary) → Highlights → Professional Experience → Selected Projects
  → Technical Skills → Selected Publications (a few, + "All publications →" link)
  → Education.
  Content migrated from current `README.md`.
- **`publication/overview.md`** — full publications list, `layout: default`, restyled to the
  same serif system. Grouped by year. Remove purple gradient, hover-lift cards, FontAwesome
  chrome. Venue shown as a small understated tag/italic; links in maroon.
- **`Gemfile`** (+ `Gemfile.lock`) — enables faithful local preview. Already excluded from the
  build in `_config.yml`.

## Visual system

- **Typography:** EB Garamond body; section headers in small-caps with a hairline rule above,
  generous letter-spacing — classic CV sectioning. System serif fallback so the page is
  readable before/without the web font.
- **Palette:** as in Locked decisions. Body black on ivory; maroon only for links/accents;
  hairline rules for separation instead of boxes/shadows.
- **Layout:** single centered column, line-height ~1.6, ample whitespace between sections.
  Photo square / lightly rounded corners (not a large circular avatar).
- **Responsive:** on narrow screens the header photo and identity stack; type scale and
  margins tighten. Body must never scroll horizontally.

## Non-goals (YAGNI)

- No gradients, floating cards, box-shadow stacks, or hover animations.
- No JS framework; keep it static. Optional tiny native-JS niceties (e.g. abstract toggle)
  are out of scope for v1.
- No dark mode.
- No unrelated refactor of `_config.yml` collections beyond what the redesign needs.

## Content source note

`README.md` stays as the GitHub **repository** landing page. The **website** homepage becomes
`index.html` with full styling control. Content is migrated (some duplication is acceptable —
different audiences). Long-term sync between the two is out of scope for v1.

## Verification

1. `bundle install` then `bundle exec jekyll serve`; site builds without errors.
2. Load `/` and `/publications/` at `http://127.0.0.1:4000`; verify layout, links, section
   hierarchy, and responsive behavior (narrow viewport).
3. Screenshot both pages to confirm the classic-serif look before delivery.
4. All external links (email, LinkedIn, Scholar, GitHub, paper PDFs) resolve to correct URLs.

## Delivery

Work on branch `classic-serif-redesign`. After live-render verification, present to user for
review, then merge to `main` (which auto-deploys via GitHub Pages).
