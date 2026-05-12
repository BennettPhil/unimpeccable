---
description: take a polished page and break it, in the locked school. preserve function.
argument-hint: <file-path or URL>
---

read the source. if URL, fetch and read.

audit pass.

1. run the POLISH check from `anti-patterns.md` against the source.
2. list every tell found, with line numbers or selectors.
3. note which surfaces are functional (nav, forms, errors, primary CTAs). those must NOT lose function.

ruin pass.

1. apply replacements from the POLISH table in `anti-patterns.md`. one-for-one.
2. introduce school-specific elements from `schools/<locked>.md`:
   - palette swap (drop the saas palette, install the school's)
   - type swap to workhorse + shouter
   - structure: butt-join sections, zero radius, hard shadows
   - one carson moment max
   - 2 to 3 motifs per section max
3. preserve every functional surface. AA contrast still holds. keyboard-reachable. focus rings still visible.

deliver.

- modified file in place (or a new file at `<original>.ruined.html` if URL source).
- summary: tells replaced, locations, what was preserved, what was added.
- count of tells found, count remaining (should be zero).

refuse politely.

if the source is already anti-design, tell the user it doesn't need ruining. recommend `audit` or `shred` instead. don't pile on chaos.

if the source has zero structure to begin with (no real layout, no real type system), tell the user to fix the structure first. you can't ruin what isn't built.
