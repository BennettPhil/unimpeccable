---
description: build a full anti-design page from a brief, in the locked school
argument-hint: <brief describing the page>
---

run the four-layer loop. no shortcuts.

prep.

1. confirm a school is locked. if not, default to lacquer and announce.
2. read in order if not already in context:
   - `MANIFESTO.md`
   - `anti-patterns.md`
   - `schools/<locked>.md`
   - `references/clashing-color.md`
   - `references/broken-grid.md`
   - `references/discordant-type.md`
3. read on-demand as the build needs them:
   - `references/twitch-motion.md` if there's any motion
   - `references/hostile-interaction.md` if there are buttons, forms, links
   - `references/defiant-responsive.md` if the page needs mobile
   - `references/counter-writing.md` for any generated copy

build, in this order. never reorder.

1. STRUCTURE. brutalist scaffolding. full-bleed, butt-joined blocks, zero radius, 3 to 6 px borders, hard offset shadows. set the grid before breaking it.
2. TYPE. workhorse + shouter. abuse the shouter at extreme sizes. body in workhorse at 18 to 20 px, line-height 1.35.
3. COLOR / PATTERN. palette set locked from the school. 2 to 3 memphis motifs per section, never more. fills are solid, not tints.
4. TEXTURE. last. halftone or grain overlay at 4 to 12 % opacity, multiply blend mode. one per page.

ration.

- one carson moment per long page, never more.
- 2 to 3 motifs per section, never more.
- one signature motion moment, never more.

audit before delivering.

- SLOP check: run the slop list in `anti-patterns.md`.
- POLISH check: run the polish list in `anti-patterns.md`.
- AA contrast on every functional surface.
- could it ship on a YC homepage? if yes, start over.
- could it be mistaken for broken? if yes, start over.

deliver.

- single HTML file with inline CSS in `<style>`.
- system fonts only (zine school webfont exception applies if school is zine-diy).
- no JS unless explicitly justified (a single carson-cycle marquee or step-eased reveal can be inline JS).
- viewport meta included.
- `prefers-reduced-motion` honored.
- HTML comments only at major section boundaries. nothing chatty.
