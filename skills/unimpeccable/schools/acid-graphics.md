# Acid Graphics

2018 to present. Brian Roettinger, Tom Galle, Jonathan Castro Alejos, Bunny Rogers, Yu Hong Hu. the "acid" movement in contemporary graphic design: hyperaggressive maximalism, 3D rendered objects, chromatic aberration, mesh gradients used as weapons, oversized type with deliberate distortion.

the rave poster, the experimental music release, the gallery announcement, the techno club night. visual energy as the message itself.

## THE WARNING (READ FIRST)

this school is the most laundered of any in unimpeccable. "acid design" has been absorbed into mainstream startup branding, web3 marketing, Behance shots, and Awwwards winners. the templated version is everywhere.

unimpeccable's acid is NOT the laundered acid. specifically:

- **NOT** iridescent / oil-slick / pastel pearl palettes (the laundered tell)
- **NOT** chrome glassmorphism wrapping every element
- **NOT** centered-symbol-with-orbital-text composition (the Spotify Wrapped template)
- **NOT** "techy" — that's the laundered version's emotional position

unimpeccable's acid is **ugly on purpose, abrasive, club-poster energy, not gallery-shop energy.** if your output could appear on the homepage of a generative-art NFT marketplace, you failed. start over.

## VISUAL MARKERS

- chromatic aberration on type (RGB channel split: a red shadow offset one direction, cyan the other)
- 3D rendered abstract objects (metallic spheres, twisted toruses, melted liquid blobs, extruded type)
- aggressive mesh gradients — but the colors clash, they don't blend nicely
- oversized display type, often `transform: scaleY(2.4)` stretched or `font-stretch: ultra-condensed` crushed
- type-as-object: typography behaves like a sculpture (3D extrusion via stacked text-shadow)
- ASCII / monospace text fragments overlaid on dense compositions
- floating UI fragments (window chrome, sliders, dropdowns) used as decoration
- liquid blob shapes via SVG path or `border-radius: 47% 53% 60% 40% / 35% 65% 50% 50%`
- dense, busy compositions. no breathing room. acid acid acid.

## PALETTE

one of two modes per page. pick.

### mode A — single acid dominant

one saturated dominant hue + true black + one accent. examples:
- toxic green `#5CFF00` + `#000000` + `#FF0000` accent
- electric blue `#1F51FF` + `#000000` + `#FFFF00` accent
- magenta `#FF2E93` + `#000000` + `#00FFFF` accent

the dominant hue fills 60 to 80% of the page. black is structure. accent is for ONE element only (a stripe, a 3D object, a chromatic aberration shadow).

### mode B — hard mesh gradient

ONE aggressive gradient per page, used as a section background or hero fill. it's NOT a soft impeccable gradient.

```css
background: conic-gradient(from 45deg, #5CFF00 0%, #FF2E93 25%, #000 50%, #1F51FF 75%, #5CFF00 100%);
```

or hard-stop linear:

```css
background: linear-gradient(90deg, #5CFF00 0% 49%, #FF2E93 51% 100%);
```

never smooth analogous gradients. never iridescent. never pastel pearl. those are the laundered tells.

## TYPE

unusual for unimpeccable: monospace is the workhorse here.

### workhorse

- `"Courier New", Courier, monospace` — default
- `"Andale Mono", monospace`
- `"Consolas", monospace`

monospace carries body, technical metadata, ASCII fragments, captions. the school feels computer-mediated, like the page was rendered by a terminal that knew it would be art.

### shouter

- `"Arial Black", Impact, sans-serif` at extreme sizes
- distortion is REQUIRED on at least one headline: `transform: scaleY(2.4)` or `transform: scaleX(0.6)` (stretched or crushed)
- or `font-stretch: ultra-condensed` if the system supports it on the shouter

### the chromatic aberration moment

ONE headline per page gets the RGB split treatment:

```css
.aberrant {
  color: #fff;
  text-shadow:
    -3px 0 0 #FF0000,
    3px 0 0 #00FFFF;
}
```

stronger version uses `mix-blend-mode: screen` on layered pseudo-elements. ration this to ONE headline per page in product register, one per major section in showcase register.

### type-as-3D

extruded type via stacked text-shadow:

