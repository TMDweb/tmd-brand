# TMD — The Marketing Department · Design System

> *Build to Grow together — in the same boat.*

TMD (**The Marketing Department**, a TTP company) builds tailored marketing departments for clients, **operates** them to drive results, and **seamlessly transfers** them back. The brand voice is partnership-first: TMD is on the same boat as the client.

This design system is the canonical source for TMD's visual language: typography, colors, layout, components, slide architecture, and the UI kits for the customer-facing surfaces.

---

## Sources & Inputs

The system was assembled from these uploads (originals preserved in `assets/`):

| Source | Stored at | Notes |
|---|---|---|
| `TMD Logo.svg` | `assets/TMD-logo.svg`, `assets/TMD-logo-dark.svg`, `assets/TMD-logo-white.svg` | Master logo. Dark/white variants generated for light/dark surfaces. |
| `IBMPlexSansArabic-Regular.ttf` | `fonts/IBMPlexSansArabic-Regular.ttf` | Brand font. Regular weight only was provided; other weights pulled via Google Fonts (see Type). |
| `TMD Color Palette.pdf` | `assets/TMD-color-palette.pdf` | Reference. Tokens transcribed in `colors_and_type.css`. |
| `TMD_Presentation_Master_Guidelines.txt` | `assets/TMD-presentation-guidelines.txt` | The authoritative rulebook for slides; followed exactly. |

> No codebase, Figma file, or live product was provided — the brand is currently expressed primarily through **slide decks** and the logo. This system therefore leans heavily on the slide master guidelines as the canonical visual reference, and the included UI kit is an extrapolation for a marketing site (see *Caveats* at bottom).

---

## Index — root manifest

| File / Folder | What it contains |
|---|---|
| `README.md` | This file. Start here. |
| `TMD-Brand-Identity.html` | **دليل الهوية الكامل** · 12 قسم، ملف واحد قابل للتحميل. افتح هذا أولاً. |
| `BRAND_RULES.md` | The strict, non-negotiable rules (R1–R8). |
| `TMD_BRAND_PROMPT.txt` | Ready-to-paste AI prompt for branded artifacts. |
| `colors_and_type.css` | Base + semantic CSS variables. `@import` or copy in. |
| `slides.css` | Shared slide foundation. Referenced by `Ar/` and `EN/` via `../slides.css`. |
| `deck-stage.js` | Web component for scalable decks. |
| `image-slot.js` | Drag-and-drop image placeholder component. |
| `assets/` | Logos, photos, color-palette PDF, brand-guidelines TXT, SAR symbol. |
| `fonts/` | IBM Plex Sans Arabic TTF. |
| `Ar/` | 19 RTL Arabic slide templates. |
| `EN/` | 19 LTR English slide templates. |

> Internal reference material (component previews, logo scratch, paste uploads, sample decks, earlier versions, agent skill spec) is stored **outside** this folder in `../internal/` and is **not** part of the published kit.

---

## Brand essence

TMD is a **partnership** brand, not a vendor brand. The phrase *"in the same boat"* is a literal positioning: TMD seats itself **inside** the client's team — build, operate, transfer.

Three verbs do all the lifting:

- **Build** — Stand up a marketing function from zero.
- **Operate** — Run it day-to-day, hit the numbers.
- **Transfer** — Hand it off cleanly so the client owns it.

Visually, this translates to a system that feels **deliberate, premium and quiet**: deep navy, soft creams, gold for emphasis, hard edges, no decoration. Marketing-agency flash is explicitly off-brand.

---

## CONTENT FUNDAMENTALS

**Voice.** Consultative, confident, partnership-driven. Always *we* with the client — never *us vs. them*. TMD positions itself as embedded.

- **Pronouns** — Prefer **we / our / together**. "You" is fine when addressing the client directly; avoid third-person ("the client", "users") in marketing copy.
- **Tone** — Plainspoken business English. No jargon, no marketing-agency hype words ("disruptive", "synergy", "rockstar"). No exclamation marks in body copy.
- **Casing** — **Title Case** for H1 (slide and section titles, marketing-site headlines). **Sentence case** for H2, H3, subtitles, breadcrumbs, body, and lists. **UPPERCASE** is reserved for short badges, page numbers, kickers, and the slide breadcrumb separator pipe. Product and service names always use Title Case.
- **Length** — Short. The Master Guidelines mandate *"fewer elements = better design"* and *"room to breathe."* Copy follows, one idea per line, max ~12 words per headline.
- **Punctuation** — **No em dashes (`—`) and no middle dots (`·`) between words in body copy.** Use **commas** to separate clauses. **Every body paragraph ends with a full stop.** The middle dot is permitted *only* inside breadcrumbs (`Section | Subsection`) and labels (`PHASE 02 · ACTIVE`), never inside running text.
- **Numbers** — Numerals always (never spelled out), even in body. Big stats get a unit caption underneath, and no `$` or `%` inside the number, let the unit carry it.
- **Emoji** — **Never.** TMD is a B2B partnership brand. Emoji are forbidden in all surfaces.
- **Unicode glyphs** — Only the vertical pipe `|` is permitted as a separator in breadcrumbs. No arrows (`←`, `→`), no bullets in headlines. Bulleted lists in body copy use plain disc bullets, not custom glyphs.
- **The boat metaphor** — Use sparingly. It anchors the *partnership* idea but loses force if hammered on every slide. Reserve for cover/intro/closing moments.

