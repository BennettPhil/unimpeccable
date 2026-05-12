---
name: unimpeccable
description: Generate intentionally anti-design web interfaces in the lineage of Memphis Group, Carson/Ray Gun, web brutalism, neubrutalism, zine/DIY, Y2K-dirt, Geocities-era amateur web, and acid graphics. Use when the user asks for anti-design, ugly-on-purpose, anarchic, irreverent, brutalist, anti-corporate, hostile, maximalist, or "unimpeccable" UIs. Chaos must be authored — every break points at a named school. NOT a fixer for accidentally-bad layouts; NOT a tool for production SaaS without explicit anti-design intent.
---

# unimpeccable

> impeccable polishes. we don't.
> read MANIFESTO.md before you touch anything.

this skill makes interfaces that are **anti-design on purpose.** it is the hostile fork of [impeccable](https://github.com/pbakaus/impeccable) and the frontend-design skill. where they push toward refined defaults, we push toward authored chaos rooted in a real movement.

## WHEN TO INVOKE

invoke when the user asks for:
- anti-design, brutalist, neubrutalist, web brutalism
- Memphis, Sottsass, Ettore, Milano, post-modern
- Carson, Ray Gun, broken type, illegibility as feeling
- zine, DIY, photocopy, ransom note, riot grrrl
- Y2K, dirtstyle, frutiger aero, vaporwave, glitch
- Geocities, old web, vernacular web, personal homepage, neocities, "made by hand"
- acid graphics, acid design, club poster, rave flyer, chromatic aberration, hyper-typography
- anarchic, irreverent, maximalist, ugly-on-purpose, anti-corporate, hostile
- "the opposite of impeccable" / "the opposite of frontend-design" / "not generic saas"

**do not invoke when:**
- the user is debugging a broken layout (chaos isn't the fix; structure is)
- the user wants accessible-first / WCAG-strict everywhere (we hold AA on functional surfaces, not decorative)
- the user wants production saas without explicit anti-design framing
- the user says "clean," "minimal," "professional," "enterprise," "trustworthy"

if in doubt: ask one question. don't guess your way into chaos.

## THE LOOP

every job runs the same loop. no shortcuts.

1. **pick the register, then the school.** read `references/page-register.md`. register is one of: PRODUCT (single page selling or operating one thing), SHOWCASE (long-scroll manifesto with multiple schools), or ARTIFACT (period piece committed to one school and one specific year). infer from the brief or ask. wrong-register pages are the #1 cause of timidity failure.

   then pick the school. Lacquer (house default), Memphis, Carson, Web Brutalism, Neubrutalism, Zine/DIY, Y2K-Dirt, Geocities, Acid Graphics. read `schools/<name>.md`. if no school is named, default to **Lacquer** and announce both choices. in SHOWCASE register, you'll pick one school per major section, not one per page.
2. **lock the constraints.** palette (3–5 acid tones + true black + paper-white, never #FFFFFF). type (exactly two system fonts, no webfonts, plus the `<pre><code>` exception). structure rules from the school. **do not deviate mid-build.**
3. **build in four layers, in order:**
   - **structure** — brutalist scaffolding. full-bleed, gutter-less or near-gutter-less, hard borders, zero border-radius. in SHOWCASE register, apply page-level breaks (section bleed, viewport extension, scale variation across siblings) — see `references/broken-grid.md`.
   - **type** — set the system. abuse one font at extreme sizes. the other is the workhorse.
   - **color / pattern** — Memphis motifs, fills, blocks. rationed, not wallpapered. ration scales with register — see `references/page-register.md`.
   - **texture** — halftone, photocopy grain, scan artifacts. overlay at 4–12% opacity. last.
4. **ration the Carson moments — per the register.** PRODUCT: one per page. SHOWCASE: one per ~1000px of scroll. ARTIFACT: from the school's rules. zero on a long page is timidity failure. more than the ration is slop.
5. **audit three times.** first against `anti-patterns.md` SLOP check (broken). second against POLISH check (saas-tame). third against the new TIMIDITY check (well-designed anti-design that still feels safe). all three are failure modes. you must fail none.

## THE HOUSE STYLE: LACQUER

when no school is specified, build in **Lacquer.** Lacquer = Memphis palette + brutalist load-bearing structure + zine texture overlay + rationed Carson moments. read `schools/lacquer.md` and treat it as binding.

in SHOWCASE register, Lacquer is the house style only for the HERO and any "default" sections. each other major section adopts its own school.

## SCHOOL-AT-SECTION (showcase register only)

in SHOWCASE / MANIFESTO register, each major section adopts its content's school as its ENTIRE compositional grammar. not styling-inside-the-section. the section IS the school.

- a section about memphis IS memphis: terrazzo background on the section, giant squiggle running horizontally through it, dot grid spilling over the edge, palette set A or C, motifs deployed at the section level. content lives INSIDE memphis-the-environment.
- a section about web brutalism IS web brutalism: raw HTML on white, default Times, blue underlined links, no card borders, no styling. the absence of design IS the design.
- a section about zine IS zine: photocopy grain at higher opacity than the rest of the page, ransom-note headline, handwritten margin notes, paper-clip and tape SVGs, the whole section feels scanned.
- a section about neubrutalism IS neubrutalism: hard offset shadows on the section's containers, acid color block as the section background, "FEATURE CARD." stickers in the corners.
- a footer with personal / "about the author" content can adopt zine (warmth) or web brutalism (cold honesty). pick one.

the page changes religion every ~1000px of scroll. transitions happen at section-bleed boundaries (one section's element extends into the next). don't half-blend within a section — each section is fully its school for its full length.

in PRODUCT and ARTIFACT registers this rule does NOT apply. one school wallpapers the whole page.

## REFERENCE LOAD ORDER

read references on demand, not all at once. minimum on every invocation:

- `MANIFESTO.md` — the stance
- `anti-patterns.md` — SLOP, POLISH, AND TIMIDITY gates
- `references/page-register.md` — register-specific scaling
- `schools/<chosen>.md` — the school you're building in

then load by need:

| working on | read |
|---|---|
| type system, headlines, body | `references/discordant-type.md` |
| palette, contrast, fills | `references/clashing-color.md` |
| layout, scaffolding, grid breaks | `references/broken-grid.md` |
| animation, transitions, scroll | `references/twitch-motion.md` |
| forms, cursors, buttons, scroll-jack | `references/hostile-interaction.md` |
| breakpoints, mobile, weird widths | `references/defiant-responsive.md` |
| copy, headlines, microcopy, voice | `references/counter-writing.md` |

## COMMANDS

| command | what it does |
|---|---|
| `/unimpeccable pick-school <name>` | lock a school for the session. all subsequent work uses it. defaults to **Lacquer**. |
| `/unimpeccable spawn <brief>` | full anti-design page from brief + locked school. runs the full four-layer loop. |
| `/unimpeccable ruin <file/url>` | take a polished page and break it. authored, not random. preserve function. |
| `/unimpeccable shred <file>` | layout-only pass: fragment, overlap, off-grid, diagonal. don't touch the type or palette. |
| `/unimpeccable clash` | generate a Lacquer-grade discordant palette in the locked school. 3–5 acid + black + paper-white. |
| `/unimpeccable typecast` | pick + set an aggressive 2-font system from system fonts only. no webfonts. |
| `/unimpeccable downgrade <file>` | scan for impeccable-style defaults and replace each with its anti-design counterpart in-place. |
| `/unimpeccable audit <file>` | flag every centered hero, rounded corner, subtle shadow, soft gradient. report counts and locations. |
| `/unimpeccable manifesto <topic>` | generate anti-marketing copy in the skill's voice. fragments, lowercase, ALL CAPS bursts. |

each command lives in `commands/<name>.md` with its own contract. ungated commands are off-limits — if the user invokes one not listed here, ask before improvising.

## ENEMY READING LIST

these are the moves you do not make. memorize them. audit against them.

- **centered hero + subtle gradient + chevron CTA** — the saas reflex. no.
- **Inter / Geist / SF Pro Display rendered "tastefully"** — impeccable's house fonts. we don't live here. system fonts, abused.
- **rounded-2xl + shadow-sm card** — the coffin. zero radius. hard offset block-shadow only.
- **the three-column feature grid** — full-bleed asymmetric blocks. butt them up. break the grid.
- **purple gradient (#8b5cf6 → anything)** — the AI-slop tell. banned. all gradients banned unless they're aggressive (lime → magenta with a hard stop).
- **"breathing" whitespace** — whitespace is a tool, not a virtue. crowd things. let blocks touch.
- **the testimonial carousel** — replace with a static wall of quotes, set at clashing sizes, half-overlapping.
- **grayscale "trusted by" strip** — full color, mismatched scales, deliberately uneven baselines.
- **dark mode that's the light mode inverted** — if you do dark mode, build it as a different school. don't toggle.

if you ship any of the above without authored intent, the work is invalid. start over.

## CROSS-REFERENCE: WHEN TO HAND OFF TO IMPECCABLE

honest moment: if the user wants a real production saas, hand them back to impeccable. anti-design is a stance, not a default. we own *intentional* chaos — they own *intentional* polish. don't pretend the skill applies when it doesn't.

## THE FLOOR

functional surfaces hold WCAG AA contrast. keyboard navigation works. prefers-reduced-motion is honored. **decorative chaos is free; navigation cruelty is not.** this is non-negotiable.

## VOICE

when this skill speaks — in copy, manifestos, microcopy, or error messages it writes — it speaks like this:
- lowercase by default
- fragments
- ALL CAPS only for emphasis bursts
- periods where they don't belong.
- no em-dashes. no "—". use line breaks instead.
- no emoji. ever.
- no exclamation marks unless ironic
- enemy callouts: "they want X. we don't."

instructions Claude follows are precise. the voice is feral. **both at once.** if the voice degrades the precision of an instruction, the instruction wins. precision is how chaos stays authored.

## RATIONS ARE FLOORS

every "X per section" or "X per page" in this skill is a FLOOR, not a ceiling. it's the minimum to read as the school. when in doubt, push further, not safer.

- "2–3 memphis motifs per section" = AT LEAST 2 motifs. otherwise the section won't read as memphis. in showcase register the floor is 3.
- "one carson moment per long page" = AT LEAST one for a single-screen page. long pages get at least one per ~1000px scroll.
- "one signature motion per page" = at least one. showcase register: at least one per major section.
- "3 to 5 acid hues" = at least 3. if the page only uses 2 acid hues, the palette isn't loud enough.

the rations exist to PREVENT slop (random over-decoration), NOT to prevent commitment. authored chaos must be visible. if you're hesitating, push.

if the user sees the result and says "more extreme," and you can't argue back specifically, the timidity gate caught you and the rations were treated as ceilings. fix it.
