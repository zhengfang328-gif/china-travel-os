---
name: China Travel OS
description: Modern China travel explained — honest, insider knowledge for first-time travelers
colors:
  accent-red: "#D94838"
  accent-red-deep: "#B8382A"
  accent-red-soft: "#FDF0ED"
  neutral-bg: "#FAFAFA"
  neutral-surface: "#FFFFFF"
  neutral-ink: "#1C1614"
  neutral-ink-sub: "#5A4D49"
  neutral-ink-faint: "#968883"
  neutral-border: "#E6E0DD"
  neutral-border-light: "#F2EFED"
  tint-peach: "#FFF3EB"
  tint-sky: "#EEF4FB"
  tint-lavender: "#F3EFF9"
  tint-mint: "#EBF7EF"
  tint-yellow: "#FFFCF0"
  tint-cream: "#FAF7F2"
  tint-stone: "#F6F3F1"
typography:
  display:
    fontFamily: "Literata, Georgia, Times New Roman, serif"
    fontSize: "clamp(2.5rem, 6vw, 4.5rem)"
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: "-0.015em"
  heading:
    fontFamily: "Literata, Georgia, Times New Roman, serif"
    fontSize: "clamp(1.75rem, 4vw, 2.5rem)"
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Work Sans, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "Work Sans, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 700
    letterSpacing: "0.06em"
rounded:
  sm: "10px"
  lg: "16px"
  pill: "999px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "32px"
  2xl: "48px"
  3xl: "64px"
  4xl: "96px"
components:
  button-primary:
    backgroundColor: "{colors.accent-red}"
    textColor: "#FFFFFF"
    rounded: "{rounded.pill}"
    padding: "13px 26px"
  button-primary-hover:
    backgroundColor: "{colors.accent-red-deep}"
  button-outline:
    backgroundColor: "transparent"
    textColor: "{colors.neutral-ink}"
    rounded: "{rounded.pill}"
    padding: "13px 26px"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.neutral-ink-sub}"
    rounded: "{rounded.pill}"
    padding: "13px 26px"
---

# Design System: China Travel OS

## 1. Overview

**Creative North Star: "The Field Notebook"**

China Travel OS looks like a well-kept traveler's notebook: honest, lived-in, organized with care but never precious. Every visual choice serves one goal — getting the reader to the answer as directly as possible, with warmth that comes from the voice and the details, not from decorative styling.

The palette is built around a single committed red (`#D94838`), used boldly on the newsletter block and buttons, whisper-quiet everywhere else. The neutrals are chroma-zero off-white and tint-shifted grays that lean imperceptibly toward warm-red — never reading as cream or sand. The typography pairs a literary serif for headings (Literata) with a humanist sans for body (Work Sans), creating hierarchy through scale and weight contrast without resorting to all-caps eyebrow labels above every section.

This system explicitly rejects: Chinese cultural motifs and red-lantern ornament, SaaS landing-page clichés (gradient buttons, hero-metric templates, "streamline/empower" vocabulary), AI-generated marketing cadences (aphoristic negation, em-dash overuse, identical card grids), and encyclopedic guidebook density.

**Key Characteristics:**
- Single committed accent color carrying 30–60% of visible surface
- Border-based depth hierarchy — no shadows except on city card hover
- Serif headings + sans body with ≥1.25 scale ratio between steps
- Flat backgrounds, chroma-neutral off-white, no warm-cream tint
- Section labels used exactly once (Anxiety zone), not as site-wide scaffolding
- All motion respects `prefers-reduced-motion` and uses targeted transitions only

## 2. Colors

A committed palette: one saturated red accent paired with a disciplined neutral ramp where every gray is tinted toward the brand hue (12°) at barely-perceptible chroma (0.002–0.005). Nothing reads as pure gray. Nothing reads as cream.

### Primary
- **Accent Red** (`#D94838`): The voice of the brand. Used on primary buttons, the newsletter CTA block background, links, and the logo dot. Carries 30–60% of surface area per the Committed strategy.
- **Accent Red Deep** (`#B8382A`): Hover state for primary buttons and links. Darker by roughly one perceptual step.
- **Accent Red Soft** (`#FDF0ED`): Tinted background for callouts, essential badges, and the hero gradient top. The accent at its quietest.

