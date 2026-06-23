---
name: ghosted.
description: Find out who isn't following you back — privately, locally, instantly.
colors:
  bg: "oklch(0.07 0.000 0)"
  surface: "oklch(0.12 0.000 0)"
  surface-2: "oklch(0.17 0.000 0)"
  border: "oklch(0.22 0.000 0)"
  border-hover: "oklch(0.32 0.000 0)"
  ink: "oklch(0.97 0.000 0)"
  muted: "oklch(0.54 0.000 0)"
  dim: "oklch(0.32 0.000 0)"
  primary: "oklch(0.68 0.130 150)"
  primary-glow: "oklch(0.68 0.130 150 / 0.12)"
  primary-sub: "oklch(0.68 0.130 150 / 0.07)"
typography:
  display:
    fontFamily: "'Syne', system-ui, sans-serif"
    fontSize: "clamp(2.5rem, 13vw, 6rem)"
    fontWeight: 800
    lineHeight: 0.92
    letterSpacing: "-0.04em"
  headline:
    fontFamily: "'Space Grotesk', system-ui, sans-serif"
    fontSize: "clamp(1.875rem, 7vw, 2.75rem)"
    fontWeight: 800
    lineHeight: 1
    letterSpacing: "-0.03em"
  title:
    fontFamily: "'Space Grotesk', system-ui, sans-serif"
    fontSize: "0.9375rem"
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: "-0.01em"
  body:
    fontFamily: "'Space Grotesk', system-ui, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 400
    lineHeight: 1.65
    letterSpacing: "0"
  label:
    fontFamily: "'Space Grotesk', system-ui, sans-serif"
    fontSize: "0.6875rem"
    fontWeight: 600
    lineHeight: 1
    letterSpacing: "0.08em"
  mono:
    fontFamily: "'JetBrains Mono', ui-monospace, monospace"
    fontSize: "0.8125rem"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: "0"
rounded:
  sm: "6px"
  md: "10px"
  lg: "14px"
spacing:
  xs: "8px"
  sm: "16px"
  md: "24px"
  lg: "40px"
  xl: "64px"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    padding: "16px 24px"
  button-primary-hover:
    backgroundColor: "oklch(0.72 0.130 150)"
    textColor: "{colors.ink}"
  button-primary-disabled:
    backgroundColor: "{colors.surface-2}"
    textColor: "{colors.dim}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.muted}"
    rounded: "{rounded.sm}"
    padding: "8px 14px"
  button-ghost-active:
    backgroundColor: "{colors.primary-sub}"
    textColor: "{colors.primary}"
  drop-zone:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.lg}"
    padding: "32px 20px 28px"
  drop-zone-loaded:
    backgroundColor: "{colors.primary-sub}"
    textColor: "{colors.primary}"
  input-search:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.sm}"
    padding: "11px 14px"
---

# Design System: ghosted.

## 1. Overview

**Creative North Star: "The Late Read"**

ghosted. is the screen you check late at night, alone — the one you wouldn't want open if someone walked by. The design holds that mood: a deep, unreflective black; one signal color that says something without shouting; Space Grotesk setting everything in clean, direct prose; the "ghosted." mark in Syne — the only typeface that doesn't apologize for itself.

This is a restrained system. The accent (a deep botanical green, `oklch(0.68 0.130 150)`) appears in fewer than 10% of any screen's surface area. Its job is to mark the loaded state, the focused element, the final tally. Its rarity is structural — when the green appears, it means something. Everything else is pure neutral: no hue leaks into the background, no warmth in the surfaces.

Motion is choreographed where it matters and absent where it doesn't. Results arrive with purpose — the list staggers in, the stats count up — because the reveal IS the moment this tool was built for. Interactions respond instantly. Reduced-motion users get the same content as immediate crossfades; nothing is ever gated behind an animation class.

**Key Characteristics:**
- Pure near-black background; no tinted neutrals anywhere in the architectural layers
- One signal color: botanical moss green, ≤10% of any screen surface
- Syne exclusively for the "ghosted." wordmark — never UI text, never stats
- Space Grotesk for all other text: clean, direct, without character debt
- JetBrains Mono restricted to @handles and timestamps — two contexts, no more
- Choreographed reveal: the results entrance is designed, not defaulted

## 2. Colors: The Unreflective Palette

One accent, no warmth, no apology. The palette reads as a private screen at night: deep black absorbs everything; a single green signal cuts through exactly when it needs to.

### Primary
- **Moss Signal** (`oklch(0.68 0.130 150)`): The brand anchor. Applied to: loaded drop-zone borders, the "not back" stat card highlight, hover states on user list items, the Analyze button fill, and focus rings. Never appears on more than 10% of any screen's total surface area. Use white text (`colors.ink`) on filled primary — the H-K effect makes saturated mid-luminance fills perceptually brighter than their measured luminance; dark text on this fill reads as muddy.

