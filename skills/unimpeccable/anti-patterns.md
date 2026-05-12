# anti-patterns

two ways to fail. you must fail neither.

- **SLOP** — accidentally bad. random where it should be authored. mismatched where it should clash on purpose. ugly because no one was steering. impeccable's entire reason for existing.
- **POLISH** — accidentally impeccable. centered. soft. rounded. tasteful. could ship on a saas landing page.

audit against BOTH lists below before you ship. mark each item PASS, FAIL, or N/A. anything FAIL = start over.

---

## THE SLOP CHECK

things that look anti-design but are actually the model giving up.

| # | symptom | why it's slop |
|---|---|---|
| 1 | random rotations on every card | "diagonal flow" is one authorized break, used on ONE element, ≤6°. every card rotated = chaos as wallpaper |
| 2 | clashing colors with no contrast check | clash without legibility = bad eyesight, not anti-design |
| 3 | broken type on body copy | Carson moment is ONE per page on a headline. broken paragraphs = unreadable, not radical |
| 4 | gradient that's clearly meant to be "edgy" (lime → magenta smooth blend) | smooth gradient is the saas tell. anti-design uses HARD STOPS or no gradient |
| 5 | every motif used everywhere | Memphis motifs are rationed 2–3 per section. wall-to-wall squiggles is decoration, not statement |
| 6 | "ugly" font picked because it's ugly (Comic Sans for shock value) | system fonts only. Comic Sans is internet nostalgia, not a school. don't reach for it unless the school is zine/DIY explicitly |
| 7 | inaccessibility on functional surfaces | navigation, forms, errors must hold AA. anti-design as exclusion is cruelty, not authorship |
| 8 | "experimental" layout where nothing aligns to anything | grid exists, then breaks at FOUR authorized points. anything else is soup |
| 9 | five different schools on one page | pick ONE school per page (Lacquer is a fused house style — different thing) |
| 10 | irony as the only register | Lacquer / Memphis / Carson are SINCERE about their lineage. ironic 90s is a separate register and rarely works |
| 11 | dark mode that's just inverted colors | dark mode is a different school if you do it. don't toggle. |
| 12 | text on a photographic background with no contrast scrim | you have a palette. use it. photographs as background fills are a saas reflex. |

---

## THE POLISH CHECK

things that smell like impeccable's house. if any of these appear in your output WITHOUT explicit anti-design recontextualization, you failed.

| # | tell | what to do instead |
|---|---|---|
| 1 | centered hero with subtle gradient background | left-aligned headline overflowing the left edge, solid color block behind, no gradient |
| 2 | "Get started →" with chevron CTA | bare verb in shouter font: `START.` or refusal: `DON'T.` no chevron. no arrow. |
| 3 | Inter / Geist / SF Pro Display / Söhne / Suisse | Times New Roman OR Georgia paired with Arial Black OR Impact. system fonts only |
| 4 | `border-radius: 0.5rem` or any non-zero | `border-radius: 0`. zero. not 2px. zero. |
| 5 | `box-shadow: 0 1px 3px rgba(0,0,0,0.1)` | `box-shadow: 8px 8px 0 0 #000` — hard offset, palette color, no blur |
| 6 | three-column feature grid | full-bleed asymmetric blocks, butted-up, irregular widths (17/83 or 31/69) |
| 7 | testimonial carousel | static wall of quotes at clashing sizes, half-overlapping, no autoplay |
| 8 | "trusted by" logo strip in grayscale | full color, mismatched scales, deliberately uneven baselines, OR just delete it |
| 9 | dark mode toggle | if dark exists, it's a different page in a different school. no toggle. |
| 10 | `padding: 4rem` "for breathing room" | `padding: 1rem` max. content crowds. |
| 11 | `text-wrap: balance` on headlines | let them wrap raggedly. orphans live here. |
| 12 | `transition: all 0.3s ease` | snap. `transition: none` or step-easing only. |
| 13 | hover state that fades opacity 0.8 | hover state SNAPS to inverted palette colors |
| 14 | "Learn more" link in palette-blue underline | `WHY` or `MORE` in shouter font, no underline, color block behind |
| 15 | grayscale `#666` body text | black or paper-white. no gray. |
| 16 | `#FFFFFF` page background | `#F4F0E6` paper-white, or a color block from the palette |
| 17 | purple gradient `#8b5cf6 → #ec4899` | banned. all such gradients banned. |
| 18 | "How it works" three-step explainer with icons | replace with a single block of text. or delete. or rewrite as a manifesto fragment. |
| 19 | rounded badge / pill / tag | rectangle. zero radius. solid border. |
| 20 | section dividers (`<hr>` with custom styling, diagonal clip-path) | sections butt up. hard color change is the divider. no `<hr>`. |
| 21 | "skeleton loader" with shimmer animation | hard color block in palette acid hue. no animation. |
| 22 | floating action button | banned. all floating UI is impeccable's reflex. |
| 23 | breadcrumb component | if you need breadcrumbs, the IA is wrong. fix the IA. |
| 24 | "AI-generated landing page" energy (you'll know) | start over. seriously. |

---

## THE FINAL QUESTION

before shipping, ask: **could this appear on a Y Combinator company's homepage in 2024?**

if yes — POLISH FAIL. start over.

before shipping, ask: **could this be mistaken for a broken page?**

if yes — SLOP FAIL. start over.

the gap between those two is where unimpeccable lives.