### Neutral
- **Neutral BG** (`#FAFAFA`): Page background. Chroma-zero off-white — not cream, not sand, not warm paper. True neutral.
- **Neutral Surface** (`#FFFFFF`): Card and nav backgrounds. Pure white for maximum contrast against the off-white page.
- **Neutral Ink** (`#1C1614`): Primary body text. Near-black tinted toward red — warmer than pure black, readable at all sizes. Contrast ratio ≥12:1 against `#FAFAFA`.
- **Neutral Ink Sub** (`#5A4D49`): Secondary text, descriptions, metadata. Reduced contrast for hierarchy.
- **Neutral Ink Faint** (`#968883`): Tertiary text, footnotes, disabled states. Lowest contrast still passing AA for small text (≥4.5:1 against white).
- **Neutral Border** (`#E6E0DD`): Active borders, card edges on hover, section dividers.
- **Neutral Border Light** (`#F2EFED`): Default card borders, nav bottom edge. Barely visible — more texture than line.

### Category Tints
Seven pastel tints for guide category cards and content labeling. Each is a near-white with a whisper of hue — used as surface backgrounds only, never as text colors.
- **Tint Peach** (`#FFF3EB`): Payments category
- **Tint Sky** (`#EEF4FB`): Internet / VPN category
- **Tint Lavender** (`#F3EFF9`): Apps category
- **Tint Mint** (`#EBF7EF`): Transport category
- **Tint Yellow** (`#FFFCF0`): Checklist / preparation
- **Tint Cream** (`#FAF7F2`): General / miscellaneous
- **Tint Stone** (`#F6F3F1`): Safety / practical

### Named Rules

**The No-Pure-Gray Rule.** Every neutral on the site is tinted toward the brand red hue. If a gray reads as purely achromatic, it's wrong. The shift is barely perceptible (0.002–0.005 chroma) — it should feel natural, not colored.

**The Committed Red Rule.** Brand red is not an accent sprinkle; it's a structural color. The newsletter block, primary buttons, links, and logo all use it. Together they occupy 30–60% of the visible surface on any given scroll. If the page looks grayscale with occasional red dots, the saturation is too low.

**The Not-Cream Rule.** The body background (`#FAFAFA`) is chroma-zero off-white. It must never drift into warm-neutral territory (cream, sand, parchment, ivory). If it looks like paper aged in a drawer, it's wrong.

## 3. Typography

**Display Font:** Literata (with Georgia, Times New Roman fallback)
**Body Font:** Work Sans (with -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif fallback)

**Character:** A literary serif built for screens paired with a humanist sans that's warm without being soft. Literata brings editorial weight to headings; Work Sans keeps body text approachable and highly readable at small sizes. The pairing works because the fonts sit on opposite sides of the serif/sans axis — they contrast rather than compete.

### Hierarchy
- **Display** (Literata, 700, clamp(2.5rem, 6vw, 4.5rem), 1.15): Hero headlines only. Italic variant used for emphasis words in accent red with underline. Letter-spacing tightened to −0.015em.
- **Heading** (Literata, 600, clamp(1.75rem, 4vw, 2.5rem), 1.15): Section titles (h2). Letter-spacing −0.01em. No eyebrow label above — the heading carries meaning alone.
- **Title** (Literata, 600, 1.375rem, 1.3): Article h2 and guide category headings. Slightly reduced weight for body-context headings.
- **Body** (Work Sans, 400, 1rem, 1.6–1.7): Primary reading text. Line length capped at 65–75ch via max-width containers. Article body uses 1.7 line-height; UI contexts use 1.6.
- **Label** (Work Sans, 700, 0.75rem, uppercase, 0.06em): The section eyebrow. Used exactly once site-wide — in the Anxiety zone ("DON'T LET THESE STOP YOU"). Also used for footer column headings and essential badges.

### Named Rules

**The One Eyebrow Rule.** The `.section-label` (small uppercase tracked label) appears in exactly one place: the Anxiety section on the homepage. Every other section lets its h2 carry meaning without a kicker. If you find yourself adding a second eyebrow, delete it.

