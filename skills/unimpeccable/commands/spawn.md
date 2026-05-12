---
description: build a full anti-design page from a brief, in the locked school
argument-hint: <brief describing the page>
---

run the four-layer loop. no shortcuts.

prep.

1. confirm a REGISTER is locked. one of: PRODUCT (single anti-design page selling or operating one thing), SHOWCASE (long-scroll manifesto with multiple schools coexisting), ARTIFACT (period piece committed to one school and one specific year). if not locked, infer from the brief. if ambiguous, ASK before building. **wrong-register pages are the #1 cause of timidity failure.**
2. confirm a school is locked. if not, default to lacquer and announce. in SHOWCASE register, plan one school PER MAJOR SECTION, not one for the whole page.
3. read in order if not already in context:
   - `MANIFESTO.md`
   - `anti-patterns.md`
   - `references/page-register.md`
   - `schools/<locked>.md` (and each per-section school in showcase register)
   - `references/clashing-color.md`
   - `references/broken-grid.md`
   - `references/discordant-type.md`
4. read on-demand as the build needs them:
   - `references/twitch-motion.md` if there's any motion
   - `references/hostile-interaction.md` if there are buttons, forms, links
   - `references/defiant-responsive.md` if the page needs mobile
   - `references/counter-writing.md` for any generated copy

build, in this order. never reorder.

1. STRUCTURE. brutalist scaffolding. full-bleed, butt-joined blocks, zero radius, 3 to 6 px borders, hard offset shadows. set the grid before breaking it. in SHOWCASE register, apply at least one section bleed and one viewport extension. sibling items in a row MUST NOT share dimensions.
2. TYPE. workhorse + shouter. abuse the shouter at extreme sizes. body in workhorse at 18 to 20 px, line-height 1.35.
3. COLOR / PATTERN. palette from the school's set. motifs per ration table:
   - PRODUCT: 2 to 3 motifs per section
   - SHOWCASE: 3 to 5 motifs per major section
   - ARTIFACT: per the school
   fills are solid, not tints.
4. TEXTURE. last. halftone or grain overlay at 4 to 12 % opacity, multiply blend mode. one per page.

ration. these are FLOORS, not ceilings.

- carson moments: PRODUCT one per page, SHOWCASE one per ~1000px of scroll, ARTIFACT per the school. zero on a long page = timidity failure.
- motifs: per the table above. fewer than the floor = the section won't read as the school.
- signature motion: PRODUCT one per page, SHOWCASE one per major section.
- snap-flinch hover on cards: at least one set of these per page if cards exist.
- ambient tic on one element if the page has any motion at all.

audit before delivering. three passes.

- SLOP check: run the slop list in `anti-patterns.md`.
- POLISH check: run the polish list in `anti-patterns.md`.
- TIMIDITY check: run the timidity list in `anti-patterns.md`. critical for long-scroll pages.
- AA contrast on every functional surface.
- could it ship on a YC homepage? if yes, POLISH FAIL — start over.
- could it be mistaken for broken? if yes, SLOP FAIL — start over.
- if asked "make it more extreme," could you list five things? if yes, TIMIDITY FAIL — push further before shipping.

deliver.

- single HTML file with inline CSS in `<style>`.
- system fonts only (zine school webfont exception applies if school is zine-diy).
- no JS unless explicitly justified (a single carson-cycle marquee or step-eased reveal can be inline JS).
- viewport meta included.
- `prefers-reduced-motion` honored.
- HTML comments only at major section boundaries. nothing chatty.
