<!-- SEED: re-run /impeccable document once there's code to capture the actual tokens and components. -->
---
name: Rolling Dough Palace
description: Mobile wood-fired pizza catering as an artsy, avant-garde statement brand. Monochrome, type-led, brutalist-leaning.
---

# Design System: Rolling Dough Palace

## 1. Overview

**Creative North Star: "The Pizza Manifesto"**

This is not a pizza place; it is a statement printed like a manifesto. Bohemian, avant-garde, novel, untraditional. The voice belongs next to a gallery poster, an artsy brewery's merch drop, or a creative studio's index page, not a catering template. Reference points: omnipollo.com (irreverent, maximalist, playful naming), ahumanfuture.co (asymmetric, oversized headings, serif + sans + monospace mixed without polite hierarchy, poetic microcopy), wondermake.xyz (anti-minimalist with character, varied column widths, conversational copy).

The work is **type-led, not image-led.** The headline is the hero; oversized display type set huge and tight carries the page, and the photograph is a supporting block, not a backdrop. Composition is asymmetric and a little raw: deliberate broken grids, varied column widths, monospace labels as texture, generous and uneven whitespace. Brutalist confidence, not brutalist ugliness; it must still be easy to navigate and read.

Stays monochrome for now (off-white + off-black) by intent. Brutalist/type-led design is *strongest* in two inks; the drama comes from scale, weight, and composition, not color. A **future color palette is planned but deliberately deferred**, routed through tokens so it drops in without re-architecting.

This system rejects the "generic beige restaurant template," overloaded Wix-style navigation, stocky corporate catering language (PRODUCT.md), AND now also rejects **traditional SaaS-clean layouts**: the polite logo-left / nav-links-right header, the tidy 50/50 hero split, centered safe symmetry. Untraditional is the brief.

**Key Characteristics:**
- Type-led: huge, tight display type is the hero; imagery supports it.
- Asymmetric, slightly raw, brutalist-leaning composition. Broken grids over tidy ones.
- Three type voices allowed: a display serif, a sans, and a **monospace** for labels/meta as texture.
- Monochrome (off-white + off-black) by intent; drama from scale and composition, not color.
- Navigation can be unconventional (placement, logo treatment) but must stay obvious and usable.
- Motion stays restrained: a confident entrance, no busy choreography.

## 2. Colors

Color-led. Bold flat blocks of saturated candy color, divided by ink rules (the YRS TRULY direction). The committed palette is **Pastel**: a playful, Omnipollo-adjacent candy set that pushes hardest on "this is not a traditional pizza place." Color carries the brand; the photograph is the only realism.

### Primary
- **Candy Pink** (`#ff5bbf`): the accent. Framed-image border, CTA fill, the loudest hue. Used where the eye should land.

### Secondary
- **Mint** (`#b6e3c6`): the heading block field. Soft, fresh, holds the big serif headline.
- **Lilac** (`#c9b8f5`): the image block field. The framed photo sits on this.
- **Electric Yellow** (`#ffe14d`): reserved accent for tags, highlights, small moments.

### Neutral
- **Indigo Ink** (`#2a2350`): all text and the brutalist divider rules. Deep blue-violet, never pure black, so it belongs to the candy world.
- **Paper** (`#fbf7ff`): the base surface (header, actions strip, footer). A cool off-white tinted toward the lilac, not warm cream.
- **Muted Indigo** (`#5b5285`): secondary text. Clears 4.5:1 on Paper.

### Named Rules
**The Block Rule.** The hero is flat color blocks divided by 1px ink rules, every cell its own hue. No gradients, no soft shadows between blocks; the hard edge is the aesthetic.

**The Token Seam Rule.** Every color is a semantic token (`--block-1`, `--block-2`, `--frame`, `--block-1-ink`, `--accent`, `--paper`, `--text`). Palettes are swapped by setting `data-palette` on `<html>`; never hardcode a hex at a call site.

