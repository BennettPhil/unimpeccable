# Lacquer

the house style. fuses four schools so the output reads as one thing instead of a survey.

- **Memphis** — palette, motifs, pattern fills
- **Web brutalism** — load-bearing structure, raw HTML scaffolding, hard borders, zero radius
- **Carson / Ray Gun** — rationed illegibility moments
- **Zine / photocopy** — texture overlay layer

brutalism is the skeleton. Memphis is the clothing. Carson is the scream. zine is the dirt. in that order, always.

## PALETTE

pick ONE set per page. do not mix sets within a page.

### set A — laminate
- acid lime `#C8FF00`
- hot magenta `#FF2E93`
- cyan `#00C2FF`
- safety orange `#FF6A00`
- true black `#000000`
- paper-white `#F4F0E6` (never `#FFFFFF` — pure white reads as default)

### set B — bratlab
- brat green `#8ACE00`
- bubblegum `#FFB3D9`
- mustard `#E8C547`
- electric blue `#1F51FF`
- true black `#000000`
- paper-white `#F4F0E6`

### set C — sottsass-domestic
- terracotta `#D2521D`
- mint `#7FDBB6`
- cobalt `#1B3FB2`
- lemon `#F5E663`
- true black `#000000`
- paper-white `#F4F0E6`

### set D — newsprint
- riso red `#FF4438`
- riso blue `#0078BF`
- riso yellow `#FFE800`
- charcoal `#1A1A1A`
- newsprint `#E8E2D0`
- (no paper-white in this set — newsprint replaces it)

**contrast rule:** any text on a color must hold ≥4.5:1 against its background OR be decoration only. if it's a heading, body copy, link, button label, error, or form label — it's not decoration. AA holds.

## TYPE

exactly two system fonts per page. no webfonts. no Inter, no Geist, no Helvetica Neue, no SF Pro Display, no Söhne, no Suisse.

### the two slots

- **the workhorse** — `Times New Roman, Times, serif` OR `Georgia, serif`
- **the shouter** — `"Arial Black", "Helvetica Inserat", "Impact", sans-serif` OR `Impact, sans-serif`

pick one of each. lock them. don't introduce a third.

### the code-display exception

`<pre><code>` blocks containing literal code may use `"Courier New", Courier, monospace`. this is the ONLY allowed third slot, and only for actual code-display. not for stylistic monospace meta-text. not for inline `<code>` outside a `<pre>`. not for captions or footer text.

### sizing

abuse the shouter at extreme sizes. minimum hero size: `clamp(72px, 18vw, 280px)`. line-height `0.85`. tracking `-0.03em`. let it overflow if it wants to.

the workhorse sets body at `18–20px`, line-height `1.35`. tight. not "comfortable." comfortable is the enemy.

### the Carson moment

ONE per long page. options (pick one, not more):
- mid-word line break in a headline
- two headlines overlapping at 60% opacity each
- a paragraph set in a font that doesn't make sense for it (e.g. Impact at 14px running text for one block)
- runaway leading (`line-height: 2.8`) for one stanza
- a word set in a single different color from the rest of the line

never two Carson moments on the same screen. that's noise, not authorship.

## STRUCTURE

brutalism carries the load. these are not suggestions.

- `border-radius: 0` everywhere. zero. not `2px`. not `4px`. zero.
- borders are `3px` or `6px` solid, color from the palette (NOT gray)
- shadows are hard offset blocks only: `8px 8px 0 0 <palette-color>`. no `blur`. no `rgba(0,0,0,0.1)`. never a soft shadow.
- gutters are `0` or `4px`. content blocks butt against each other.
- full-bleed by default. `max-width` is the exception, not the rule. when you do constrain width, do it asymmetrically (e.g. `margin-left: 17%; margin-right: 4%`).
- breakpoints break at arbitrary widths (`712px`, `923px`), not the canonical Tailwind ones. defies the framework.

## MEMPHIS MOTIFS

rationed, not wallpapered. ration scales with register (see `references/page-register.md`).

- PRODUCT register: 2 to 3 per section.
- SHOWCASE register: 3 to 5 per major section. memphis-school sections in showcase mode should sit at the upper end.
- ARTIFACT register: per the school's rules.

inline SVG, no images. fewer than 2 in any section means the section won't read as memphis — that's a timidity failure, not restraint.

- squiggle line (3px black stroke, 4 humps, 200px wide)
- dot grid (5x5, alternating two palette colors, 8px dots, 24px spacing)
- diagonal hatch (2px black lines at 45°, 6px spacing)
- triangle / circle / squiggle floating in a corner of a block, slightly clipped by the edge
- a single color block behind a heading, rotated 2–4°, NOT the heading itself rotated

if you find yourself filling whitespace with motifs because the page feels empty, **stop.** the page is allowed to be empty. crowding empty is impeccable's reflex, not ours.

## TEXTURE LAYER

last. always last.

- one SVG halftone or grain overlay across the page at `opacity: 0.06` to `0.12`
- `mix-blend-mode: multiply` on the overlay
- one photocopy-distress treatment on ONE element (a heading, a single button) — `filter: url(#photocopy)` with a custom feTurbulence
- no animation on the texture layer. it's static. it's dirt.

## WHAT LACQUER IS NOT

- not glitch. glitch is its own school. don't blend.
- not vaporwave. don't reach for chrome / palms / sunset gradient.
- not "ironic 90s." Lacquer is sincere about its lineage. irony is a different register.
- not maximalism for its own sake. every motif justifies itself or it doesn't ship.

## SELF-CHECK BEFORE SHIPPING

ask, in order:
1. is the structure brutalist? (zero radius, hard borders, butt-joined blocks)
2. is the palette ONE of the four sets, not a remix?
3. is there exactly ONE Carson moment, no more?
4. are motifs rationed (2–3 per section)?
5. is the texture overlay subtle (4–12% opacity) and singular?
6. does functional text hold AA contrast?
7. could this ship as a Webflow template? **if yes, you failed. start over.**