**The Scale-Step Rule.** Every step in the type scale is at least 1.25× the previous: 0.75 → 0.875 → 1 → 1.125 → 1.375 → 1.75 → 2.25 → 2.875 rem. No two adjacent sizes are closer than 1.25:1.

## 4. Elevation

This is a flat system. Depth is conveyed through borders and background color shifts, not shadows. The design language treats the page as a single plane with differentiated zones — lighter cards on a slightly darker background, separated by 1px hairline borders.

The sole exception: city cards gain a hover shadow (`0 12px 40px rgba(0,0,0,.18)`) combined with a 3px upward translate. This is the only shadow in the entire system, and it's reserved for the one element type that benefits from a "lifting off the page" affordance.

### Shadow Vocabulary
- **City card hover** (`box-shadow: 0 12px 40px rgba(0,0,0,0.18)`): Applied only on `:hover` to city cards. Combined with `transform: translateY(-3px)`. Disabled under `prefers-reduced-motion`.

### Named Rules

**The Flat-By-Default Rule.** Surfaces are flat at rest. If an element needs depth, use a border or a background-color shift. Never use `box-shadow` as decoration — the one city-card exception proves the rule by being conspicuously special.

**The Border-Not-Shadow Rule.** Cards, nav, and sections are separated by `1px solid` borders in `--border-light` (`#F2EFED`). A 1px border and a soft wide shadow on the same element is prohibited. Pick the border.

## 5. Components

### Buttons

Warm and approachable: fully rounded pill shapes, confident hover feedback with a 1px lift, targeted transitions on background-color and transform only.

- **Shape:** Fully rounded pill (`border-radius: 999px`).
- **Primary:** `background: #D94838; color: #fff; padding: 13px 26px`. Hover darkens to `#B8382A` and lifts 1px. CTA placement in hero and newsletter.
- **Outline:** Transparent background, `1.5px solid` border in `#E6E0DD`, text in `#1C1614`. Hover shifts border to `#D94838` and text to `#D94838`.
- **Ghost:** Transparent background, `1.5px solid` border in `#F2EFED`, text in `#5A4D49`. Hover shifts border to `#E6E0DD` and text to `#1C1614`. Used for secondary actions.
- **Teal variant:** `background: #0D9488` with hover `#0F766E`. Reserved for VPN/eSIM CTAs where a distinct color signals a different action category (connectivity). For inline text emphasis and badges on teal-tinted backgrounds (`#F0FDF9`), use `#0F766E` for AA contrast compliance (~5.2:1).
- **Transitions:** `background-color`, `color`, and `transform` only. 200ms, `cubic-bezier(0.4, 0, 0, 1)`. Never `transition: all`.

### Navigation

Solid white bar, sticky. No glassmorphism, no backdrop-filter.

- **Bar:** `position: sticky; background: #FFFFFF; border-bottom: 1px solid #F2EFED; height: 64px`.
- **Logo:** Literata 700, 20px, letter-spacing −0.01em. The "Travel" segment is in accent red.
- **Links:** Work Sans 500, 0.875rem, color `#5A4D49`. Hover shifts to `#1C1614`.
- **Mobile:** Hamburger toggle reveals full-width dropdown below the nav bar. Same solid white background, border-bottom separator.

### Cards

Three card families, each with a distinct role:

- **Anxiety cards:** White surface, 1px `#F2EFED` border, 16px radius. 24px horizontal padding. Emoji icon in a 52×52px rounded square with `#F2EFED` background. Hover: border shifts to `#E6E0DD`, background to `#F8F6F5`. Link text reveals accent hover color. No shadow. Soon/disabled variants at 0.5 opacity.
- **Guide items:** Transparent background, 10px radius, list-item layout with icon + text + arrow. Hover: background shifts to `#F8F6F5`, border appears (1px `#F2EFED`). Arrow slides right 3px and turns accent red.
- **City cards:** Solid dark color background (no gradient — flat color + radial gradient pseudo-element for light source at 30%/20%, 8% white at center). White text. 360px min-height. 16px radius. Hover: lifts 3px with `0 12px 40px rgba(0,0,0,.18)` shadow. Gradient overlay via `::before` for text readability. "Explore →" text fades in on hover.