### Neutral
- **Void** (`oklch(0.07 0.000 0)`): Page background. Pure, untinted near-black. Chroma exactly 0.
- **Well** (`oklch(0.12 0.000 0)`): Card and panel surfaces. Drop zones, stat cards, user list items, the instruction block.
- **Risen** (`oklch(0.17 0.000 0)`): Hover state for surface elements. Never the default.
- **Hairline** (`oklch(0.22 0.000 0)`): Default borders and separators.
- **Lit** (`oklch(0.32 0.000 0)`): Hover borders, decorative non-text icons and arrows. Not for any text content.
- **Ink** (`oklch(0.97 0.000 0)`): All primary text. No hue. No warmth.
- **Muted** (`oklch(0.54 0.000 0)`): Secondary text and all placeholder text. Verify ≥4.5:1 against the surface it sits on.

### Named Rules
**The One Color Rule.** The moss signal appears in one role per element at most — either border, or background tint, or text color. Never two simultaneously on the same element. Scarcity is structural.

**The No-Tint Rule.** `void` and `well` have chroma exactly 0.000. The brand lives in the primary color and the typography. It does not live in the room's walls.

## 3. Typography

**Display Font:** Syne (system-ui, sans-serif fallback) — the "ghosted." wordmark only
**UI Font:** Space Grotesk (system-ui, sans-serif fallback)
**Data Font:** JetBrains Mono (ui-monospace fallback) — @handles and timestamps only

**Character:** Syne holds "ghosted." as a mark, not a headline — its wide, assured weight makes the name feel claimed, not set. Space Grotesk is its foil: geometric, clear, built for instruction and navigation without drawing attention to itself. JetBrains Mono appears only where the data is machine-readable; its presence is suppressed elsewhere to keep the experience edgy and minimal, not terminal.

### Hierarchy
- **Display** (Syne 800, `clamp(2.5rem, 13vw, 6rem)`, leading 0.92, tracking −0.04em): The "ghosted." wordmark. One use per page. Never reused for any other heading.
- **Headline** (Space Grotesk 800, `clamp(1.875rem, 7vw, 2.75rem)`, leading 1, tracking −0.03em): Stat card numbers. Large numeric readouts only.
- **Title** (Space Grotesk 600, 0.9375rem, leading 1.3, tracking −0.01em): Section headers, drop-zone labels, results section header.
- **Body** (Space Grotesk 400, 0.875rem, leading 1.65): Instruction steps, error messages, tagline copy. Max 65ch per line.
- **Label** (Space Grotesk 600, 0.6875rem, tracking 0.08em, uppercase): Stat card identifiers. Used sparingly — only where a label structurally identifies a figure that needs it. Not on every section.
- **Mono** (JetBrains Mono 400, 0.8125rem): @username handles and follow timestamps. Two contexts only.

### Named Rules
**The Two-Font Rule.** Syne appears once. Mono marks data. Everything else is Space Grotesk. If a third typeface appears, one of the three is wrong and must be removed.

**The Mono Fence.** JetBrains Mono is not an aesthetic choice — it is a data marker. It marks machine-readable identifiers: @usernames, timestamps. Labels, instructions, hints, the tagline, error messages, footer: all Space Grotesk. Any mono usage outside those two data contexts is a violation of The Mono Fence.

## 4. Elevation

Flat by default. Surfaces are differentiated by background lightness (L steps of ~0.05), not by shadows. There are no drop shadows at rest or on hover.

Three levels: `void` → `well` (panels) → `risen` (hover). Transitions between levels are 0.2s ease-out background shifts; no shadow appears as a result of interaction.

Focus rings use the primary signal as a 2px outline at 3px offset. This is the one case where color appears on a neutral structural element in response to state.

A single radial gradient glow (`primary-glow`) sits at the top of the page at 10% opacity — it establishes place, not decoration, and is non-interactive.

### Named Rules
**The Flat-by-Default Rule.** Elements are flat at rest. Depth is value (lightness), never shadow. There are no box-shadows in this system except the focus ring (which is an outline, not a shadow).

## 5. Components

### Buttons
- **Shape:** Gently rounded (10px, `rounded.md`)
- **Primary (Analyze):** Moss signal fill, ink text, full width, Space Grotesk 600 uppercase label tracking 0.08em. The button occupies full container width; it's not a small inline action — it's the commit moment.
- **Hover:** Lightness up to `oklch(0.72 0.130 150)`. No scale, no shadow.
- **Active:** `scale(0.985)`, 0.15s ease-out.
- **Disabled:** `surface-2` fill, `dim` text, cursor not-allowed.
- **Ghost (Sort Cycle):** Transparent fill, `border` stroke (1px), `muted` text. Hover: `border-hover` stroke, `ink` text. Active sort: `primary-sub` fill, `primary` text and border (1px solid).

