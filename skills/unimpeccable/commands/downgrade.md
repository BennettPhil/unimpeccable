---
description: scan for impeccable-style defaults and replace each with its anti-design counterpart, in place.
argument-hint: <file-path>
---

read the source. read `anti-patterns.md`.

scan.

go through every entry in the POLISH list. for each, scan the file for matches. record line numbers and selectors.

replace.

for each match, apply the replacement from the POLISH table:

- centered hero with subtle gradient → left-aligned headline overflowing left edge, solid color block, no gradient.
- `Get started →` with chevron → bare verb in shouter, no chevron.
- Inter / Geist / SF Pro / Söhne / Suisse / Helvetica Neue → Times + Arial Black.
- `border-radius` non-zero → `border-radius: 0`.
- `box-shadow: 0 1px 3px rgba(0,0,0,0.1)` (or any soft shadow) → hard offset block-shadow, palette color, no blur.
- three-column feature grid → asymmetric butt-joined blocks (17/83 or 31/69).
- testimonial carousel → static wall of quotes at clashing sizes.
- grayscale "trusted by" strip → full color, mismatched scales, OR delete.
- `transition: all 0.3s ease` → `transition: none` or step-easing.
- hover state that fades opacity → snap to inverted palette colors.
- gray body text `#666` → black or paper-white.
- `#FFFFFF` background → paper-white `#F4F0E6` or a palette color block.
- purple gradient → banned. delete the gradient entirely.
- rounded badge / pill / tag → rectangle, zero radius, solid border.
- `<hr>` section dividers → hard color change between butt-joined sections.
- skeleton loader with shimmer → hard color block, no animation.
- floating action button → banned. delete.
- breadcrumb component → if needed, the IA is wrong. flag, don't replace.

rules.

- apply in place. preserve function on every functional surface.
- if a tell is load-bearing for functionality (e.g. a soft shadow on a dropdown that signals overlay), replace the visual while preserving the affordance.
- never break the page's primary task.

deliver.

- modified file.
- a diff summary. every tell found, every replacement made, with line numbers.
- counts: tells found, replacements applied, tells remaining (should be zero).
- a final note: the page now reads as `<locked-school>`. confirm the school suits the page's purpose, or recommend a switch.
