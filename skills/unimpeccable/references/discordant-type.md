# discordant-type

type is not a "system." type is an argument. pick two fonts that don't get along and make them work the same page.

## THE TWO SLOTS

every page has exactly two fonts. one workhorse, one shouter. never three. never four.

ONE exception: a `<pre><code>` block containing literal code may use `"Courier New", Courier, monospace`. this is the only allowed third slot, and only for actual code-display where character alignment matters. it does NOT extend to:
- stylistic monospace metadata text
- inline `<code>` outside a `<pre>` (use the workhorse with a visual treatment like inverted color block)
- captions or footer text wanting a "technical" feel
- anything that isn't literal code

if you find yourself reaching for monospace because it "feels right," that's the saas reflex. the workhorse is the workhorse.

### workhorse (body, paragraphs, labels, captions)

pick ONE of:

- `Times New Roman, Times, serif`
- `Georgia, serif`
- `"Courier New", Courier, monospace` — only in zine/DIY school

### shouter (headlines, section labels, buttons)

pick ONE of:

- `"Arial Black", "Helvetica Inserat", Impact, sans-serif`
- `Impact, "Helvetica Inserat", sans-serif`
- `"Comic Sans MS", cursive` — ONLY in zine/DIY, ONLY ironically, ONLY if user opted in

never mix two serifs. never mix two sans. they must argue.

## THE BAN LIST

these fonts do not appear in unimpeccable output. ever.

- Inter (impeccable's house)
- Geist (Vercel's house)
- SF Pro / SF Pro Display
- Söhne, Söhne Mono
- Suisse Int'l
- Helvetica Neue (Helvetica is fine — Helvetica Neue specifically is the AI-slop sans)
- Roboto
- Open Sans
- Lato
- Montserrat
- Poppins
- Manrope
- Plus Jakarta Sans
- DM Sans / DM Serif
- any font you've seen on a Webflow template

if a user asks for one, push back once. if they confirm, do it but flag that it weakens the school.

## SIZES

abuse the shouter at the top of the page. specifically:

```
hero headline:    clamp(72px, 18vw, 280px)
section heading:  clamp(48px, 8vw, 120px)
body:             18–20px
captions:         14–16px
```

- line-height on hero: `0.85`
- line-height on body: `1.35` (not `1.5`. comfortable is the enemy.)
- letter-spacing on shouter: `-0.03em` (tight, crushed)
- letter-spacing on workhorse body: `0` (default)
- letter-spacing on ALL-CAPS labels: `0.04em` only

## TYPE CASE

- body: sentence case
- headlines: lowercase by default, ALL CAPS for one or two emphasis bursts per page
- buttons: ALL CAPS, short verbs
- labels: lowercase
- never title case. title case is corporate.

## THE CARSON MOMENT

ration scales with register (see `references/page-register.md`).

- PRODUCT register: one per page.
- SHOWCASE register: one per ~1000px of scroll. a typical long manifesto page gets 3 to 5 carson moments total, distributed across sections.
- ARTIFACT register: per the school's rules. carson-raygun school allows 2 to 3 per page.

zero on a long page is a TIMIDITY failure. more than the ration is a SLOP failure.

pick ONE option per moment.

1. **mid-word break** — `word-break: break-all` on one headline only. let `INSTAL` wrap to `LATION` mid-word.
2. **overlap pair** — two headlines positioned over each other at 60% opacity each. read separately by squinting.
3. **wrong-font paragraph** — set ONE paragraph in the shouter at 14–16px. uncomfortable to read; that's the point.
4. **runaway leading** — `line-height: 2.8` on one stanza. it's a poem now.
5. **color-jumping word** — one word in a line set in a different palette color from the rest.
6. **flipped baseline** — one heading set with `writing-mode: vertical-rl` along a section edge.
7. **floating ghost word** — a single word in 400–600px Impact, paper-white, opacity 0.08–0.12, behind everything, rotated -8 to -4 degrees, hard cropped by the viewport. the page mutters something at the user. one of these is permitted per long page in addition to the per-section moments above.

never two Carson moments visible AT THE SAME TIME on screen. distribute them down the scroll. never on functional UI (nav, form fields, error messages).

## TEXT BLOCKS

- line length: 50–75ch. wider is fine, narrower is fine, "comfortable" 65ch is impeccable's default — don't aim for it specifically.
- text-wrap: `text-wrap: pretty` is acceptable. `text-wrap: balance` is banned (faked even line lengths read as polish).
- hyphenation: off. let it overflow. let it wrap raggedly.
- justification: left-align. never `text-align: justify` (river-of-whitespace energy from corporate annual reports).

## DECORATIVE TYPE

palette colors are fair game for headlines. body stays black (or paper-white on dark). these treatments are allowed on display type only:

- color block behind the heading (rotated 2–6°), heading itself flat
- underline that is a 4–8px solid color bar offset 4px below the text
- strikethrough at random words (use sparingly, max one per page)
- outlined type: `-webkit-text-stroke: 3px #000; color: transparent;` for ONE block per page

## THE MICRO-RULES

- no font weights between 400 and 700. you're either at 400 or at 900. middle weights are saas defaults.
- no italic body. italic is for emphasis bursts only, max one per paragraph.
- no font ligatures unless the school is zine (which doesn't have them anyway because system fonts).
- no variable font axis play. system fonts have fixed weights. that's the constraint.

## SELF-CHECK

- exactly two fonts?
- both from the system-font allow list?
- hero ≥ 72px on mobile, ≥ 280px on wide screens?
- letter-spacing tight on shouter?
- exactly ONE Carson moment, on a non-functional element?
- no title case?
- no banned fonts?