**Alternate palettes (kept, not active).** Two other palettes live in the tokens behind `data-palette`: **Italian** (blue / green / red / white / near-black) and **Marigold** (ochre / ink-blue / tomato, the first color pass). Pastel is the committed default; the others are one attribute away for future comparison.

## 3. Typography

**Display Font:** A characterful serif `[family to be chosen at implementation]` (with `Georgia, serif` fallback). The hero. Set huge and tight; this carries the page.
**Body Font:** A sans-serif `[family to be chosen at implementation]` (with `system-ui, sans-serif` fallback). Running text, lead copy, buttons.
**Label/Mono Font:** A monospace `[family to be chosen at implementation]` (with `ui-monospace, monospace` fallback). Eyebrow-free labels, meta, indices, nav accents. Texture, not decoration.

**Character:** Three voices used with intent, not politeness: a display serif for statements, a clean sans for reading, a monospace for raw/technical texture. The pairing is the avant-garde signal (serif + mono is the move on the reference sites). Still distinct classifications, never two near-identical sans (the earliest attempt paired two grotesques; don't repeat that).

### Hierarchy
- **Display** (serif, ~600–700, `clamp()` up to ~6rem, line-height ~0.95, letter-spacing ~-0.02em): the hero statement and primary section titles. Goes BIG. This is where the drama lives.
- **Headline** (serif, ~2–2.6rem): section headings.
- **Title** (sans or serif medium, ~1.25–1.5rem): sub-sections.
- **Body** (sans, regular, ~1–1.25rem, line-height ~1.55): running and lead copy. Cap measure at 65–75ch.
- **Label** (mono, ~0.8rem, optionally caps with light tracking): meta, nav accents, indices, small wayfinding. The monospace texture replaces the banned eyebrow.

### Named Rules
**The Three-Voice Rule.** Serif (display), sans (body), monospace (labels/meta). Three classifications, no two from the same family. The mono is what makes it read avant-garde instead of corporate; use it for small labels and texture, never for body copy.

**The Type-Is-The-Hero Rule.** Display type is the largest, loudest element on any primary view. If an image is competing with the headline for dominance, the type loses its job. Set the headline big enough to feel like a statement.

## 4. Elevation

Flat by default. Depth comes from contrast, scale, and composition, not shadows. This suits the brutalist lane: surfaces sit on the page rather than floating above it. The one exception is the navigation dropdown, which lifts with a single soft shadow to read as a temporary overlay.

**Layout doctrine (folded here, no separate Layout section per spec).** Composition is **asymmetric and type-led**. Reject the tidy 50/50 split and the centered safe layout. Favor a dominant headline column with a narrower supporting image/meta column, varied widths, deliberate uneven whitespace, and the occasional element that breaks the grid line on purpose. Monospace meta labels (an index number, a location tag, a year) anchor the rawness. It must read as intentional and stay easy to navigate; raw is a posture, not an excuse for confusion.

### Named Rules
**The Flat-By-Default Rule.** Surfaces are flat at rest. A shadow appears only when an element genuinely floats above the page (the nav panel), never as decoration.

**The Broken-Grid Rule.** Symmetry is the enemy here. No 50/50 hero, no centered-everything. Bias the composition: oversized type on the larger side, image/meta on the smaller, and let at least one element sit off the expected line.

## 5. Components

*Seed stage. Components are synthesized from tokens at build time. The stylesheet currently carries a working centered-logo header, a color-block hero, footer, and button variants. These get documented for real on the next scan-mode run.*

### Buttons
- **Shape:** fully rounded pill (`border-radius: 999px`).
- **Primary:** Press Black fill, Flour White text. The `--accent` token (today = ink) drives the fill so a future color slots in cleanly.
- **Hover / Focus:** restrained — subtle state change only; visible focus ring (current: 2px outline, offset 3px).

### Brand glyph (the wheel)
- One bespoke motif: a **bike wheel** (tyre, hub, four spokes), the cykel-oven identity redrawn as a quirky marker. **Not** a stock icon set; the brutalist register rejects tidy SaaS iconography, so the brand speaks in its own mark.
- Stored as the `--glyph-wheel` token and rendered via CSS `mask`, so it inks itself from `currentColor` and flips to paper on dark cells automatically. Never hardcode the SVG at a call site; use the `.glyph-mark` class.
- Two roles: a **corner stamp** on genuine text/checklist cells (step-list, contact-brief), sitting alongside (not replacing) the mono index; and a small **section-heading mark** (`.glyph-mark--head`, in `--accent`) that punctuates a title rather than competing with it. Use sparingly, as fun punctuation, not as a bullet on every list (card/tag/grid lists already carry their own visual meaning and stay glyph-free).

### Food icons (the pizzaicons set)
- A hand-picked Noun Project line set lives in `/public/pizzaicons/` (pizza piece, chilli, cheese, hot pizza, pizza flipper, pizza cutter, tomato, onion). Single-path, so they ink themselves from `currentColor` via the same `.glyph-mark` mechanism as the wheel and flip on dark cells.
- These are **content** markers, tied to meaning, never generic UI bullets: a per-pizza icon beside the menu index (Margherita=slice, Diavola=chilli, Quattro formaggi=cheese), the cooking story on `/event` "Så funkar det" (cutter then fire then flipper, matching plan/light/bake), and food-relevant section head-marks.
- Set the file per call site with the `--mark` custom property via a `.glyph-mark--<name>` modifier; the base `.glyph-mark` defaults to the wheel. Never reference the SVG path directly at a call site.

### Navigation
- Inline links in Muted Ink, darkening to full ink on hover; a pill CTA ("Boka oss") at the end. A `<details>` dropdown groups city/catering links so the top nav stays scannable (per PRODUCT.md). Dropdown panel floats with one soft shadow. Mobile: header stacks vertically.

## 6. Do's and Don'ts

### Do:
- **Do** keep it strictly two inks (off-white + off-black) plus neutral grays until the color palette is intentionally introduced.
- **Do** use off-white (`~#fafafa`) and off-black (`~#222`), never pure `#fff` / `#000`.
- **Do** route every color through a token so the planned palette drops in without touching components.
- **Do** pair one serif (titles) with one sans (body) — contrast on the type axis.
- **Do** keep secondary/muted text dark enough to clear 4.5:1 on the off-white surface.
- **Do** keep motion restrained: state changes and quiet transitions only.

### Don't:
- **Don't** ship a "generic beige restaurant template" — no cream/sand/parchment body; the neutral is true off-white, not warm-tinted.
- **Don't** build "overloaded Wix-style navigation" — keep the top nav short and scannable; group city links under catering.
- **Don't** write "stocky corporate catering language" — the voice stays handmade and direct.
- **Don't** introduce accent hues yet. The color palette is a deliberate later step, not an early indulgence.
- **Don't** pair two fonts from the same classification (e.g. two grotesques).
- **Don't** add decorative shadows or glassmorphism; surfaces are flat at rest.

### Hard bans (non-negotiable — apply to every surface, in copy and in UI):
- **Don't use em dashes (—) anywhere** — not in copy, headings, or labels. Rewrite the sentence: use a period, a comma, parentheses, or "och"/"till" instead. Hyphens in compound words (e.g. "vedugns-") are fine; the ban is on the em-dash punctuation mark.
- **Don't use eyebrows** — the small kicker/label sitting above a heading (e.g. "Mobil vedugnspizza sedan 2021" over the hero H1). No section gets a little intro label. Lead with the heading itself.
- **Don't use decorative rule lines** — no short hairline strokes, dividers, or accent lines used as ornament (the dash before a kicker, a line under a heading, a stroke separating sections). Functional structural lines are the only exception: a real table rule, or a genuine content-dividing `<hr>` where the document semantics call for one. Decoration-only lines are forbidden.
