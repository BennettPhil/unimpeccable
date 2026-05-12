# Web Brutalism

emerged on the web around 2014–2016. brutalistwebsites.com curated the canon. the movement: **raw HTML against the corporate web.** default browser styles. system fonts. unstyled links. no images, or photographic images with no treatment.

this is the school of refusal. you are not designing. you are NOT designing.

the irony: this is harder than it looks. true web brutalism is not "ugly on purpose." it's "what the browser does when you stop fighting it." that takes restraint.

## VISUAL MARKERS

- default Times New Roman serif everywhere
- default browser blue underlined links (`#0000EE`), visited purple (`#551A8B`)
- no `<style>` block, or minimal CSS
- single-column flow, browser default reset
- ONE photograph per page, untreated
- date and timestamps visible
- file sizes visible
- author name as plain text
- the page feels like 1995 reading the new york times website

## PALETTE

```
background: #FFFFFF;  /* yes, pure white. this is the one school where #FFF is correct. */
text:       #000000;
link:       #0000EE;
visited:    #551A8B;
```

that's it. no fifth color. accent allowed: ONE rectangular block of color (riso red, riso yellow, cobalt) somewhere on the page, used as a structural break, not decoration.

## TYPE

```css
body {
  font-family: "Times New Roman", Times, serif;
  font-size: 18px;
  line-height: 1.4;
  color: #000;
  background: #FFF;
  max-width: 720px;
  margin: 2rem;
  padding: 0;
}
h1 { font-size: 32px; font-weight: bold; margin: 1em 0 0.5em; }
h2 { font-size: 24px; font-weight: bold; margin: 1em 0 0.5em; }
a { color: #0000EE; text-decoration: underline; }
a:visited { color: #551A8B; }
```

that's the entire stylesheet for a pure-brutalist page. no further treatment.

## RULES SPECIFIC TO THIS SCHOOL

- no webfonts
- no `border-radius`
- no shadows of any kind
- no transitions
- no animations
- no gradients (not even hard-stop)
- no SVG motifs
- no Memphis decoration
- minimal images — one per page max, photographic, unedited
- file structure visible: `2026-05-12-post.html`, dates in URLs
- "view source" should be readable and uncommented

## STRUCTURE

- one column, left-aligned (browser default)
- `max-width: 720px` or unconstrained
- margin top/left only (the browser's default body margin)
- headings stand out by size only (default `<h1>` styling)
- lists use default bullets (`disc`)
- tables get NO styling — they look like 1996 spreadsheets

## INTERACTIONS

- buttons look like browser default `<button>` elements (gray, beveled — yes, the OS chrome look)
- forms look like browser default form controls
- no JavaScript except where strictly required for functionality
- forms `POST` to a real endpoint, no client-side validation theater

## WHEN TO REACH FOR THIS SCHOOL

- archives, indexes, blog post listings
- documentation that wants to feel like a manual
- "about" pages for projects that take themselves seriously
- portfolios where the work itself is loud (the page recedes)
- developer-facing tools (code editors, CLIs documented as HTML)

## WHEN NOT TO

- consumer products (users expect at least some design)
- e-commerce
- marketing landing pages for commercial software
- anywhere user trust matters and "looks broken" reads as "is broken"

## THE TENSION WITH LACQUER

Lacquer uses brutalism as its structural skeleton. web brutalism is a different school: it doesn't add Memphis on top. Lacquer is "brutalism dressed in Memphis." pure web brutalism is "brutalism naked."

don't confuse them. picking web-brutalism means removing the Memphis layer entirely.

## NAMED REFERENCES

- **brutalistwebsites.com** — the canonical archive (curated by Pascal Deville, started 2014)
- **the early-internet aesthetic** — geocities (without the under-construction GIFs), late-90s personal homepages, university faculty pages
- **Bloomberg.com, terminal-era** — when finance sites looked like Bloomberg terminals
- **craigslist.org** — the longest-running pure-brutalist site that actually has product-market fit

## SELF-CHECK

- is the stylesheet under 30 lines?
- are all links the default `#0000EE` underlined?
- is the font Times New Roman?
- is there zero animation, zero transition, zero shadow?
- could this be 1995 with new content?
- if I add Memphis decoration, this becomes Lacquer — am I sure I want pure brutalism?
