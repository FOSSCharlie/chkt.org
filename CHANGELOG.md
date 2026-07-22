# Changelog

All notable changes to the chkt.org landing page are documented in this file.

## 2026-07-22

### Changed
- Removed all Google Fonts dependency — no more requests to
  `fonts.googleapis.com` / `fonts.gstatic.com`. The Inter typeface is
  now self-hosted: downloaded directly from its official source
  ([rsms/inter](https://github.com/rsms/inter) on GitHub, SIL Open
  Font License) and embedded directly in `index.html` as base64, so
  the page has zero external font requests of any kind.
- Inter is now used for both headings and body text everywhere on
  the page (previously headings used a separate display face pulled
  from Google Fonts). Date badges and the code block remain on the
  system monospace stack, since that's a distinct fixed-width role
  Inter doesn't cover.
- Note: this increases the page size to ~950KB (previously ~35KB),
  entirely due to the embedded font file. It's a one-time load per
  visit with no external dependency, but if page weight matters more
  than eliminating every external request, hosting the font as a
  separate `.woff2` file alongside `index.html` (rather than inlined)
  would reduce this while still avoiding Google entirely.

## 2026-07-21

### Changed
- Hero hint text below the live demo enlarged, with "This is not a
  screenshot." set on its own bold line, followed by "It is the real
  interface, live, try it for yourself. Add a task, check one off,
  click the red dot." on a second line — makes it unmistakable that
  the demo is fully interactive rather than a static image.
- Hero tagline shortened from "A stupidly simple todo list, sorted by
  due date." to "A stupidly simple todo list."

### Fixed
- Live demo rebuilt to faithfully mirror the real app's interface:
  - Tasks now render as individual rounded cards with a colored left
    border by urgency (red/orange/yellow), matching the real app
    exactly, instead of a flat divided list.
  - Due-date badge text now uses the same logic as the app itself
    (e.g. "3d overdue · Sat 18 Jul", "Due today · ...", "Due
    tomorrow · ..."), computed from the visitor's actual current date
    so it never goes stale.
  - Added a working "what needs to be done?" add-task row above the
    list, matching the real app's layout.
  - Added a "Completed (n)" section with the real completed-badge
    format ("Completed [date] · was due [date]").
  - Checkbox and delete-dot styling corrected to the app's exact
    colors and dimensions (previously drifted during the visual
    redesign: overdue/today badge colors, checkbox radius, dot glow).

## Initial launch

### Added
- First version of the "modern" landing page: dark aurora-gradient
  background, glassmorphic hero card containing a live interactive
  checklist demo, bento-style feature grid, "Get started" section
  with Docker install steps, and a footer matching the app's own
  style.
