# Zine / DIY

photocopied, stapled, handed to you. riot grrrl chapbooks, punk newsletters, queercore manifestos, conspiracy pamphlets from the 70s, abstinence brochures from the 80s, art school dissertations photocopied at a Kinko's. xerographic culture.

the zine aesthetic is **handmade and reproduced.** every artifact carries the marks of its production: staple holes, paste-up edges, photocopier streaks, handwritten captions, typewriter text, halftone dot patterns from screened photographs.

translating this to the web requires honesty about the medium. don't fake paper. evoke it.

## VISUAL MARKERS

- black ink, newsprint paper
- halftone-dotted photographs
- handwritten captions and corrections in margin
- typewriter text (monospace, irregular spacing)
- ransom-note headlines (mixed-font, mixed-size letters)
- staple marks, tape strips, photocopier streaks
- scanned-in collage elements
- multi-column text with no consistent grid
- visible page numbers, dates, "FREE" stamps
- ALL CAPS shouting

## PALETTE

- charcoal `#1A1A1A` (the ink)
- newsprint `#E8E2D0` (the paper)
- optional accent: riso red `#FF4438` OR riso blue `#0078BF` (one only, for "second pass" effect)

monochrome black-on-newsprint is the default. riso is for "this is a special issue."

## TYPE

zine is the one school where the font allow-list expands:

- `"Courier New", Courier, monospace` (typewriter) — workhorse
- `"Times New Roman", Times, serif` — secondary workhorse, for "borrowed from a real publication" feel
- `Impact, "Arial Black", sans-serif` — shouter, for ALL CAPS headlines
- handwritten via web font: `"Permanent Marker", "Reenie Beanie"` from Google Fonts — **the one exception to the no-webfonts rule, allowed for zine school only, for handwritten captions**

ransom-note mode: when you need it, set every letter or word in a different font / size / weight inline, using `<span>` per character or word.

example ransom-note CSS pattern:
```css
.ransom > * {
  display: inline-block;
  font-family: serif;
  text-transform: uppercase;
}
.ransom > *:nth-child(2n) { font-family: monospace; transform: rotate(2deg); }
.ransom > *:nth-child(3n) { font-family: sans-serif; transform: rotate(-3deg); font-size: 1.4em; }
.ransom > *:nth-child(5n) { font-family: serif; font-weight: 900; }
```

## STRUCTURE

- multi-column flow (2–3 columns), but the columns are RAGGED — content overflows, captions wander
- elements appear "pasted in": rectangles of content with slight rotation (2–6°), uneven margins
- visible "tape" strips (4px thick rotated paper-white rectangles) attaching elements
- staple marks: small black dots in pairs at the top of the page
- photographs are halftoned via SVG filter or CSS:
  ```css
  .halftone { filter: contrast(2) grayscale(1); }
  ```
- page numbers in corners, plain
- "PRINTED [DATE]" or "ISSUE #X" markers visible

## RULES SPECIFIC TO THIS SCHOOL

- the page should look like a SCAN, not a paper. don't fake torn edges with `border-radius` or fancy SVG. use a high-contrast halftone overlay across the whole page.
- handwritten elements are RARE — one or two per page, not throughout. they're the personal voice.
- typewriter monospace is the default workhorse, not the exception.
- the texture overlay opacity goes UP in this school: `8–18%`, vs. Lacquer's `4–12%`.
- everything is reproducible — the page should look like it could be printed and photocopied without losing meaning. this means: high contrast, no subtle gradient, no fine detail that wouldn't survive a Xerox.
- mistakes are GOOD: a misaligned line, a smudge, a struck-through-and-corrected word.

## MICROCOPY VOICE

in zine school, the voice gets more personal:
- first-person OK ("i think this is a problem")
- direct addressing ("listen.")
- rhetorical questions ("why does this exist")
- ALL CAPS shouting bursts
- handwritten correction strikethrough: <s>this was wrong</s> THIS IS RIGHT

## NAMED REFERENCES

- **riot grrrl zines (1991+)** — Bikini Kill, Bratmobile circles
- **Punk Planet, Maximum Rocknroll (1980s–2000s)** — long-form punk publications
- **Whole Earth Catalog (1968–1972)** — pre-zine influence, similar paste-up aesthetic
- **conspiracy / fringe pamphlets** — the visual energy of someone who NEEDED to tell you this
- **Tibor Kalman, M&Co work (1980s–90s)** — high-design zine-adjacent
- **art school thesis books** — the genre that influenced 2010s indie zine revival

## WHEN TO REACH FOR THIS SCHOOL

- manifesto pages, essays, position papers (overlaps with web brutalism's cold honesty, but warmer and handmade)
- "story behind the project" pages
- newsletter archives
- small community / collective sites
- art project documentation

## WHEN NOT TO

- product / commercial pages (the homemade-ness reads as untrustworthy)
- enterprise contexts
- e-commerce
- anywhere the user is paying you money — zine school feels free, and that bleeds into "is this real"

## SELF-CHECK

- is the page black ink + newsprint, with optional ONE accent?
- is there a halftone/grain overlay at 8–18% opacity?
- is at least one element "pasted in" (rotated 2–6°, slightly offset)?
- is at least one element handwritten or ransom-note style?
- are there visible production marks (page numbers, dates, "ISSUE #X")?
- does it look like it could be photocopied without losing meaning?
