# clashing-color

color is not a vibe. color is a fight.

impeccable picks "restrained / committed / drenched." we pick **enemies.** every page is a brawl between three hues that should not be in a room together.

## THE FIVE LAWS OF CLASH

1. **no analogous schemes.** if two hues sit next to each other on the wheel, drop one.
2. **no monochrome.** monochrome is impeccable's panic button. we don't reach for it.
3. **no pastels.** pastels apologize. we don't.
4. **no #FFFFFF.** ever. use paper-white `#F4F0E6` or a tinted neutral. pure white is the saas default.
5. **no gray.** if you reach for `#666` for body text, you're building impeccable's site. body text is black on paper-white or paper-white on a color block. that's it.

## THE PALETTE RULE

3 to 5 acid hues + true black + a tinted neutral. no exceptions.

acid hues are saturated (HSL saturation ≥ 80%) and high in chroma. examples:

- lime `#C8FF00`
- magenta `#FF2E93`
- cyan `#00C2FF`
- safety orange `#FF6A00`
- riso red `#FF4438`
- riso yellow `#FFE800`
- electric blue `#1F51FF`
- brat green `#8ACE00`

## CLASH PAIRS (use one per page as the dominant fight)

- lime × magenta — the loudest. classic Memphis.
- cyan × orange — opposed on the wheel. industrial-poster energy.
- riso red × riso blue — newsprint, riot grrrl.
- yellow × cobalt — sottsass.
- brat green × bubblegum — current-era pop.

never use two clash pairs on the same page. one fight at a time. otherwise it's wallpaper.

## DEPLOYMENT

how to actually use the palette:

- **black** is structure: borders, baseline text, hard shadows.
- **paper-white** is the page.
- **one acid hue** is the section block backgrounds. used in 2–3 large rectangles.
- **the second acid hue** is the headline color and one button color. used sparingly.
- **the third acid hue** (if you have one) is a single accent — one icon, one motif, one underline. once.
- **the fourth and fifth** are emergency reserves. don't reach for them unless you've justified the first three.

## CONTRAST FLOOR

decorative text can be illegible. functional text cannot.

| element | floor |
|---|---|
| body copy | AA (4.5:1) against its actual background, not a "lightened" version |
| buttons / links | AA, and the hit target visible without a hover |
| form labels | AA |
| error / validation messages | AA AND not the same color as a button |
| decorative headline (Carson moment) | no floor — illegibility is allowed once per page |
| navigation | AA, no exceptions, no "ironic" disorientation |

verify with an actual contrast checker, not vibes.

## GRADIENT POLICY

default: **no gradients.** the saas industry has poisoned the gradient. it now reads as "AI generated landing page."

exceptions, narrowly drawn:
- **hard-stop gradients** (no smooth blend): lime → magenta with a sharp boundary at 50%. acceptable.
- **conic gradients** with 3+ acid hues, no smoothing. acceptable as a single background block, not full page.
- **never**: purple → pink, pink → orange, blue → cyan, or any combination that has appeared on a YC company's homepage since 2019.

## THE PURPLE BAN

`#8b5cf6` and its neighbors (indigo-violet 250–270° hue range) are **banned.** they are the single most over-used hue of the AI-slop era. they don't appear in any unimpeccable output. ever.

if a user requests purple, push back once. if they confirm, use only **electric violet `#9D00FF`** at full saturation, never as a gradient, never paired with another cool hue. and explain why we made them confirm.

## FILL TREATMENT

color blocks are not "subtle background tints." they are LOUD.

- solid fills, not 10%-opacity wash
- when overlaying a fill on another fill, use `mix-blend-mode: multiply` or `mix-blend-mode: difference` — never opacity
- never use a CSS `background-color` lighter than `#E0` per channel on a "background" element. backgrounds carry weight or they don't exist.

## SELF-CHECK

- is there ONE clash pair driving the page?
- is the third+ acid hue used like a spice, not a sauce?
- is there any gray on the page? if yes, replace or delete.
- is the page background a tinted neutral (or a color block), not `#FFF`?
- can a stranger name the dominant clash pair in 2 seconds? if not, the fight isn't loud enough.
