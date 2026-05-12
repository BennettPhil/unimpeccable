# unimpeccable.

the hostile fork of [impeccable](https://github.com/pbakaus/impeccable) and the [frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design) skill.

an agent skill for claude code. anti-design as a discipline. authored chaos rooted in a real movement.

---

## what it is

impeccable wants your interface to be impeccable. we don't.

unimpeccable is a skill that makes claude produce intentionally anti-design interfaces in the lineage of:

- memphis group (sottsass, milano, 1981)
- david carson / ray gun (1990s)
- web brutalism (2010s)
- neubrutalism (2020s)
- zine / diy (riot grrrl, punk, photocopy culture)
- y2k / dirtstyle (1998 to 2003)
- geocities / sincere old web (1995 to 2002)
- acid graphics (2018 to present)

plus **lacquer**, a house style that fuses memphis palette + brutalist structure + rationed carson moments + zine texture.

chaos must be authored. every break points at a named school. random is not radical.

## the floor

functional surfaces hold WCAG AA contrast. keyboard navigation works. `prefers-reduced-motion` is honored.

decorative chaos is free. navigation cruelty is not.

## install

one line. via [skills.sh](https://skills.sh/).

```bash
npx skills add BennettPhil/unimpeccable
```

this installs the skill into your agent of choice (claude code, cursor, codex, windsurf, gemini, copilot, etc.).

then invoke.

```
/unimpeccable:spawn "a landing page for my band that argues with itself"
```

or lock a school first.

```
/unimpeccable:pick-school memphis
/unimpeccable:spawn "a poster site for a basement noise show"
```

### manual install (if you want symlinks for live edits)

```bash
git clone git@github.com:BennettPhil/unimpeccable.git
ln -s "$PWD/unimpeccable/skills/unimpeccable" ~/.claude/skills/unimpeccable
ln -s "$PWD/unimpeccable/skills/unimpeccable/commands" ~/.claude/commands/unimpeccable
```

## commands

| command | what it does |
|---|---|
| `pick-school` | lock the school for the session |
| `spawn` | build a full anti-design page from a brief |
| `ruin` | take a polished source and break it. preserve function. |
| `shred` | layout-only fragmentation. four authorized grid breaks. |
| `clash` | generate a discordant palette |
| `typecast` | pick the 2-font system from system fonts only |
| `downgrade` | replace impeccable defaults with anti-design counterparts in place |
| `audit` | scan for polish tells and slop tells. do not modify. |
| `manifesto` | generate anti-marketing copy in the skill's voice |

## what's in the box

```
skills/unimpeccable/
  SKILL.md                  the entry point. read first.
  MANIFESTO.md              the stance. five laws. the enemy.
  anti-patterns.md          two-gate audit. SLOP check + POLISH check.
  references/
    clashing-color.md       palette rules, contrast carve-outs, gradient policy
    broken-grid.md          four authorized grid breaks, alignment policy
    discordant-type.md      two-font system, font ban list, carson moment options
    twitch-motion.md        easing policy, reduced-motion contract
    hostile-interaction.md  buttons, links, focus rings, form copy
    defiant-responsive.md   non-canonical breakpoints, mobile as its own beast
    counter-writing.md      voice rules, banned phrases, replacement table
  schools/
    lacquer.md              the house style
    memphis.md
    geocities.md
    acid-graphics.md
    carson-raygun.md
    web-brutalism.md
    neubrutalism.md
    zine-diy.md
    y2k-dirtstyle.md
  commands/
    pick-school.md
    spawn.md
    ruin.md
    shred.md
    clash.md
    typecast.md
    downgrade.md
    audit.md
    manifesto.md
site/
  index.html                the promo site. lacquer school. dogfood.
```

## what unimpeccable is NOT

- not "ugly on purpose." ugly is accidental. we are authored.
- not a fixer for broken layouts. structure is the fix. chaos is not.
- not for production saas without explicit anti-design framing. if the user says "clean, modern, professional," hand them to impeccable.
- not anti-user. functional surfaces hold AA. the floor is the floor.

## hostile-fork notice

unimpeccable defines itself in opposition to two existing projects:

- [pbakaus/impeccable](https://github.com/pbakaus/impeccable)
- [anthropics/skills — frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design)

both are good at what they do. what they do is not what we do. the antagonism is structural, not personal.

## license

MIT. see [LICENSE](./LICENSE).

take it. break it. ship it.
