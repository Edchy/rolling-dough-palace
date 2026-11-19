# Rolling Dough Palace

Portfolio concept: a mobile wood-fired pizza catering site (Astro). Brand register; design IS the product.

## Before any frontend work

Always read **DESIGN.md** and **PRODUCT.md** at the project root first, and follow them. DESIGN.md is the visual system (color, type, components, do's and don'ts); PRODUCT.md is the strategy (users, voice, anti-references). When they conflict on a visual call, DESIGN.md wins; on a strategic/voice call, PRODUCT.md wins.

## Hard bans (never violate, in copy or UI)

These live in full in DESIGN.md's "Hard bans" section. Restated here so they are never missed:

- **No em dashes (—)** anywhere — in copy, headings, or labels. Rewrite with a period, comma, parentheses, or a word. (Hyphens inside compound words are fine.)
- **No eyebrows** — never place a small kicker/label above a heading. Lead with the heading.
- **No decorative rule lines** — no hairline strokes, dividers, or accent lines used as ornament. Only genuinely structural lines (a real table rule or a semantic `<hr>`) are allowed.

## Stack notes

- Astro. Styles are global via `import "../styles/global.css"` in `BaseLayout.astro` (not scoped — applies site-wide). Colors route through tokens (`--bg`, `--text`, `--muted`, `--accent`); never hardcode hex at call sites — a real color palette is planned for later.
- Edit source and run `npm run build`; never write to `dist/`.
