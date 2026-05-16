# TMD — Strict Brand Rules

These rules are MANDATORY for every asset produced in this project.
Full reference, including the AI-platform prompt, lives in
[`TMD_BRAND_PROMPT.txt`](TMD_BRAND_PROMPT.txt).

## R1 · Direction
- Arabic content → entire layout is **RTL** (`dir="rtl"`), every element mirrored.
- English content → entire layout is **LTR** (`dir="ltr"`).
- Never mix directions in one document.

## R2 · Character Spacing
- `letter-spacing: normal` (0) on every element, always. No "tight", no "loose".
- Enforced globally by `colors_and_type.css` via a `*` override.

## R3 · Typography Marks
- Em-dash (—) is **forbidden** anywhere — including as a list marker. Use a small rectangular pseudo-element marker, a period, comma, colon, line break, or hyphen-minus.
- Straight double quotes only (`"`). No curly quotes.
- Ellipsis: `...` (three periods), not the single glyph.

## R4 · No Depth, No Gradients
- No shadows, no glows, no blur, no decorative gradients. Solid fills + lines only.
- A dark-to-transparent veil over photos for legibility is allowed.

## R5 · Geometry
- Radii: 0 (sharp) or 2–4px max. No pill shapes. Rings and percentage dials use circular SVG, not rounded rectangles.

## R6 · Emoji
- Never. In any asset.

## R7 · Saudi Riyal
- For SAR amounts, use the official SAR glyph SVG (`assets/SAR-symbol.svg`).
- Render it inline with `width="1em" height="1em" fill="currentColor"`.
- LTR: glyph **before** the number. RTL: glyph **after** the number.
- Forbidden: "SAR", "SR", "ر.س", "﷼", any text abbreviation.

## R8 · Numerals
- Always use Western Arabic numerals: **0 1 2 3 4 5 6 7 8 9**.
- **Never** use Eastern Arabic-Indic numerals (٠ ١ ٢ ٣ ٤ ٥ ٦ ٧ ٨ ٩), not even inside fully Arabic copy.
- Applies to: page numbers, section numbers, statistics, dates, percentages, decimals, ordinals, currency amounts, phone numbers, version numbers.
- Forbidden Unicode block in output: `U+0660`–`U+0669`.

## Sizes & Colors (quick reference)
- Slide canvas: **33.867 cm × 19.05 cm** (1280 × 720 px @ 96 dpi).
- Slide title: **28 pt** Bold. Subtitle / breadcrumb: **18 pt** Medium.
- Subtitle on light slide: `#29366C`. Subtitle on dark slide: `#FCBF2C`.
- Primary Blue `#29366C` is **only** on white backgrounds.

## Template library (LTR + RTL pairs)

Each template has both an English (LTR) and Arabic (RTL) file.

| # | Template | File pair |
|---|---|---|
| T1 | Cover | `CoverSlide.html` / `ArabicCoverSlide.html` |
| T2 | Section Divider | `SectionDividerSlide.html` / `ArabicSectionDividerSlide.html` |
| T3 | Agenda · Table of Contents | `AgendaSlide.html` / `ArabicAgendaSlide.html` |
| T4 | Content Light (3 columns) | `ContentLightSlide.html` / `ArabicContentLightSlide.html` |
| T5 | Content Dark (breadcrumb + lede) | `ContentDarkSlide.html` / `ArabicContentDarkSlide.html` |
| T6 | Stats (3 large numbers) | `StatsSlide.html` / `ArabicStatsSlide.html` |
| T7 | Comparison | `ComparisonSlide.html` / `ArabicComparisonSlide.html` |
| T8 | Tables (light + dark) | inline in component preview |
| T9 | Timeline (year markers) | `TimelineSlide.html` / `ArabicTimelineSlide.html` |
| T10 | Stat Grid (4 ring charts) | `StatGridSlide.html` / `ArabicStatGridSlide.html` |
| T11 | Phase Chevrons | `NumberedRowsSlide.html` / `ArabicNumberedRowsSlide.html` |
| T12 | Process Steps (4 sequential) | `ProcessStepsSlide.html` / `ArabicProcessStepsSlide.html` |
| T13 | Pros vs Cons | `ProsConsSlide.html` / `ArabicProsConsSlide.html` |
| T14 | Profile Card (partner snapshot) | `ProfileCardSlide.html` / `ArabicProfileCardSlide.html` |
| T15 | Photo Hero (full-bleed) | `PhotoHeroSlide.html` / `ArabicPhotoHeroSlide.html` |
| T16 | Photo Split (50 / 50) | `PhotoSplitSlide.html` / `ArabicPhotoSplitSlide.html` |
| T17 | Photo Grid (3 × 2) | `PhotoGridSlide.html` / `ArabicPhotoGridSlide.html` |
| T18 | Photo with Stat | `PhotoStatSlide.html` / `ArabicPhotoStatSlide.html` |
| T19 | Photo Quote | `PhotoQuoteSlide.html` / `ArabicPhotoQuoteSlide.html` |

See `colors_and_type.css` for the full token set and `slides/slides.css` for the shared slide foundation (page number, header sizes, footnote, RTL mirroring).
