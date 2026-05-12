# broken-grid

the grid is not sacred. the grid is a tool. tools can be put down.

but: **off-grid is not no-grid.** random placement is slop. authored breaks need a system to break against. you set the grid, then you violate it on purpose, in specific places, for specific effects.

## THE BASE

start with a real grid. you can't break what doesn't exist.

- 12 columns
- gutters: `4px` (not `24px`, not `32px` — we don't breathe)
- max-width: **none by default.** full-bleed is the law.
- breakpoints: pick non-canonical numbers. `712px`, `923px`, `1186px`. NOT Tailwind's `640 / 768 / 1024 / 1280`. the framework's defaults are the enemy's defaults.

## THE FOUR AUTHORIZED BREAKS

these are the only ways to break the grid. anything else is slop.

### 1. ASYMMETRIC SPLIT

split a section non-50/50, non-golden-ratio. specifically:
- 17 / 83
- 31 / 69
- 38 / 62
- 71 / 29

the small column is content-dense (heading + paragraph). the large column is a single object (one image, one color block, one motif). reverse the conventional weighting.

### 2. FULL-BLEED OVERLAP

place a block so it extends past the section above or below it by 60–120px. it crashes the boundary. the next section's background color shows through where it doesn't reach, OR the block sits ON TOP of the section line.

use this **once or twice per page.** more = soup.

### 3. DIAGONAL FLOW

rotate ONE element 2°–6°. never more than 6° (becomes "fun startup mascot energy"). the rotation is on a heading container, a color block, or a card — NOT on body text, NOT on functional buttons.

a second diagonal element on the page must rotate in the **opposite direction.** they argue.

### 4. NEGATIVE INDENT / NEGATIVE MARGIN

pull a headline or block `margin-left: -8%` so it overflows the section's notional content column. it spills into the gutter, into the next column. let it.

never pull functional elements. only headlines, color blocks, decorative type, motifs.

## THE THREE PAGE-LEVEL BREAKS (SHOWCASE REGISTER)

the four breaks above are COMPONENT-level. these three are PAGE-level. valid only in SHOWCASE / MANIFESTO register. these are what make a long-scroll page argue with itself instead of stacking politely.

### 5. SECTION BLEED

a block from section N extends 60 to 200 px past the section's boundary INTO section N+1 (or N-1). the next section's background color shows around the bleed, OR the block sits on top of the section line.

implement.

- don't constrain the section with `overflow: hidden`. let it bleed.
- use `margin-bottom: -120px` or `position: relative; top: 80px;` on the bleeding block.
- ensure the bleeding block has `position: relative; z-index: 2;` so it sits above the next section.
- the next section uses `position: relative; z-index: 1;`.

use this 1 to 2 times per page. more = soup. SECTION BOUNDARIES MUST CRASH at major transitions. if all your sections butt up at flat horizontal lines, the page is a stack and you failed the timidity check.

### 6. VIEWPORT EXTENSION

content extends past the right edge of the viewport intentionally. radical-italian's "il monumento continuo" is the canonical example — a grid that doesn't stop at the page edge.

implement.

- `overflow-x: visible` on the section.
- `body { overflow-x: hidden; }` globally so the page doesn't gain horizontal scroll.
- a decorative element uses `position: relative; right: -240px;` or `width: calc(100% + 400px);` to push past the right edge.
- works equally on the left edge (`left: -240px`) — a headline running off the left edge with the user expected to know what it would say.

use this 1 to 2 times per page. headlines, grid lines, marquees, terrazzo blocks. not functional content. not navigation.

### 7. SCALE VARIATION ACROSS SIBLINGS

when displaying N items of the same kind (school cards, command rows, feature blocks) — they MUST NOT share dimensions. assign each footprint to match its content's character.

if you find yourself writing `grid-template-columns: repeat(N, 1fr)` for a row of cards with the same height, **stop.** that's a catalogue. you're presenting anti-design as information design. it's a contradiction.

instead.

- one item is wide and dominant
- one is small and almost-missed
- one is rotated and overlapping its neighbors
- one is bare (no card border, just content directly on the page background)
- one has fake browser chrome / period-piece chrome wrapping it
- one is a TOWER (taller than wide, content stacked vertically)
- one is a STRIP (wider than tall, content stacked horizontally)
- one is a SCAN (rotated, ragged-edged, halftone-overlaid)

if eight schools share a footprint, you've told the user the schools are interchangeable. they aren't. each footprint argues for itself. no card respects the others' bounds.

**this is the single most important page-level rule in showcase register.** more pages have failed the timidity check on this rule than any other.

## WHAT YOU DO NOT DO

- random rotation on every card (this is the 2017 "fun" landing page tell)
- "absolute position the elements wherever" — that's not breaking, that's abandoning
- overlap text on text where both must be read (Carson moment is for headlines, ONE per page)
- masonry / Pinterest-style layouts — they're 2014, and they're "discovery feeds," not anti-design
- diagonal section dividers (the saas-clip-path tell) — banned

## SCAFFOLD RULES

- sections butt up against each other. `margin: 0` between sections. the border between them is a `6px solid black` line, or a hard color change, or both.
- inside a section: content blocks butt up against each other too. gaps are `0` or `4px`.
- if a designer reflex tells you to add `padding: 4rem` for "breathing room" — cut it in half. then cut it in half again. content crowds.

## ALIGNMENT POLICY

- **left-aligned by default.** centered is the saas reflex. don't.
- right-align is reserved for ONE element per page, used for impact.
- when text wraps, let it wrap raggedly. no `text-wrap: balance` to fake an "even" two-line headline. orphans and widows live here.
- baseline alignment between adjacent type sizes is not required. let them argue.

## ROUNDED-CORNER POLICY

zero. `border-radius: 0` on everything. not `2px`. not `4px`. zero.

the one exception: a perfect circle as a Memphis motif (`border-radius: 50%` on an SVG or a `div` that is exactly square). that's a shape, not a "softened corner."

## SHADOW POLICY

no soft shadows. ever.

allowed:
- hard offset block-shadow: `box-shadow: 8px 8px 0 0 #000` (or a palette color)
- the shadow is the same size and shape as the element it's behind
- the shadow color is from the palette, not gray, not `rgba(0,0,0,0.1)`

banned:
- any `blur` > 0
- any `rgba(0,0,0,*)` shadow
- any "elevation" abstraction from Material / Tailwind

## SECTION RHYTHM

a long page has at least three different scaffold treatments. don't repeat the same layout twice in a row. patterns to alternate:

- full-bleed color block + headline overflowing left edge
- 17/83 split with the dense column on the right (reverse of convention)
- centered column with a 6° rotated background block behind it
- two stacked rows, the upper row's bottom-edge eaten by a Memphis motif from below

mix and match. never repeat.

## SELF-CHECK

- did I set a grid before I broke it?
- did I use only the four authorized breaks?
- is `border-radius: 0` on everything except true circle motifs?
- are all shadows hard offsets, no blur, palette color?
- did I avoid Tailwind's default breakpoint numbers?
- did I crowd, not breathe?
