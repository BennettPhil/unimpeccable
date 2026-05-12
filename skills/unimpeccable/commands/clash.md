---
description: generate a lacquer-grade discordant palette in the locked school
argument-hint: <optional: set-name or hue-anchor>
---

read `references/clashing-color.md`.

if a school is locked, read `schools/<locked>.md` for the school's allowed palette sets.
if no school locked, default to lacquer and offer sets A through D.

palette rules.

- 3 to 5 acid hues (HSL saturation ≥ 80 %).
- one true black.
- one tinted neutral. paper-white `#F4F0E6`, never `#FFFFFF`.
- no analogous hues. if two sit next to each other on the wheel, drop one.
- no monochrome.
- no pastels.
- no gray.
- one clash pair drives the palette. examples:
  - lime × magenta
  - cyan × orange
  - riso red × riso blue
  - yellow × cobalt
  - brat green × bubblegum
- the purple ban (`#8b5cf6` and neighbors 250 to 270° hue) holds. if the user requests purple, push back once. confirm before using `#9D00FF`.

deliver.

- a CSS custom-properties block ready to paste:
  ```css
  :root {
    --acid-1: #...;
    --acid-2: #...;
    --acid-3: #...;
    --ink: #000;
    --paper: #F4F0E6;
  }
  ```
- one line naming the clash pair that drives the palette.
- a contrast matrix. which combinations hold AA for functional text. which are decoration-only.
- one paragraph on how to deploy: which hue is the section block backgrounds, which is the headline color, which is the single accent.
