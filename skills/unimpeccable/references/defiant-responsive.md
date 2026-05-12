# defiant-responsive

mobile-first is a polite fiction the framework taught everyone. we don't follow it.

unimpeccable layouts are designed for a specific viewport and **don't apologize at others.** they break visually. they stay functional. that's the contract.

## THE TWO LAWS

1. **functional surfaces work at every viewport.** navigation, forms, errors, primary content — all reachable, all readable, at every screen size.
2. **decorative surfaces are allowed to break.** a Memphis motif that overlaps a headline at 1440px can clip awkwardly at 360px. let it. it's decoration.

## BREAKPOINTS

forget `640 / 768 / 1024 / 1280`. those are Tailwind's defaults, and the saas world's defaults. use non-canonical numbers.

suggested unimpeccable set:
- `492px` — phone landscape / small tablet portrait
- `712px` — tablet portrait
- `923px` — small laptop
- `1186px` — desktop
- `1487px` — wide desktop

pick three from the above per project. you don't need all five.

reasons:
- the canonical breakpoints make designs slot into existing mental models. anti-design rejects the slot.
- arbitrary breakpoints reveal the choice — they look intentional because they ARE intentional.
- they make screenshots look distinct from "another Tailwind site."

## MOBILE IS ITS OWN BEAST

mobile is not "narrowed desktop." it's a different layout altogether.

at narrow viewports (< 712px):
- the hero shouter shrinks but stays brutal — `clamp(72px, 22vw, 140px)`
- multi-column splits become full-width stacks
- Memphis motifs reduce to ONE per section (not 2–3)
- the texture overlay opacity drops to `4–6%` (more would crush a small screen)
- the Carson moment may be SKIPPED on mobile entirely — illegibility on a small screen reads as a bug, not a statement

## FLUIDITY POLICY

unimpeccable uses fluid `clamp()` sparingly. fluidity makes everything average. discrete jumps make every breakpoint feel chosen.

allowed:
- `clamp()` on hero headlines (size scales smoothly with viewport — fine, hero anchors the page)
- `clamp()` on horizontal padding (so the layout doesn't suffocate)

banned:
- `clamp()` on body text (pick a fixed size and own it: 18px or 20px)
- `clamp()` on grid gaps (gaps are 0 or 4px, fixed)
- `clamp()` on border thickness (3px or 6px, fixed)
- `clamp()` on shadow offset (8px hard offset, fixed)

## VISUAL BREAKAGE: WHAT'S ALLOWED

at viewports the layout wasn't designed for:
- a decorative element clips the edge — fine
- a Memphis motif overlaps a heading awkwardly — fine
- a color block runs taller than its content — fine (it's a color block)
- two stacked sections share a hard color edge that "wasn't aligned" — fine
- a Carson-moment headline becomes single-line where it was two — fine

at viewports the layout wasn't designed for:
- form inputs overflow the viewport — NOT FINE. fix it.
- buttons get cut off or unreachable — NOT FINE. fix it.
- error messages clipped — NOT FINE. fix it.
- nav becomes unusable — NOT FINE. fix it.
- content unreadable (4px text, overlap with no contrast) — NOT FINE. fix it.

## TOUCH TARGETS

minimum `44px × 44px` for any tappable thing. non-negotiable. that's the WCAG floor and we hold it on functional surfaces.

decorative non-interactive elements can be any size.

## ORIENTATION

design for the default (portrait on phones, landscape on desktops). landscape phone is a corner case — the layout may break visually, must stay functional.

never use `orientation` media queries to swap the layout entirely. one layout per breakpoint, responsive to the viewport's width.

## CONTAINER QUERIES

use sparingly. they're useful for component-level responsive behavior in design-system contexts. anti-design rarely needs them — we don't reuse components across contexts because every page is its own thing.

## VIEWPORT META

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

never disable user scaling. never `maximum-scale=1`. accessibility floor.

## PRINT STYLES

if a user prints an unimpeccable page, give them black ink on paper. specifically:

```css
@media print {
  * { background: white !important; color: black !important; box-shadow: none !important; }
  /* Memphis motifs hide in print */
  .motif, .texture-overlay { display: none; }
}
```

the print version reads as zine. that's on-brand.

## THE SELF-CHECK

- does the layout work at three viewport widths I designed for?
- does it stay FUNCTIONAL at viewports I didn't design for?
- are touch targets ≥ 44px on tappable elements?
- did I avoid canonical Tailwind breakpoints?
- is `clamp()` rationed (hero + padding only)?
- does the page hold up if I rotate my phone?
