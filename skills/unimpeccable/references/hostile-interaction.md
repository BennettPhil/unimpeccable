# hostile-interaction

interactions in unimpeccable are **abrupt, not cruel.** the page argues. it doesn't entrap.

the difference:
- argues = a button labeled `NO.` that toggles dark mode
- entraps = a "close" button that opens an upsell modal

we do the first. we do not do the second. ever.

## BUTTONS

buttons are rectangles. solid border. zero radius. hard offset shadow. ALL CAPS label in the shouter font.

```css
.btn {
  background: var(--acid-1);
  color: #000;
  border: 3px solid #000;
  border-radius: 0;
  padding: 12px 24px;
  font-family: "Arial Black", Impact, sans-serif;
  text-transform: uppercase;
  letter-spacing: 0.04em;
  box-shadow: 6px 6px 0 0 #000;
  transition: none;
  cursor: pointer;
}
.btn:hover {
  background: #000;
  color: var(--acid-1);
  /* no transform, no shadow change. snap. */
}
.btn:active {
  box-shadow: 0 0 0 0 #000;
  transform: translate(6px, 6px);
}
```

label rules:
- one word ideal. two words max.
- imperatives or refusals: `START`, `READ`, `STOP`, `NO`, `BURN`, `OPEN`, `KILL`
- never `Get Started`, `Learn More`, `Discover`, `Explore`, `Sign up free`
- no chevron. no arrow. no icon.

## LINKS

links underlined, palette color, NOT browser blue (unless the school is web brutalism — then yes, exactly `#0000EE` and `#551A8B` for visited).

```css
a { color: var(--acid-2); text-decoration: underline; text-decoration-thickness: 3px; text-underline-offset: 4px; }
a:hover { background: var(--acid-2); color: #000; text-decoration: none; }
```

no fade. no color slide. snap.

## FOCUS RINGS

VISIBLE. UGLY. UNAPOLOGETIC.

```css
:focus-visible {
  outline: 4px solid var(--acid-magenta);
  outline-offset: 2px;
}
```

never `outline: none` without a louder replacement. focus must be the most visible state on the page. keyboard users get the loudest treatment.

## FORMS

functional surfaces hold AA. forms are functional.

- labels ABOVE the input, not floating, not placeholder-as-label
- labels in lowercase, workhorse font, 16px minimum
- inputs: `border: 3px solid #000`, paper-white background, `border-radius: 0`, padding `12px 16px`
- focus state: `border-color: var(--acid-magenta)`, no transition
- error state: red border (`#FF2E93` or `#FF4438`), error message in workhorse font below, ALWAYS readable
- error messages are direct. `wrong.` or `not an email.` or `try again.` — not "Oops! Something went wrong."
- never use color alone to indicate state. errors also get an icon or a bold label prefix.
- never disable submit buttons until form is "valid" — let them try, fail, learn

## ERRORS

- direct
- lowercase
- functional (tell the user what's wrong)
- never apologetic
- never cute

GOOD:
> wrong password.
> we need a real email.
> file too big. 10MB max.

BAD:
> Oops! Something went wrong 😅
> We couldn't find that. Please try again!
> Hmm, that doesn't look quite right...

## CURSORS

default cursor everywhere. exceptions, narrowly:
- `cursor: pointer` on actual clickable things (the browser does this for buttons automatically)
- `cursor: crosshair` on ONE decorative interactive zone per page, max
- never `cursor: none`
- never custom cursor images
- never replace the cursor with a Memphis squiggle

## HOVER STATES

snap. always snap. never fade.

- background color inverts to palette opposite
- text color inverts
- border stays
- shadow may collapse to zero (button press feel)
- NO `transform: translateY(-2px)` lift
- NO `scale(1.05)` grow
- NO opacity change

## SCROLL-JACK

banned. never override scroll behavior. never `prevent default` on wheel events. never scroll-snap a whole page.

allowed:
- `scroll-snap-type: x mandatory` on ONE horizontal marquee section
- nothing else

## MODALS

avoid. modals are impeccable's reflex.

if you absolutely need one:
- ESC closes it
- click-outside closes it
- focus traps inside while open
- never auto-open on page load
- never auto-open on scroll position
- never auto-open ever

cookie banners and similar are the saas reflex's saas reflex. if the user really needs a banner, make it a static block at the top of the page that doesn't dismiss. honesty.

## TOOLTIPS

prefer not. if a UI element needs a tooltip to be understood, the label is wrong.

if you must:
- show on focus AND hover
- never on click-and-hold
- accessible with `aria-describedby`
- timeout: `0ms` show, `0ms` hide. snap.

## DRAG / DROP

case-by-case. drag must have keyboard equivalents. never make drag the ONLY way to do something.

## TIMING POLICY

interactions snap. animations snap. menus open and close instantly. there is no "delightful pause." pauses are impeccable's reflex.

## THE SELF-CHECK

- can the entire page be operated with a keyboard?
- are all focus rings visible and louder than hover states?
- do form errors hold AA contrast and not rely on color alone?
- is there zero scroll-jack?
- zero auto-opening modals?
- do all hover states SNAP (no fade, no transform)?
- are buttons labeled with one-word imperatives or refusals, no chevrons?
