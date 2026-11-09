# afkbird.com homepage, scroll-craft build (November 2026)

**Brief status:** authored under explicit creative delegation. Robby asked for a
redesign of afkbird.com using scroll-craft and humanizer, then chose three
things directly (Nov 8, 2026). Everything not listed under "Decisions from
Robby" is an authored decision, labeled as such.

## Decisions from Robby (his answers)

- Skill: nateherkai/scroll-craft (not maraja/shipcraft).
- Scope: "Homepage showpiece". Layered hero and a scroll-driven project
  showcase on the homepage; other pages get the new look with calmer motion.
- Visuals: "Brand kit + existing art". No AI-generated imagery. The bird mark,
  the amber/slate palette, and the real in-game renders and app screenshots
  already in the repo.

## Standing rules carried over from earlier decisions

- Platform-neutral studio portfolio, not a Minecraft site.
- Simple but very professional. Keep slate #15171C, amber #F0B13E, Archivo,
  lowercase "afkbird".
- Layout B stays: homepage grouped by project type, one filterable Projects
  page, Discord button in the header.
- Downloads only link to GitHub Releases. No invented numbers anywhere.

## The eight topics (authored, except where noted)

1. **Vibe:** quiet, precise, a little playful. References: a small museum
   hall with matted prints, a pixel-art bird that naps.
2. **Journey:** who this is, what's new, walk the projects, the server, the
   community, how to reach the studio.
3. **Energy:** calm open, quiet ledger, the most movement in the projects
   hall, calm again after.
4. **Feeling and the one moment:** see the curve and peak below.
5. **The one thing no other site does:** the bird mascot walks the visitor
   through the projects and falls asleep (turns into the logo) when they stop.
6. **Distance from premium-minimal:** close to it (Robby's standing "simple
   but very professional"), with one playful device.
7. **One world or scenes:** distinct scenes.
8. **Assets (Robby):** brand kit and existing project art only.

## Journey

1. Recognition: an independent studio, its real work stacked in front of you.
2. Proof: the latest versions and dates, straight from GitHub.
3. Range: every project, grouped by type, labeled with facts.
4. Belonging: the server you can join, its live status.
5. Community: Discord first, then YouTube, X and GitHub.
6. Commitment: one plate with how to reach the studio.

## Feeling curve

| Act | Feeling | What causes it |
|---|---|---|
| Hero | curiosity | Real project art stacked like prints in front of the bird mark; the stack fans apart as you scroll (pinned stage, parallax planes) |
| Latest releases | calm confidence | A plain ledger of real version numbers and dates (flow, staggered entry) |
| Projects hall | delight (the peak) | Walking sideways past matted projects while a small bird hops along the frames with you (pan) |
| Servers | anticipation | A live status card wipes in (reveal) |
| Latest videos | curiosity, lighter | Thumbnails arrive in order (flow); hidden when the channel has nothing new |
| Community | warmth | The Discord card leans toward your pointer (tilt) |
| Close | resolve | One quiet label plate with the studio's facts and contacts |

**Authored silence:** none. The ledger is the quiet act before the peak.

## The peak

"A little bird hopped along the picture frames with me, and when I stopped
scrolling it fell asleep." Lives in the Projects hall, the longest act on the
page.

## Tell-someone sentence

It's the site where a bird walks you past every project and nods off if you
stop scrolling.

## Grammar

**Gallery / catalog.** The visitor's real question on a studio site is "what
do they make", which is a range question. Objects get one label schema
(title; type and platform; version and date; status; one factual line).

Why the other seven lost:
- Filmic one-shot: there is no single argument to carry anyone through.
- Chaptered editorial: there is no long-form story to read.
- Live surface: the studio is not one product.
- Continuous world: no real geography.
- Typographic poster: the projects have real art worth showing.
- Split stage: no two-sided comparison.
- Rhythmic cutlist: wrong energy for "simple but very professional".

Deviation, on purpose: the site header stays (Layout B needs the Projects,
About and Discord links on every page). The ledger and the hall's type
sections act as the index of objects.

## Signature move

**The AFK bird.** A small copy of the mark perches on the top edge of the
frame nearest the middle of the screen and hops to the next frame as the hall
pans. After seven seconds without scrolling, pointer movement, keys or touch,
its round eye becomes the X from the logo and a small "afk" tag appears; any
input wakes it. Coded in the page, not in the engine.

## Score

| Act | Device | Why |
|---|---|---|
| Hero | `pin` + `parallax` planes, `--sc-p` fan | Layered depth from real art, readable headline held the whole time |
| Latest releases | `flow` + `in` | Quiet before the peak |
| Projects hall | `pan` + bespoke bird | Lateral travel reads as range; largest span |
| Servers | `reveal` | A change of state for a live status |
| Latest videos | `flow` + `in` | Light, optional |
| Community | `tilt` + `in` | The page responds to the visitor being present |
| Close | label plate, held | Resolves on facts and one action |

Device families: pin, parallax, flow/in, pan, reveal, tilt (six). No family
twice in a row. No `scrub` (no video assets, by choice). Total length about
11 to 12 viewport-heights; the hall alone is about 6.

## Fingerprint gate

Registry was empty; this is the first row.

## Build report (Nov 8, 2026)

**Feel check (scrolled cold, one word per act):** curious, settled, delighted,
expectant, (videos hidden in the test build), warm, done. Matches the curve.
Changes made after the first pass: the hero's middle print covered the headline
at rest (moved right of the copy column); prints were stacked in the wrong
depth order (fixed with z-index); the bird stood off-screen when its frame ran
past the right edge (now clamped to the visible part of the frame); the phone
hall left half the screen empty (content is now centred vertically).

**Verified with screenshots:** desktop 1440x900, phone 390x844 and reduced
motion; hero at rest and mid-pin; bird awake, afk after 7 s idle, awake again
on mouse move; keyboard Tab order with every stop on screen (the hall scrolls
to the focused item); text contrast 6.1:1 or better; scroll-craft harness "no
dead scroll" on all three; shipcraft launch audit 0 fails after adding
og:image size/alt and twitter tags.

**Not verified:** a real phone (headless Chrome can't reproduce iOS Safari);
live server status, Discord counts and YouTube videos (the test machine
couldn't reach those services); release versions came from the real tags with
stand-in dates because the GitHub API was blocked there. GitHub Actions has
access, so the live build fills these in.