### Examples (in the right voice)

| ❌ Off-brand | ✅ On-brand |
|---|---|
| "We're revolutionizing marketing!" | "We build, operate, and transfer your marketing department." |
| "Synergize your growth strategy 🚀" | "Growth, built on shared ownership." |
| "Our team will help your team succeed." | "We're in the same boat." |
| "Q3 ROAS up 4.2x vs Q2 🎉" | "Q3 ROAS · 4.2× vs Q2" |

---

## VISUAL FOUNDATIONS

### Colors
Strictly enumerated — see `colors_and_type.css`. **14 colors total**, nothing else. Gradients are **forbidden**. Pure black is forbidden; use **TMD Dark `#0C0E1D`** instead. Primary Blue `#29366C` is allowed **only** on white backgrounds, never on dark.

**Core (4)** — `#0C0E1D`, `#ffffff`, `#29366C`, `#fcbf2c`

**Secondary · dark shades (4)**

| Role | Token | Hex |
|---|---|---|
| Blue · dark | `--tmd-blue-dark` | `#2f3e75` |
| Gold · dark | `--tmd-gold-dark` | `#dd9c03` |
| Red · dark | `--tmd-red-dark` | `#92112d` |
| Teal · dark | `--tmd-teal-dark` | `#33716b` |

**Secondary · light shades (4)**

| Role | Token | Hex |
|---|---|---|
| Blue · light | `--tmd-blue-light` | `#f0f2f9` |
| Gold · light | `--tmd-gold-light` | `#fff9eb` |
| Red · light | `--tmd-red-light` | `#fdedf0` |
| Teal · light | `--tmd-teal-light` | `#f1f9f8` |

**Extra (2)** — Section Number `#141B36`, Neutral Gray `#F2F2F2`

### Typography
**IBM Plex Sans Arabic** — strictly mandatory. No substitutions allowed (the guidelines are explicit on this). Latin glyphs render in IBM Plex Sans's Latin set, which keeps RTL/LTR consistent.

- **Cover/Section titles** — Bold, very large, tight tracking, tight leading.
- **Slide titles** — Bold, large, tight leading.
- **Body** — Regular, comfortable leading (1.5).
- **Stats** — Massive bold numbers, small unit caption underneath in a muted color.
- **Captions / footnotes / page numbers** — Extra small, medium weight, wide tracking.

### Spacing & Layout
- **0.5-inch safe margin** on every slide edge — equivalent to `--tmd-safe-margin: 48px`.
- **Generous whitespace** between sections. Minimalist. "Room to breathe" is doctrine.
- Slide content is **right-aligned for Arabic / RTL** (per the master guidelines: page number top-left, title top-right). For **English / LTR**, mirror the entire layout: **page number top-right, title top-left, footnote bottom-left**. The elements always sit on the *reading-start* edge.
- **Page numbers are the bare number** (e.g. `01`, never `01 / 12`). Sit on the top *trailing* edge inside the safe margin.
- **Footnotes sit in the bleed zone**, outside the 0.5-in safe margin, hugging the bottom *leading* edge. They are meta-data, not content.
- **Header architecture** has three permitted cases: (1) Main title only, (2) Main title + subtitle, (3) Breadcrumb + main title. No horizontal divider lines anywhere.

### Backgrounds
- **Solid only.** Pure `--tmd-white` or pure `--tmd-dark`. **No gradients. No imagery underneath text. No textures, no patterns, no noise.**
- Full-bleed photography is allowed *only* on cover/section divider slides if a real client photo is supplied; otherwise leave the dark navy solid.

### Borders, lines & dividers
- Hairline (`1px`) and thin (`2px`) only. Sharp.
- **Closely-spaced dashed lines** (1px dashed) are a signature TMD stroke. Used for: table internal gridlines (dark mode), comparison-card outlines, slide safe-margin guides, occasional decorative dividers. Always 1px, no thicker.
- A **6px gold accent line** is available as a generic divider element via `.tmd-accent-line`. **It is not used on the Cover slide** — the canonical Cover (T1) is logo + title + subtitle + version/date only. Source of truth: `slides/ArabicCoverSlide.html`.
- Tables in dark mode use **thin gold gridlines**; in light mode, alternating row fills replace gridlines.
- No drop shadows, no inner shadows, no glows. The brand reads as *flat geometric printwork*.

