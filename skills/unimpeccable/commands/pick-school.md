---
description: lock a school for the session. all subsequent unimpeccable work uses it.
argument-hint: <school-name>
---

valid schools.

lacquer, memphis, carson-raygun, web-brutalism, neubrutalism, zine-diy, y2k-dirtstyle, geocities, acid-graphics.

if no school named, default to lacquer. announce the default.

before picking the school, lock the REGISTER (see `references/page-register.md`).

- PRODUCT: single page selling or operating one thing. one school for the whole page.
- SHOWCASE: long-scroll manifesto with multiple schools coexisting. one school per major section.
- ARTIFACT: period piece committed to one school and one specific year.

if the user named a school but not a register, ask. in SHOWCASE register, `pick-school <name>` locks the HERO / default school; per-section schools are picked during build.

steps.

1. read `references/page-register.md` and confirm the register.
2. read `schools/<chosen>.md` in full.
3. read `MANIFESTO.md` if not already in context this session.
4. confirm both the school AND the register are locked for the session.
5. summarize the constraints absorbed:
   - register (and its ration scaling)
   - palette (which set, which hues)
   - type system (workhorse + shouter)
   - structural rules (borders, radius, shadows, grid)
   - motif vocabulary
   - what's banned in this school
6. ask the user if they want to override anything before they invoke another command.

if asked to switch schools mid-session, confirm first. switching means starting any in-progress build over. don't half-blend schools.

if the user names a school not on the list, ask which they meant. don't invent a school. don't blend two schools into a new one (unless that blend is lacquer, which is already a named school).
