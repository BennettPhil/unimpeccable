---
description: layout-only pass. fragment, overlap, off-grid, diagonal. do not touch type or palette.
argument-hint: <file-path>
---

read the source. note the current type system and palette. these stay.

read `references/broken-grid.md`.

apply only the four authorized breaks. nothing else.

1. asymmetric split (17/83, 31/69, 38/62, 71/29). one or two per page.
2. full-bleed overlap. a block extends past its section by 60 to 120 px. one or two per page, max.
3. diagonal flow. rotate one element 2 to 6 degrees. if you rotate a second, opposite direction.
4. negative indent. pull a headline or color block out of its column. headlines and decoration only, never functional elements.

rules.

- do not change fonts.
- do not change palette.
- do not change copy.
- functional elements (nav, forms, buttons) keep working.
- if the existing layout already uses these breaks, don't pile on. tell the user.

deliver.

- modified file with structure-only edits.
- summary: which of the four breaks were applied, where, with line numbers or selectors.
- count of breaks added. ideally three or four, never more than six per page.
