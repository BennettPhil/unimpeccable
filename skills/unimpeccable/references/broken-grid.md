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