### Callouts

Full border, never a left-side stripe.

- **Style:** `1px solid` border in `#E6E0DD`, background in `#FDF0ED` (accent-muted), 16px radius, 24px padding.
- **Teal variant:** Same structure with `border-color: #99F6E4; background: #F0FDFA` for connectivity-related callouts.
- **Typography:** Body text in Work Sans, links underlined in accent red.
- **Anti-pattern:** `border-left: 4px solid` is forbidden. Always use the full 4-side border.

### Inputs (Newsletter form)

- **Style:** Pill radius, dark field on red background. `background: rgba(255,255,255,0.1); border: 1.5px solid rgba(255,255,255,0.25); color: #fff`. Placeholder at 50% white opacity.
- **Focus:** Border shifts to 50% white opacity.
- **Error:** Border shifts to `#FECACA`, background to `rgba(255,100,100,0.15)`.
- **Button:** White background with accent red text, 700 weight. Hover: `#F5F0EE` background.

### Social Proof Items

- **Layout:** Centered icon (40px emoji) + heading + description in a grid.
- **Typography:** Heading in Work Sans 600, 1rem. Description in Work Sans, `#5A4D49`, 0.875rem.

### Footer

- **Brand:** Literata 700, 20px. "Travel" segment in accent red.
- **Column headings:** Work Sans 700, 0.75rem, uppercase, 0.04em letter-spacing, color `#968883`.
- **Links:** Work Sans, 0.875rem, `#5A4D49`. Hover shifts to `#1C1614`.
- **Separators:** `1px solid #F2EFED` border-top on footer-bottom.

## 6. Do's and Don'ts

### Do:
- **Do** use the single brand red (`#D94838`) for buttons, links, the newsletter block, and the logo accent. It's committed, not sprinkled.
- **Do** differentiate surfaces with 1px borders (`#F2EFED` / `#E6E0DD`), not shadows.
- **Do** pair Literata headings with Work Sans body text. The serif/sans contrast is the hierarchy engine.
- **Do** use `cubic-bezier(0.4, 0, 0, 1)` for all interactive transitions. Target specific properties — never `transition: all`.
- **Do** wrap every animation and transition in `@media (prefers-reduced-motion: reduce)` with instant or near-instant alternatives.
- **Do** use `text-wrap: balance` on all h1–h3 elements.
- **Do** fill transparent PNG areas with `#FAFAFA` before placing on the page — images must read as part of the surface.
- **Do** put text descriptions above their corresponding screenshots in guide articles.

### Don't:
- **Don't** use Chinese cultural motifs, red lanterns, gold accents, or ornate decoration. This is not a tourism bureau site.
- **Don't** use SaaS landing-page clichés: gradient buttons, hero-metric templates (big number + small label), "streamline/empower/supercharge" vocabulary.
- **Don't** use AI-generated marketing cadences: aphoristic negation ("No fluff. Just results."), em-dash overuse, identical card grids repeated across sections.
- **Don't** use encyclopedic Lonely Planet / WikiTravel density with nested categories and cross-references. One problem, one page.
- **Don't** use `border-left` or `border-right` greater than 1px as a colored accent stripe on callouts, cards, or list items. Full 4-side borders only.
- **Don't** add `.section-label` (small uppercase tracked eyebrow) to any new section. It exists in exactly one place: the Anxiety zone.
- **Don't** use warm-tinted backgrounds (cream, sand, parchment, ivory). The body background is chroma-zero `#FAFAFA`.
- **Don't** pair a 1px border with a soft wide drop shadow on the same element. Pick the border.
- **Don't** use `border-radius` larger than 16px on cards or sections. Pill radius (`999px`) is for buttons and badges only.
- **Don't** use `transition: all`. Target properties explicitly.
- **Don't** use glassmorphism, backdrop-filter blur, or frosted-glass effects.
- **Don't** use gradient text (`background-clip: text`).
- **Don't** write all-caps body copy. Uppercase is reserved for short labels (≤4 words) and badges.
