# Carson / Ray Gun

David Carson. Beach Culture (1989–1991). Ray Gun magazine (1992–2000). the graphic designer who set a Bryan Ferry interview entirely in Zapf Dingbats because the interview was boring.

Carson's contribution: typography that prioritizes **feeling over legibility.** illegibility is itself a message. emotional impact precedes communication.

unimpeccable inherits this as the "Carson moment" — ONE per long page, never more. pure Carson school is for art-direction-heavy pages where the type IS the content.

## VISUAL MARKERS

- type overlapping type
- mid-word breaks
- baseline shifts that don't make sense
- multiple typefaces colliding in one paragraph
- type set on top of photographs at low contrast
- ragged, hand-set composition feel
- text frequently rotated, mirrored, fragmented
- white space used as composition tension, not "breathing"

## PALETTE

Carson was a print designer. his palette was usually:
- black ink on newsprint
- two-color riso jobs (red + black, yellow + black, blue + black)
- four-color process when the magazine could afford it
- color photography treated harshly: high contrast, color casts, deliberately wrong

for unimpeccable's web translation:
- charcoal `#1A1A1A`
- newsprint `#E8E2D0`
- ONE acid hue for emphasis: riso red, electric blue, or acid lime

never the full Memphis palette. Carson's energy is **monochrome with occasional violence.**

## TYPE

this is the school where typography rules are deliberately broken. but the breaks are STILL rationed.

allowed Carson moves (mix freely on a Carson-school page):

- **mid-word line break** — `IDEN` / `TITY` set as two stacked lines, the break in the middle of a word
- **overlapping headlines** — two headlines at 40–60% opacity each, positioned over each other
- **wrong-font paragraph** — a paragraph set in Impact at 14px for one block
- **baseline runaway** — `line-height: 3` for one stanza, words floating apart
- **font mid-paragraph swap** — one word in the workhorse, the next word in the shouter
- **type on photo** — body text laid across a photograph with NO contrast scrim — this is intentional Carson illegibility
- **mirrored type** — `transform: scaleX(-1)` on a headline or word, ONCE per page
- **size collision** — `48px` next to `200px` next to `16px` in the same line

on a Carson-school page you may use 2–3 of these per page. on any OTHER school's page (Lacquer, Memphis, etc.), only ONE.

## STRUCTURE

- composition is editorial-magazine, not web-grid
- pages feel like spreads: left-page / right-page tension
- content flows around blocks of photography
- no fixed columns — text frames are shapes, not grids
- captions wander far from their photos

implement with `grid-template-areas` for tight control, or `position: absolute` for true composition (ACCEPTABLE in this school only).

## RULES SPECIFIC TO THIS SCHOOL

- functional surfaces (navigation, forms, error messages) are NOT subject to Carson treatment. AA contrast, legible type, real labels. illegibility is for editorial moments only.
- a Carson-school page should have at least ONE photographic element. text-only is fine elsewhere; here it isn't.
- color photography is treated with high contrast and deliberate color casts. apply via CSS `filter: contrast(1.2) saturate(1.5)` or via the source image directly.
- DO NOT load actual Carson typefaces from the era (Template Gothic, Mason). use system fonts abused at extreme sizes. that's the unimpeccable constraint.

## NAMED REFERENCES

- **Ray Gun magazine, Bryan Ferry interview (1994)** — set entirely in Zapf Dingbats
- **Beach Culture, "End of Print" (1991–1992)** — Carson's surf-and-skate magazine, set the template
- **Carson's book "The End of Print" (1995)** — definitive monograph
- **Rudy VanderLans / Emigre magazine (1984–2005)** — adjacent, more programmatic, also relevant

## WHEN TO REACH FOR THIS SCHOOL

- art direction-heavy pages (portfolio, agency, exhibition catalogue)
- music / culture / publication sites
- single-page editorial pieces
- "feel-over-function" landing pages where the user is meant to GET A VIBE, not parse information

## WHEN NOT TO

- saas product pages (function loses)
- documentation
- dashboards
- e-commerce
- ANY page where the primary action is "convert the visitor"

## SELF-CHECK

- is there at least one photographic element on the page?
- are 2–3 Carson moves present (and rationed to non-functional elements)?
- is functional UI (nav, forms, errors) NOT subject to Carson treatment?
- is the palette monochrome + one acid accent?
- does the composition feel like an editorial spread, not a grid?
- could a user still complete the page's ONE functional task? (if there isn't one, that's fine; if there is, it must still work)
