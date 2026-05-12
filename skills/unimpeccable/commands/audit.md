---
description: scan a file for impeccable-style polish tells AND slop tells. report counts and locations. do not modify.
argument-hint: <file-path>
---

read the source. read `anti-patterns.md`.

run two passes.

pass 1. SLOP CHECK.

go through the 12 slop symptoms in `anti-patterns.md`. for each:
- symptom number and description
- locations found (line numbers, selectors)
- severity: FAIL, PASS, or N/A
- one-line note on what would fix it

pass 2. POLISH CHECK.

go through the 24 polish tells in `anti-patterns.md`. for each:
- tell number and description
- locations found
- the prescribed replacement from the POLISH table
- severity: FAIL, PASS, or N/A

deliver.

a structured report.

```
=== SLOP CHECK ===
1. random rotations on every card             [PASS]
2. clashing colors with no contrast check     [FAIL]
   - line 142: white-on-acid-lime button label, contrast 1.8
   - fix: swap to black-on-acid-lime (contrast 11.2)
...

=== POLISH CHECK ===
1. centered hero with subtle gradient         [FAIL]
   - line 18: <section class="hero center">
   - fix: left-aligned headline overflowing left edge, solid color block, no gradient
2. "Get started →" with chevron               [PASS]
...

=== SUMMARY ===
SLOP:   2 FAIL, 8 PASS, 2 N/A
POLISH: 6 FAIL, 16 PASS, 2 N/A
top 5 urgent fixes:
  1. ...
  2. ...
ship-ready: NO. start over on type system and palette.
```

rules.

- do not modify the file. audit only.
- if asked to fix, recommend `downgrade` (polish tells) or `ruin` (full pass).
- be honest. if the file is already strong unimpeccable, say so. don't manufacture findings.