### Drop Zones
- **Shape:** 14px radius (`rounded.lg`) — wider than cards; the zones invite action.
- **Default:** `surface` fill, 1.5px dashed `border` stroke.
- **Hover / Drag-over:** `primary-sub` fill, `primary` border (stays dashed), `scale(1.02)`.
- **Loaded:** `primary-sub` fill, `primary` border (solid). Hint text: `✓ loaded` in `primary` color via mono. Filename below in mono `primary`.
- **Icon:** Emoji, 32px. Animates `scale(1.12) translateY(-2px)` on zone hover.

### Stat Cards
- **Shape:** 14px radius. Three-column grid.
- **Standard:** `surface` fill, `border` stroke (1px).
- **Hot ("not back"):** `primary-sub` fill, `primary` border (1px solid). Number in `primary`.
- **Number:** Space Grotesk 800, `clamp(1.875rem, 7vw, 2.75rem)`, tracking −0.03em. Standard: `ink`. Hot: `primary`.
- **Label:** Space Grotesk 600, 9px, uppercase, tracking 0.16em, `muted`.
- **Padding:** 22px top, 18px bottom, 16px sides.

### User List Items
- **Shape:** 10px radius. `surface` fill, `border` stroke (1px).
- **Layout:** Flex row. Left: @handle + date (stacked). Right: → arrow.
- **Handle:** Space Grotesk 500, 0.875rem, `ink`. On hover: `primary`.
- **Date:** JetBrains Mono 400, 10px, `muted` (must reach 4.5:1 against `surface`).
- **Arrow:** Space Grotesk, `dim` at rest. On hover: `translateX(4px)`, `primary`.
- **Row hover:** `translateX(4px)`, `surface-2` bg, `border-hover` border. Transition 0.15s ease-out.
- **Entrance animation:** Staggered `slideIn` (translateX(−10px) + opacity 0 → 1), 0.3s `cubic-bezier(0.16, 1, 0.3, 1)`, 18ms per item, capped at 900ms total delay. Reduced-motion: instant opacity transition, no translate.

### Search Input
- **Shape:** 6px radius (`rounded.sm`). `surface` fill, `border` stroke (1px).
- **Text:** Space Grotesk 400, 0.875rem. Placeholder: `muted` (≥4.5:1 vs `surface`).
- **Focus:** Border shifts to `primary`. No glow, no ring — the border shift is the focus signal.
- **Inline clear button:** Ghost-style, position absolute right-inside. Visible only when input has value.

### Instruction Block (How It Works)
- **Container:** `surface` fill, `border` stroke (1px), 14px radius, 24px padding.
- **Step numbers:** 22px circle, `surface-2` fill, `border` stroke, `primary` numeral. This is a genuine 4-step ordered sequence; numbered markers are appropriate here. Do not reproduce the numbered circle pattern elsewhere unless the sequence is also real.
- **Step text:** Space Grotesk 400, 0.875rem body.

## 6. Do's and Don'ts

### Do:
- **Do** use `oklch(0.97 0.000 0)` (ink) on the moss signal fill — the H-K effect makes this saturated fill read brighter than its luminance; near-white text is the correct call.
- **Do** restrict JetBrains Mono to @handles and timestamps. The Mono Fence is a hard rule.
- **Do** use `text-wrap: balance` on the "ghosted." display heading and any h2.
- **Do** provide a `@media (prefers-reduced-motion: reduce)` alternative to every animated element. List stagger, section fadeUp, stat count-up: all must degrade to a crossfade or instant show. Content must never be gated behind an animation class.
- **Do** verify ≥4.5:1 for muted and placeholder text against the immediate surface behind them (`well`, not `void`).
- **Do** treat the numbered step circles as a one-time deliberate affordance — they mark an actual 4-step ordered sequence. They do not generalize.
- **Do** use `scale(0.985)` on the primary button's `:active` state — the micro-press is the tool's only physical gesture.

### Don't:
- **Don't** use Syne for anything except the "ghosted." wordmark. Not for stat numbers, not for step labels, not for the tagline. Syne is a brand identity mark, not a display typeface in this system.
- **Don't** add any chroma to `void` or `well`. Both surfaces have chroma exactly 0.000. The No-Tint Rule is absolute.
- **Don't** use neon or bright green anywhere in this system. The moss signal (`oklch(0.68 0.130 150)`) is botanical and desaturated. Any brighter green — `#00ff00` adjacents, terminal greens, neon limes — turns this into a hacker tool. This is not a hacker tool.
- **Don't** build a SaaS-template layout: no feature tables, no pricing rows, no hero-metric grids. The stats block answers one question. It is not a product landing page.
- **Don't** apply Instagram-adjacent colors: no pink gradients, no purple/magenta, no colorful ring aesthetics. ghosted. is deliberately counter-branded in that direction.
- **Don't** use `border-left` or `border-right` greater than 1px as a colored accent stripe on list items or cards. Full borders, tints, or nothing.
- **Don't** place uppercase tracked labels above sections that don't structurally need identification. Stat cards need them (the figure needs naming); section headings that read fine as titles don't.
- **Don't** add box-shadows to cards, panels, or buttons at rest. The Flat-by-Default Rule is absolute.