```css
.extruded {
  color: #5CFF00;
  text-shadow:
    1px 1px 0 #000,
    2px 2px 0 #000,
    3px 3px 0 #000,
    4px 4px 0 #000,
    5px 5px 0 #000;
}
```

use once per page max. it's loud.

## STRUCTURE

dense. busy. every pixel does something.

- techno-poster composition: stacked, layered, overlapping content blocks
- floating UI fragments as decoration: rendered `<dialog>` shapes, fake buttons, fake input fields, all non-functional, all decorative
- liquid blob SVGs as background elements behind content
- ASCII text fragments inline with body content (like a manifest from a terminal):

```
[+] LOADED: section_2.acid
[+] PALETTE: toxic_green / black / red
[+] STATUS: ready
```

- type rotated to non-rectilinear angles (15°, 22°, -8°) when used decoratively
- often centered, but the center is dense not balanced — orbital satellites of content around the core

rules for keeping it un-laundered:

- never `border-radius: 9999px` (the rounded pill is the laundered acid tell)
- never `backdrop-filter: blur(20px)` glassmorphism on cards
- never an animated gradient that smoothly cycles hues (rainbow loop is web3)
- never a centered "logomark in a circle" composition

## DECORATION

- one 3D rendered object per major section. inline SVG can fake it (metallic gradients, fake highlights) or use placeholder asset slots for real renders.
- one aggressive gradient per page (or per major section in showcase register).
- one chromatic aberration headline per page (or per major section in showcase register).
- ASCII fragments throughout, as captions / metadata / chrome.
- liquid blob SVGs behind content, opacity 0.3 to 0.6, mix-blend-mode multiply or difference.

## MOTION

allowed:
- snap-flinch hover on cards (per `references/twitch-motion.md`)
- chromatic aberration intensifies on hover: the RGB offset grows from `±3px` to `±6px`. snap, not smooth.
- ambient tic on the 3D object (it jerks once every 10-20 seconds)
- ascii text "loading bars" that step-cycle through frames

banned:
- smooth rainbow gradient cycling
- smooth rotation of any element
- particle backgrounds, animated dot fields
- mouse-trail effects

## NAMED REFERENCES

- **Brian Roettinger / Hand Held Heart** — LA-based studio. Liturgy album covers. designed for Kanye's *Yeezus* sleeve (the Roettinger one, not the final). hyperaggressive type as the constant.
- **Tom Galle** — Belgium-based. work for Adidas, NTS, Vans, Vfiles. 3D objects + system type + aggressive color.
- **Jonathan Castro Alejos** — Peruvian designer. gallery and music identity work. high acid energy.
- **Bunny Rogers** — net artist. acid-adjacent through her web work.
- **NTS Radio identity** (Sam Drewett, Marius Hennig) — sometimes acid territory.
- **club night posters from any major city, 2019-present** — boiler room, sub club, berghain side rooms.
- **bandcamp pages for noise, harsh techno, experimental electronic** — frequently acid by accident
- **Yu Hong Hu, Studio Sans Nom** — recent acid practitioners

## WHEN TO REACH FOR THIS SCHOOL

- electronic music, club nights, festival pages, label sites
- experimental fashion brand pages (small labels, not luxury houses)
- exhibition / gallery announcements
- generative art / experimental web projects (within reason — see warning)
- anything that wants to feel CONTEMPORARY and aggressive without going corporate-techy

## WHEN NOT TO

- if you're reaching for this because it looks "modern" or "techy" — that's the laundered version. use neubrutalism, web brutalism, or geocities instead.
- saas
- mass-market e-commerce
- enterprise
- web3 / NFT marketing (this is what laundered the school in the first place; even if you do it well, the audience won't separate signal from slop)
- anywhere the audience reads "acid" as "edgy startup"

## SELF-CHECK

- is there exactly ONE aggressive gradient, ONE 3D object, ONE chromatic aberration headline (per page or per section depending on register)?
- is the type monospace as workhorse, not soft sans?
- did I AVOID iridescent / oil-slick / pearl / pastel palettes?
- did I AVOID `border-radius: 9999px` pills, glassmorphism, smooth gradient hue-cycle animations?
- did I AVOID the centered-logo-in-orbital-text composition?
- could this appear unmodified on a web3 marketing page? if yes, push uglier — system fonts, cheaper textures, more abrasive type distortion.
- does it feel like a club poster, or a SaaS landing page? club poster wins. saas fails.
