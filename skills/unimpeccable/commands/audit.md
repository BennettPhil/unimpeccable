---
description: scan a file for slop tells, polish tells, AND timidity tells. report counts and locations. do not modify.
argument-hint: <file-path>
---

read the source. read `anti-patterns.md`. read `references/page-register.md` and determine which register the page is in (or should be in — long-scroll multi-school pages should be SHOWCASE; if they're built in PRODUCT register they will fail timidity).

run three passes.

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

pass 3. TIMIDITY CHECK.

go through the 8 timidity symptoms in `anti-patterns.md`. critical for long-scroll pages. for each:
- symptom number and description
- evidence (e.g. "all 8 cards are 360x320, line 142-160" / "only 1 carson moment on a 4-screen page" / "every section sits in its own horizontal stripe with butt-joined edges")
- severity: FAIL, PASS, or N/A
- one-line note on the escalation that would fix it

deliver.

a structured report.

```
=== REGISTER ===
inferred: SHOWCASE (long-scroll, multiple schools displayed)
built in: PRODUCT (one school wallpapers everything)
→ this is the root cause of most timidity findings below.

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
...

=== TIMIDITY CHECK ===
1. tidy stack of horizontal stripes           [FAIL]
   - every section ends at a flat horizontal line. no section bleed anywhere.
   - fix: extend memphis section's terrazzo into the next section by 120px.
2. sibling items share dimensions             [FAIL]
   - 8 school cards at identical 360x320. line 234-340.
   - fix: scale-variation across siblings. lacquer wide, web-brutalism naked, carson small-and-overlapping, zine rotated, y2k browser-chrome-wrapped.
...

=== SUMMARY ===
SLOP:     2 FAIL, 8 PASS, 2 N/A
POLISH:   6 FAIL, 16 PASS, 2 N/A
TIMIDITY: 5 FAIL, 2 PASS, 1 N/A   ← the urgent category
top 5 urgent fixes (timidity first):
  1. ...
  2. ...
ship-ready: NO. timidity is the dominant failure. consider switching register from PRODUCT to SHOWCASE.
```

rules.

- do not modify the file. audit only.
- if asked to fix, recommend `downgrade` (polish tells) or `ruin` (full pass including timidity escalation).
- be honest. if the file is already strong unimpeccable, say so. don't manufacture findings.
- if the page is in the wrong register, say so prominently. wrong register is the #1 cause of timidity failure and most other timidity findings are downstream of it.