### Cards & containers
- **Stat cards** show only the big number and a short uppercase description below it in **bold Accent Gold** (`#FCBF2C`). No label above, no side rule, no background fill. The descriptive line tells the reader what the number measures.
- **Analytical text boxes** use an *extremely subtle* one-shade-deeper background + a thin accent line on one side. Heavy backgrounds are forbidden.
- **Comparison cards** — dark mode: `#2f3e75` thin borders, no fill. Light mode: `#f0f2f9` fill + `#F2F2F2` border.
- **Badges** — gold fill, dark text, small radius (2–4px).

### Corner radii
- Default: **2–4px**. TMD is sharp. Pills (`999px`) are reserved for small interactive chips. Big rounded `20px+` cards are off-brand.

### Hover & press states
The slide system is static, but for the marketing site UI kit the brand-consistent defaults are:
- **Hover** — small opacity drop on text links (to 80%); fill darken-by-10% on buttons (e.g. gold `#fcbf2c → #e8aa15`).
- **Press** — slight darken + 1px translateY downward. No scale.
- **Focus** — 2px gold outline offset 2px. Never use the OS default blue ring.

### Animation
Sparse and functional. The brand reads as printwork; motion should not dominate.
- **Easing** — `cubic-bezier(0.2, 0.7, 0.2, 1)` for entrances; linear for hover/state transitions.
- **Durations** — 200ms for state, 400ms for entrances. No bouncing, no overshoot, no parallax.
- **Fades** are preferred to slides; if sliding, ≤ 16px translate.

### Transparency & blur
Generally **avoid**. The brand's clarity comes from solid color contrast. The only exceptions:
- **Section-divider giant background number** at ~10% lightness (`#141B36` on `#0C0E1D`) — this is *one shade deeper*, not a transparency.
- Subtle dark-overlay on top of any client photography to ensure white text passes contrast.

### Imagery (when used)
- **Editorial / documentary** — real boats, real ports, real teams. Avoid stock-photo marketing tropes (handshakes, brainstorming, etc).
- **Color cast** — slightly cool, deep navy shadows, restrained saturation.
- B&W is acceptable for editorial portraits.
- No illustration system, no hand-drawn marks, no geometric clip-art.

---

## ICONOGRAPHY

TMD's source materials contain **no icon set**. The slide guidelines never reference iconography — the system is text-, color-, and number-driven. For decks, the strong recommendation is **no icons at all**: rely on numbers, badges, and the gold accent line for visual hierarchy.

For interface surfaces (the marketing site UI kit), we substitute **Lucide Icons** as the closest visual match: hairline stroke (`1.5px`), no fill, geometric, neutral. Lucide is loaded from CDN — see `ui_kits/marketing-site/index.html`. **This is a substitution and should be confirmed with the brand owner.** Once an official icon set is supplied, swap the CDN import.

**Rules in use**

- Icon stroke color must match text color (currentColor) — never gold inside icons.
- Icon size = body text size at 1× (20px), or h3 size at 1.4× for hero blocks.
- Gold (`#fcbf2c`) is for the *occasional* status indicator only — never a default icon fill.
- Emoji are forbidden everywhere.
- Unicode arrows (`→`, `←`) are forbidden in breadcrumbs; allowed inside body copy if absolutely necessary.

---

## Caveats & Open Questions

> **Action items for the brand owner — please review:**
>
> 1. **Font weights.** Only the `Regular` (400) weight of IBM Plex Sans Arabic was uploaded. Weights 300 / 500 / 600 / 700 are pulled from Google Fonts at runtime. If your licensed bundle has different metrics or you need offline fallback, please supply the additional TTFs and I'll wire them in.
> 2. **Iconography.** No icon set was provided. I'm using **Lucide** as a stand-in. Confirm or supply the official icon set.
> 3. **Photography.** No brand photo library was provided. The slides currently use solid colors only. If you have a photo library (especially the "boat" / "team" / "transfer" metaphor visuals), share and I'll integrate them.
> 4. **Product surfaces.** No website code, Figma file, or product screenshots were attached — only slide guidelines and a logo. The marketing-site UI kit is therefore a **speculative extrapolation** using the slide system's vocabulary. Please share any existing site/product files so I can ground the UI kit in real source.
> 5. **Arabic content.** The slide guidelines mandate strictly RTL (Arabic) content. The samples in `slides/` include both RTL Arabic and LTR English variants for flexibility, but the canonical brand expression is RTL — confirm preferred sample copy.
