# TMD — Brand & Design System

**The Marketing Department** · هوية بصرية، نظام تصميم، قوالب شرائح، وبرومت جاهز للذكاء الاصطناعي.

> الملف الرئيسي للتصفّح: [`TMD-Brand-Identity.html`](./TMD-Brand-Identity.html) — افتحه في المتصفح لمشاهدة الدليل كاملًا.

---

## 🇸🇦 العربية

### ما هذا المستودع؟

نظام التصميم الرسمي والكامل لـ TMD. كل أصل، قاعدة، لون، خط، قالب، ومتغير CSS في مكان واحد قابل للنسخ والاستيراد.

### البنية

```
tmd-brand/
├── TMD-Brand-Identity.html     ← الدليل المتكامل القابل للتصفّح
├── README.md                   ← هذا الملف
├── BRAND_RULES.md              ← القواعد الثمانية الصارمة
├── TMD_BRAND_PROMPT.txt        ← برومت للذكاء الاصطناعي (ChatGPT/Claude/Gemini)
├── colors_and_type.css         ← متغيرات CSS جاهزة للاستيراد
├── fonts/                      ← IBM Plex Sans Arabic
├── assets/                     ← الشعارات، رمز الريال، الصور
└── slides/                     ← 19 قالب شريحة (LTR + RTL)
```

### الألوان · 14 لونًا فقط

**أساسية (4):**

| اللون | الـ Hex | الاستخدام |
|---|---|---|
| Official Dark | `#0C0E1D` | الخلفية الداكنة، بديل الأسود |
| White | `#ffffff` | الخلفية الفاتحة |
| Primary Blue | `#29366C` | على الأبيض فقط |
| Accent Gold | `#fcbf2c` | العناصر المميزة |

**ثانوية · غامقة (4):**

| اللون | الـ Hex |
|---|---|
| Blue Dark | `#2f3e75` |
| Gold Dark | `#dd9c03` |
| Red Dark | `#92112d` |
| Teal Dark | `#33716b` |

**ثانوية · فاتحة (4):**

| اللون | الـ Hex |
|---|---|
| Blue Light | `#f0f2f9` |
| Gold Light | `#fff9eb` |
| Red Light | `#fdedf0` |
| Teal Light | `#f1f9f8` |

**إضافية (2):** Section Number `#141B36` · Neutral Gray `#F2F2F2`

### الخط

**IBM Plex Sans Arabic** فقط، أوزان 300-700، بدون أي بدائل.
الخط متوفر في مجلد [`fonts/`](./fonts/) وأيضًا على Google Fonts.

### الاستخدام السريع

#### في موقع ويب

```html
<link rel="stylesheet" href="https://raw.githubusercontent.com/TMDweb/tmd-brand/main/colors_and_type.css">
```

ثم استخدم المتغيرات:

```css
.heading {
  color: var(--tmd-blue);
  font-family: var(--tmd-font);
  font-size: var(--tmd-size-h1);
}
```

#### مع الذكاء الاصطناعي

انسخ محتوى [`TMD_BRAND_PROMPT.txt`](./TMD_BRAND_PROMPT.txt) كاملًا والصقه كتعليمات نظام (system prompt) قبل طلبك.

### القواعد الثمانية (لا تُكسر)

تفاصيلها في [`BRAND_RULES.md`](./BRAND_RULES.md):

1. **الاتجاه** — العربي RTL، الإنجليزي LTR. لا خلط.
2. **التباعد** — `letter-spacing: normal` دائمًا.
3. **علامات الطباعة** — ممنوع الشرطة الطويلة (—) والاقتباس المنحني.
4. **بدون عمق** — لا ظلال، لا تدرّجات، لا blur.
5. **زوايا حادة** — radius من 0 إلى 4px.
6. **بدون إيموجي** — مطلقًا.
7. **رمز الريال** — SVG الرسمي فقط.
8. **الأرقام** — الإفرنجية فقط (0–9).

---

## 🇬🇧 English

### What is this?

The complete official design system for TMD — every asset, rule, color, font, template, and CSS variable in one importable place.

### Structure

See [the Arabic section above](#-العربية) — the same files apply.

### Color System · 14 colors only

**Core (4):** `#0C0E1D` · `#ffffff` · `#29366C` · `#fcbf2c`

**Secondary Dark (4):** `#2f3e75` · `#dd9c03` · `#92112d` · `#33716b`

**Secondary Light (4):** `#f0f2f9` · `#fff9eb` · `#fdedf0` · `#f1f9f8`

**Extra (2):** `#141B36` · `#F2F2F2`

### Typography

**IBM Plex Sans Arabic** only — weights 300–700. No substitutes.
Bundled in [`fonts/`](./fonts/), also available on Google Fonts.

### Quick start

#### In a website

```html
<link rel="stylesheet" href="https://raw.githubusercontent.com/TMDweb/tmd-brand/main/colors_and_type.css">
```

Then use the tokens:

```css
.heading {
  color: var(--tmd-blue);
  font-family: var(--tmd-font);
  font-size: var(--tmd-size-h1);
}
```

#### With AI platforms

Copy the entire content of [`TMD_BRAND_PROMPT.txt`](./TMD_BRAND_PROMPT.txt) and paste it as a system instruction before your request.

### The 8 non-negotiable rules

See [`BRAND_RULES.md`](./BRAND_RULES.md) for full detail:

1. **Direction** — Arabic = RTL, English = LTR. Never mixed.
2. **Spacing** — `letter-spacing: normal` always.
3. **Type marks** — No em-dash (—), no curly quotes.
4. **No depth** — No shadows, no gradients, no blur.
5. **Sharp corners** — Radius 0–4px max.
6. **No emoji** — Ever.
7. **Saudi Riyal** — Official SVG glyph only.
8. **Numerals** — Western Arabic numerals only (0–9).

---

## 📦 Direct asset URLs

After this repo is published as public, all assets are accessible via:

```
https://raw.githubusercontent.com/TMDweb/tmd-brand/main/<path>
```

Examples:

- **Logo (default):** `assets/TMD-logo.svg`
- **Logo (on dark bg):** `assets/TMD-logo-white.svg`
- **Logo (on gold bg):** `assets/TMD-logo-dark.svg`
- **SAR currency glyph:** `assets/SAR-symbol.svg`
- **Font:** `fonts/IBMPlexSansArabic-Regular.ttf`
- **CSS tokens:** `colors_and_type.css`
- **AI prompt:** `TMD_BRAND_PROMPT.txt`

---

## License

© TMD · The Marketing Department · A TTP Company. All rights reserved.
