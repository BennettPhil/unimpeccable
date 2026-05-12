# Y2K / Dirtstyle

two related but distinct lineages, fused here for convenience:

- **Y2K (1998–2003)** — frutiger aero, brushed metal, chrome, lens flare, sky-and-grass desktops, glass UI before glassmorphism, Winamp / WMP visualizers, MSN Messenger, Bonzi Buddy energy
- **dirtstyle (early-2000s)** — the digital-dirt graphic design of Designers Republic, Buffalo, Build, Hudson-Powell, Carson-adjacent but 5 years later and more computer-rendered

both share: maximalism, layered imagery, digital nostalgia, comfort with low-resolution / aliased / artifacted visual elements.

this is the **hardest school to do well.** the slip into pastiche is fast. nostalgia kitsch is not anti-design — it's a costume.

## VISUAL MARKERS

- chrome / brushed metal gradients (use HARD STOP gradients only, not smooth)
- lens flares on UI elements (rationed — one per page max)
- low-resolution photographic textures
- aliased / jagged text effects ("3D" text with hard pixel edges)
- iridescent / oil-slick color overlays
- transparency / glass effects WITHOUT impeccable-style smooth blur
- mixed digital nostalgia artifacts: dial-up sounds (as text references), AIM-era window chrome, MS Sans Serif rendered at the wrong size
- "info-dense" hud-style layouts with brackets, gauges, registration marks

## PALETTE

two sub-modes. pick ONE per page.

### sub-mode A — frutiger aero (clean Y2K)
- sky blue `#7DBDFF`
- grass green `#7FCC4A`
- chrome silver `#D8D8D8` (used in HARD STOP gradient with `#FFFFFF` only)
- glass cyan `#A0E6F2`
- true black `#000000`
- one accent: hot magenta `#FF2E93`

### sub-mode B — dirtstyle (dirty Y2K)
- charcoal `#1A1A1A`
- safety orange `#FF6A00`
- toxic green `#5CFF00`
- iridescent purple `#9D00FF`
- newsprint `#E8E2D0`
- one accent: riso red `#FF4438`

## TYPE

- workhorse: Times New Roman OR Courier New (the early-2000s default web aesthetic)
- shouter: Arial Black OR Impact
- **decorative ONLY**: a single element per page may use a "3D extruded" treatment via CSS:
  ```css
  .y2k-3d {
    text-shadow:
      1px 1px 0 #000,
      2px 2px 0 #000,
      3px 3px 0 var(--accent),
      4px 4px 0 var(--accent);
  }
  ```
- never use a webfont that "looks Y2K" (Bodoni Moda, Druk, etc.) — system fonts abused into Y2K territory is the constraint

## STRUCTURE

- HUD-style overlays: brackets in corners (`⌐ ¬ └ ┘`), registration marks, crosshairs
- info panels with visible borders, sometimes nested inside other panels
- floating UI windows (rectangles with title bars styled like Windows 2000 / MSN Messenger)
- mixed-media layouts: photographs + 3D-rendered objects + raw HTML + chrome buttons
- layouts feel "instrumented" — like an interface from a movie that never existed

## DIRTSTYLE-SPECIFIC ELEMENTS

- typography crashes through layered photo collage
- registration marks, ISO standard graphics, schematic-drawing energy
- vector-art "characters" (low-poly humans, abstract figures from Designers Republic's lexicon)
- a numerical / data-driven aesthetic: serial numbers, version stamps, technical-looking captions

## RULES SPECIFIC TO THIS SCHOOL

- ration the chrome / lens flare. ONE per page. not five.
- HARD STOP gradients only. no smooth metal blends.
- the page should evoke an artifact from a specific year (1999, 2001, 2003) — pick one, commit to its constraints.
- avoid the obvious pastiche trio: clippy + AIM + Windows XP wallpaper. these are nostalgia memes, not anti-design.
- if you're tempted to add a "Y2K palette" gradient because it looks cool, you're slipping into kitsch. stop.
- this school requires more discipline than any other — write down WHAT YEAR and WHAT ARTIFACT you're channeling. if you can't, you're doing nostalgia, not Y2K.

## NAMED REFERENCES

- **Designers Republic (1986–2009)** — sheffield, Sheffield, dirtstyle's headquarters. Wipeout game UI, Pop Will Eat Itself sleeves
- **Buffalo (1995–2009)** — David Carson-influenced, more digital
- **Hudson-Powell (2000s)** — typography + 3D-render energy
- **Microsoft Windows XP "Bliss" wallpaper era (2001–2007)** — frutiger aero peak
- **early Apple aqua UI (2000)** — glass / chrome / drop shadows
- **MSN Messenger 6.0, ICQ 99** — chat-window chrome
- **dirty design / "the cult of the ugly"** — Steven Heller's essays on the era

## WHEN TO REACH FOR THIS SCHOOL

- music / culture sites with electronic / experimental music
- interface-fiction projects (sites pretending to be from a parallel-history era)
- vaporwave-adjacent but more grounded
- design-history / archive sites
- a single landing page that's CONSCIOUSLY a period piece

## WHEN NOT TO

- general commercial sites (kitsch risk too high)
- saas (catastrophic mismatch)
- when the user wants "current" anything — Y2K is intentionally non-current
- any context where the audience is too young to have nostalgia for this era (Y2K depends on cultural memory)

## SELF-CHECK

- did I pick a specific year and artifact to channel?
- is the page sub-mode A (clean) or sub-mode B (dirty), not a mix?
- are chrome / lens flares rationed to ONE per page?
- are gradients HARD STOP, not smooth?
- did I avoid the obvious pastiche memes (clippy, XP bliss, AIM nudge)?
- does this look like an artifact, or a nostalgic reference to one? the first is good. the second is kitsch.
