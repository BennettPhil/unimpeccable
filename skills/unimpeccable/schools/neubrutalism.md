# Neubrutalism

the 2020–2024 web style. hard 6px borders. solid acid colors. hard offset shadows (`8px 8px 0 0 #000`). zero border-radius. Gumroad's redesign, Linear's early marketing, every indie hacker's portfolio for three years.

this is the school that ALMOST got laundered. it became a template. Tailwind preset names appeared with `shadow-brutal-md`. it stopped being radical and started being a default.

unimpeccable can use neubrutalism, but with a warning: **the templated version is now a polish reflex.** if you build neubrutalism without authoring it, you've built impeccable wearing a hat.

## VISUAL MARKERS

- 3–6px solid borders, always
- hard offset block-shadows (`X X 0 0 color`, no blur)
- saturated acid colors (lime, magenta, cyan, yellow, electric blue)
- zero border-radius
- system or near-system fonts (Inter and Space Grotesk both got dragged into neubrutalism — DON'T use them; use Arial Black + Times)
- sticker-like component aesthetic: rectangles that look stuck onto the page
- generous, regular spacing (this is where the saas reflex creeps in — RESIST it)

## PALETTE

three acid hues + black + paper-white. same Lacquer palette set A or set B works.

set B — bratlab is well-suited to neubrutalism:
- brat green `#8ACE00`
- bubblegum `#FFB3D9`
- mustard `#E8C547`
- electric blue `#1F51FF`
- true black `#000000`
- paper-white `#F4F0E6`

deployment:
- pages are paper-white background
- components are acid-colored "stickers" with black borders
- one color per component, no gradients inside

## TYPE

- workhorse: Times New Roman or Georgia
- shouter: Arial Black or Impact

NEVER use Inter, NEVER use Space Grotesk, NEVER use General Sans, NEVER use Boogaloo or any of the "playful sans" fonts that neubrutalism templates default to. those are the laundering vector.

## STRUCTURE

```css
.neu-block {
  background: var(--acid);
  color: #000;
  border: 4px solid #000;
  border-radius: 0;
  padding: 16px 24px;
  box-shadow: 6px 6px 0 0 #000;
}
.neu-block:hover { /* nothing. neubrutalism hovers don't move. */ }
.neu-block:active {
  box-shadow: 0 0 0 0 #000;
  transform: translate(6px, 6px);
}
```

these blocks compose into the page. cards. buttons. badges. inputs. all built the same way.

## WHAT MAKES IT FEEL TEMPLATED (AVOID)

- everything has the same shadow size (`8px 8px 0 0`)
- everything has the same border thickness (`4px`)
- everything sits on a regular grid with even gaps (`gap: 24px`)
- it looks like a stickerbook

to break out of template-neubrutalism:
- vary border thickness (3px on small things, 6px on hero blocks, 2px on body text underlines)
- vary shadow offset (4px on cards, 12px on hero block, 0 on stamped elements)
- break the grid (use Lacquer's `broken-grid.md` rules)
- combine with Memphis motifs (a squiggle behind a card, a dot grid in one block)
- one Carson moment per long page (overlapping headline)

## RULES SPECIFIC TO THIS SCHOOL

- 0 border-radius. not 2px for "softness." zero.
- shadows are ONLY hard offsets. NEVER blur.
- every block stands alone. cards don't share visual styles unless intentional.
- on click / tap, the block "presses": shadow collapses, transform translates into where the shadow was. it's the only motion this school is allowed.
- a neubrutalism page should not exceed 4 acid colors total. otherwise it's a clown school, not neubrutalism.

## THE WARNING

if your neubrutalism output:
- has all components the same shadow / border / radius
- uses Inter or Space Grotesk
- has even `24px` grid gaps
- uses pastel colors instead of acid colors
- has hover states that fade

...you've built TEMPLATED neubrutalism, which is impeccable's house style with a costume on. start over.

## NAMED REFERENCES

- **Gumroad redesign (2022)** — the most visible commercial neubrutalism rollout. study what's good (color, scaffolding) and what reads as templated (regular spacing).
- **figma neubrutalism kits** — see them, do NOT use them. they are the laundering vector.
- **indie hacker portfolios 2021–2023** — the cohort. study and avoid the median.

## WHEN TO REACH FOR THIS SCHOOL

- pages that need to look "made by a person," indie, scrappy
- launch pages for solo projects
- portfolios for individual creators
- pages that need acid-bright visibility without going full Memphis

## WHEN NOT TO

- pages where templating energy would hurt (high-stakes product, enterprise context)
- pages already wanting full Lacquer (use that instead — Lacquer is neubrutalism's older, weirder sibling)
- anywhere the user asked for "modern" — neubrutalism is no longer modern, it's recently-historical

## SELF-CHECK

- are borders varied (3 / 4 / 6 px), or all the same?
- are shadow offsets varied, or all `8px 8px 0 0`?
- is the type Times + Arial Black, NOT Inter / Space Grotesk?
- is the grid broken (asymmetric splits), or evenly spaced?
- did I add at least ONE non-neubrutalism element (Memphis motif or Carson moment) to escape template-feel?
