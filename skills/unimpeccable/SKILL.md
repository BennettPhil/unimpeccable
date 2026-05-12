---
name: unimpeccable
description: Generate intentionally anti-design web interfaces in the lineage of Memphis Group, Italian Radical Design, Carson/Ray Gun, web brutalism, neubrutalism, zine/DIY, and Y2K-dirt. Use when the user asks for anti-design, ugly-on-purpose, anarchic, irreverent, brutalist, anti-corporate, hostile, maximalist, or "unimpeccable" UIs. Chaos must be authored — every break points at a named school. NOT a fixer for accidentally-bad layouts; NOT a tool for production SaaS without explicit anti-design intent.
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

1. **pick a school.** Lacquer (house default), Memphis, Radical Italian, Carson, Web Brutalism, Neubrutalism, Zine/DIY, Y2K-Dirt. read `schools/<name>.md`. if no school is named by the user, default to **Lacquer** and say so.
2. **lock the constraints.** palette (3–5 acid tones + true black + paper-white, never #FFFFFF). type (exactly two system fonts, no webfonts). structure rules from the school. **do not deviate mid-build.**
3. **build in four layers, in order:**
   - **structure** — brutalist scaffolding. full-bleed, gutter-less or near-gutter-less, hard borders, zero border-radius.
   - **type** — set the system. abuse one font at extreme sizes. the other is the workhorse.
   - **color / pattern** — Memphis motifs, fills, blocks. rationed, not wallpapered.
   - **texture** — halftone, photocopy grain, scan artifacts. overlay at 4–12% opacity. last.
4. **ration the Carson moments.** ONE illegible / overlapping / broken-type moment per long page. more = meaningless.
5. **audit twice.** first against `anti-patterns.md` (slop check). then against the ENEMY READING LIST below (polish check). both are failure modes. you must fail neither.

## THE HOUSE STYLE: LACQUER

when no school is specified, build in **Lacquer.** Lacquer = Memphis palette + brutalist load-bearing structure + zine texture overlay + rationed Carson moments. read `schools/lacquer.md` and treat it as binding.

## REFERENCE LOAD ORDER

read references on demand, not all at once. minimum on every invocation:

- `MANIFESTO.md` — the stance
- `anti-patterns.md` — the slop floor AND the polish ceiling
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
