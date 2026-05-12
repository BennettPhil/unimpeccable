# Geocities / Sincere Old Web

1995 to 2002. personal homepages, fan sites, band pages, hobby shrines. made by hand, on a platform that didn't have design conventions yet, by people who had never heard the word "designer."

this is anti-design by **innocence**, not refusal. web brutalism KNOWS what design is and rejects it. geocities never met design in the first place. that's the whole point. the page is built, not designed. it carries the marks of being typed into Notepad by an enthusiast.

## VISUAL MARKERS

- tiled patterned background images (starfield, marble, plaid, gradient bars, dithered noise)
- animated GIFs: under-construction signs, mailboxes, hourglasses, dancing babies, "new!" stars, dividers, hit counter widgets
- `<frame>` and `<frameset>` layouts (top nav frame + main content frame)
- `<table border="3" cellpadding="0" cellspacing="0">` for layout
- `<center>` tag wrapping everything
- web-safe colors (the 216-color palette, all values from `00 33 66 99 CC FF`)
- comic sans for personal headlines (allowed only in this school)
- mixed system fonts mid-paragraph
- blue underlined links (`#0000EE`), purple visited (`#551A8B`)
- "best viewed in Netscape 4 at 800x600" badges
- `<marquee>` and `<blink>` tags (use CSS equivalents to honor accessibility)
- horizontal rule GIFs (rainbow, gradient, animated)
- "you are visitor #00042" hit counter at the bottom
- "© 1997 by [name]" footers
- guestbook links, webring nav, "sign my guestbook"
- email addresses written as "me [at] domain [dot] com" to dodge spammers
- midi music references (we won't autoplay audio — but the page can show a `[NOW PLAYING: a-ha - Take On Me.mid]` badge as decoration)

## PALETTE

web-safe colors only. the 216-color palette. all six values are exactly `#00`, `#33`, `#66`, `#99`, `#CC`, `#FF` per channel.

deployment is amateur, not chosen. mix:
- pure primaries: `#FF0000`, `#00FF00`, `#0000FF`, `#FFFF00`, `#FF00FF`, `#00FFFF`
- background is usually a tiled image (starfield, marble, plaid, gradient bar) OR `bgcolor="#FFFFFF"` OR `bgcolor="#000000"` with bright text
- no concept of contrast accessibility — this school predates WCAG. **BUT** the unimpeccable floor still holds: body text passes AA on actual readable backgrounds. tiled-image-behind-text is fine if the text has a solid background block.

zero regard for harmony. if it looks like it was chosen, it's wrong. if it looks like the page author thought "i like this color, and i like that one too," it's right.

## TYPE

free for all. multiple fonts on a page is THE NORM.

allowed:
- `Times New Roman, serif` — default browser body
- `Verdana, Arial, sans-serif` — when the author "wanted it cleaner"
- `"Comic Sans MS", cursive` — for personal headlines, "about me" sections, captions
- `Courier, monospace` — for `<code>`, "computer stuff", ASCII art
- WORDart-style decorative type — implemented via `<img>` of period type (or, since we don't have those images, via aggressive CSS text-shadow stacks for fake 3D)

rules.

- font CAN change mid-paragraph. that's authentic.
- `<font size="7">` (or its CSS equivalent `font-size: 36px`) for emphasis. mid-paragraph size changes too.
- `<b>` `<i>` `<u>` used liberally and often combined.
- ALL CAPS for excitement. lowercase for the rest.
- no concept of "type system." each font choice is local.

this school is the ONLY place comic sans is permitted in unimpeccable.

## STRUCTURE

table-based layout. period. `<table border="3" cellpadding="8" cellspacing="0">` is the unit. cells contain text, images, more tables.

- `<center>` for centering — yes the actual tag, or CSS `text-align: center` if you must
- `<frameset>` layouts allowed for the canonical geocities experience (a top frame for nav, a main frame for content). use `<iframe>` if you can't use `<frame>` semantically.
- `<body background="path/to/tile.gif">` for tiled patterned backgrounds. use CSS `background-image: url(...); background-repeat: repeat;`
- horizontal rules everywhere: `<hr>` styled as rainbow gradient, or replaced with an `<img>` of a rainbow divider
- pages stack content vertically with no constraint on width

**banned**: `position: absolute`, `display: flex`, `display: grid`. this school predates them. if you reach for them, you're not in geocities anymore.

## DECORATION RATIONS

generous, but authored:
- 3 to 5 animated GIFs per significant section. more is slop, fewer is "modernized geocities" which is impeccable wearing the costume.
- tiled background: ONE image, repeating, behind everything.
- horizontal rule decorations: between every section. that's the rhythm.
- "new!" stars next to recently updated content. 1 to 3 per page.
- under-construction badge: exactly one per page, at the bottom, near the email-address-with-bracketed-at-sign.

## VOICE

shifts in this school. lowercase rules from `counter-writing.md` are relaxed.

- title case is OK ("Welcome To My Homepage")
- exclamation marks are FINE — they're authentic to the era
- emoji are still banned (the era used emoticons and ASCII faces instead: `:)` `:-D` `>:-(` `<3`)
- "this site updated [DATE]" badges
- "i made this site myself!" disclaimers
- first-person sincerity ("my name is X and i love Y")
- enthusiastic links ("check out my friend's site, it's the BEST!")

avoid:
- ironic 90s nostalgia voice (that's a costume, not the school)
- product-marketing copy of any kind
- "i'm just a humble webmaster" self-deprecation that reads as ironic

the voice is **sincere**. the era's amateurs meant it. so do we.

## ANIMATED GIF VOCABULARY

inline SVG can fake the spirit, but the originals are pixelated 16-32 color GIFs. when generating, the visual should:
- be pixelated (`image-rendering: pixelated`)
- loop on a short cycle (1 to 4 seconds)
- have 4 to 8 frames maximum
- be obviously low-resolution (32x32, 48x48, 64x64)

vocabulary (each one is its own visual element):
- "Under Construction" — yellow/black hazard stripes, a stick figure with a hard hat
- mailbox with a letter popping in
- spinning at-sign or envelope
- "New!" star burst
- dancing baby
- hourglass with sand running through
- "You are visitor # X" with a flip-counter display
- spinning globe (network earth)
- text-marquee scrolling left

## NAMED REFERENCES

- **Cameron's World** (cameronsworld.net) — the canonical archive of preserved Geocities pages, now itself an art project
- **neocities.org** — the current revival, active community of people building hand-coded personal homepages
- **Olia Lialina, "A Vernacular Web"** (2005) — the foundational essay on amateur internet aesthetics
- **archive.org Geocities collection** — actual preserved pages, sortable by neighborhood
- **Space Jam (1996) website, archived** — corporate page that accidentally became geocities-canonical
- **early Yahoo!, AOL homepage scenes**
- **tilde.club, ctrl-c.club** — current "old web" communities
- **dirt.fyi** — current site that channels the vernacular

## WHEN TO REACH FOR THIS SCHOOL

- personal homepages, "about me" pages, online identities
- band / artist / musician sites
- fan sites, shrine pages, obsession sites
- hobby and collection archives
- school / class project pages where personality is the point
- "weird internet" projects
- archives presenting old content (the archive matches its subject)
- anywhere "i made this myself" is the desired feeling

## WHEN NOT TO

- corporate sites (this school looks "untrustworthy" to mainstream eyes — that's a feature for personal sites, a bug for businesses)
- e-commerce (buy buttons read as scams in this aesthetic)
- saas product pages
- production dashboards or app UIs
- anywhere user trust is load-bearing and the audience won't read "geocities" as "authentic personal voice"

## SELF-CHECK

- is the layout `<table>` based, not flexbox or grid?
- is there a tiled patterned background image?
- are there 3 to 5 animated GIFs visible?
- are links blue underlined, visited purple?
- did I use at least two different fonts (one of which may be comic sans)?
- is there a hit counter, "last updated" date, AND an under-construction badge?
- could this be mistaken for a real 1998 page if you squinted?
- did I resist the urge to make it look "designed"? if it looks designed, you failed.
