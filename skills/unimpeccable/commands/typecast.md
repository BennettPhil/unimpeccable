---
description: pick a 2-font type system from system fonts only. set the scale.
argument-hint: <optional: school-override>
---

read `references/discordant-type.md`.

steps.

1. pick the workhorse:
   - `"Times New Roman", Times, serif` (default)
   - `Georgia, serif`
   - `"Courier New", Courier, monospace` (only in zine-diy school)
2. pick the shouter:
   - `"Arial Black", "Helvetica Inserat", Impact, sans-serif` (default)
   - `Impact, "Helvetica Inserat", sans-serif`
   - `"Comic Sans MS", cursive` (only in zine-diy school, only ironically, only if user opted in)
3. confirm neither is on the ban list. Inter, Geist, SF Pro, Söhne, Suisse, Helvetica Neue, Roboto, Open Sans, Lato, Montserrat, Poppins, Manrope, Plus Jakarta Sans, DM Sans, DM Serif. if user asked for one, push back once.
4. set the scale:
   - hero: `clamp(72px, 18vw, 280px)`, line-height `0.85`, letter-spacing `-0.03em`
   - section heading: `clamp(48px, 8vw, 120px)`
   - body: 18 to 20 px, line-height `1.35`
   - captions: 14 to 16 px
5. assign one carson move type for the page. mid-word break, overlap pair, wrong-font paragraph, runaway leading, color-jumping word, or flipped baseline. exactly one. write it down.

deliver.

- a CSS block defining the font system and scale:
  ```css
  :root {
    --workhorse: "Times New Roman", Times, serif;
    --shouter: "Arial Black", "Helvetica Inserat", Impact, sans-serif;
  }
  body { font-family: var(--workhorse); font-size: 18px; line-height: 1.35; }
  h1.hero { font-family: var(--shouter); font-size: clamp(72px, 18vw, 280px); line-height: 0.85; letter-spacing: -0.03em; text-transform: uppercase; }
  h2 { font-family: var(--shouter); font-size: clamp(48px, 8vw, 120px); line-height: 0.85; letter-spacing: -0.03em; text-transform: uppercase; }
  ```
- one line naming the carson move reserved for this page.
- one line confirming neither font is on the ban list.
