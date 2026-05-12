# twitch-motion

motion in impeccable's tradition is graceful. exponential easing. orchestrated reveals. tasteful staggers. we don't do that.

motion in unimpeccable is **a glitch with a purpose.** it snaps. it jitters. it cuts. it doesn't fade.

## THE FIRST LAW

`prefers-reduced-motion: reduce` is honored without exception. all motion below is wrapped:

```css
@media (prefers-reduced-motion: no-preference) {
  /* twitch lives here */
}
```

users who opt out get static. anti-design is not anti-user.

## EASING POLICY

allowed:
- `transition: none` (default for everything)
- `transition-timing-function: steps(1, end)` (snap)
- `transition-timing-function: steps(3, end)` (chunky stop-motion)
- `cubic-bezier(0.95, 0, 0.05, 1)` (near-instant overshoot — for a single signature moment)

banned:
- `ease`, `ease-in`, `ease-out`, `ease-in-out` (the saas defaults)
- any spring physics that "feels nice"
- exponential easing on layout
- bouncy easing on anything that isn't ironic

## DURATIONS

- hover state: `0ms` (instant snap)
- click feedback: `40–80ms` (quick chunk)
- page transition: `0ms` (no SPA-fade; full reload is fine, brutalist)
- signature moment (ONE per page): `150–250ms` with step-easing

if a designer reflex says "300ms ease-out" — that's impeccable. don't.

## ALLOWED MOTION PATTERNS

### snap-hover

button hover: instantly inverts colors. no fade. no transform. the cursor lands and the button changes. that's it.

```css
.button:hover { background: var(--acid-magenta); color: #000; }
.button { transition: none; }
```

### jitter-on-idle

a single decorative element jitters: micro-translate `±2px` on `x` and `y`, 8 keyframes, 0.5s loop. ONLY on Memphis motifs or a hero accent. never on functional UI. never on text.

### step-cycle

a marquee of headlines that cycles in `steps(1, end)` every 1200ms. no scroll. no fade. cut. cut. cut.

### scroll-trigger snap

ONE element per page reveals on scroll via `step(1, end)` — it's there, then it's there. no fade-in, no slide-up.

### snap-flinch hover

NOT a smooth lift. the element FLINCHES.

```css
.card {
  transition: none;
  box-shadow: 8px 8px 0 0 #000;
}
.card:hover {
  box-shadow: 24px 24px 0 0 #000;
  transform: translate(-3px, -3px);
}
```

shadow jumps OUT (16px more offset) and the element moves the opposite direction simultaneously. visual: the card got startled. use on cards, blocks, callouts. never on functional buttons (those stay snap-invert per `hostile-interaction.md`).

a card that lifts smoothly is impeccable. a card that flinches is unimpeccable.

### ambient tic

a single decorative element jitters ONCE every N seconds (8 to 30s). not a loop. a tic.

```css
@keyframes tic {
  0%, 95% { transform: translate(0); }
  95.5% { transform: translate(2px, -1px); }
  96% { transform: translate(-3px, 2px); }
  96.5% { transform: translate(1px, 1px); }
  97%, 100% { transform: translate(0); }
}
.tic { animation: tic 12s infinite steps(1, end); }
```

dead static 95% of the cycle, jitter for ~360ms, dead static again. eye catches it once and isn't sure it happened. use on ONE element per page (hero word, primary logomark, a single headline). NEVER on multiple at once — the eye would clock the rhythm and it becomes decoration.

### scroll-triggered follower

a decorative element associated with a school sticks to the viewport edge until the next school's section invalidates it. the page is being haunted by whichever school you're currently inside.

```css
.section--memphis { position: relative; }
.section--memphis .follower {
  position: sticky;
  top: 24px;
  right: 24px;
}
```

the follower sits at `position: sticky` inside its parent section. when the user scrolls into the next section, the parent scrolls off and the follower disappears.

works for: memphis squiggle, y2k HUD bracket, zine paper-clip, neubrutalism sticker corner, radical-italian grid line. one follower per major section, showcase register only.

### the signature moment

one transition per page (or per major section in showcase register) may have actual choreography. examples:
- a heading slams in from off-screen (`translateX(-100%) → 0` in 150ms with overshoot)
- a color block cascades across the viewport in chunky steps
- type cycles through 3 wrong fonts and lands on the right one

ONE per page. more = noise.

## BANNED MOTION PATTERNS

- `fade-in-on-scroll` (the IntersectionObserver saas reflex)
- parallax of any kind (Y-translate scaled to scroll position = banned)
- smooth-scroll behavior (`scroll-behavior: smooth` removed)
- counter animations ("0 → 1,247,892 customers!") — banned, embarrassing
- staggered list reveals (each `<li>` fading in 50ms apart) — the AI-slop tell
- gradient angle animation (the rainbow conic spin) — banned
- particle backgrounds, floating dots, "constellation" networks — all banned forever
- typewriter text effects — exception: zine school may use them, sparingly
- shimmer skeleton loaders — solid color block, no animation

## LAYOUT-SHIFT POLICY

unimpeccable tolerates layout shift in ways impeccable doesn't. specifically:

- font-display: `swap` (the FOUT is fine; FOIT is impeccable's reflex)
- images without explicit dimensions are acceptable IF the layout absorbs the shift visually (it crashes into a color block, doesn't push content down past the fold)
- never: layout shift that moves a button the user was about to click. functional cruelty is banned.

## CURSORS

default cursor everywhere. one exception: a single section may use `cursor: crosshair` or `cursor: pointer` on a non-button element as a Carson-equivalent moment. never `cursor: none` on the whole page (hostile, useless).

## SCROLL BEHAVIOR

- `scroll-behavior: auto` (browser default). NEVER `smooth`.
- no scroll-jacking. if you find yourself reaching for a library to "control the scroll experience," you're building the wrong school.
- horizontal scroll IS allowed for a single section (a marquee, a wall of cards). never page-wide.

## THE SELF-CHECK

- is `prefers-reduced-motion` honored?
- are all `transition`s either `none` or step-eased?
- is there exactly ONE signature motion moment?
- did I avoid every saas reflex (fade-in-on-scroll, parallax, smooth-scroll, counters, particles)?
- can a keyboard user reach every interactive element without motion getting in the way?
