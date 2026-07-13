# Trailheads — Curiosity-Driven Paper-App Studio

A sister site to the [Instructor Study](https://buildlittleworlds.github.io/instructor-study/). One page per session, starting at Session 3: each takes the week's AI idea, restates it as a *traveling question*, and marks trailheads from it into six recurring interest lanes (living things, games & play, music & sound, stories & words, art & pictures, everyday life) plus a seventh lane that always points the idea back at the student's own app.

**Live site:** https://buildlittleworlds.github.io/paper-app-trailheads/ (repo `paper-app-trailheads`)

## Course boundary

Trailheads is possibility space, wider than the Instructor Study's demonstrations. Nothing here is an assignment: no card is required, and no page collects, exports, or aggregates anything a visitor does. Cards are invitations with vetted questions; the Dealer is labeled as a shuffle, not a syllabus.

One honesty rule travels on every page, inherited from the course's "a transformer is not a cellular automaton" discipline: **analogies find questions, not answers** — the idea travels; the mechanism doesn't.

## Structure

```text
index.html                 hub: lanes, how to wander, session shelf
session-04/                Who writes the rules? (first built page; doubles as the template)
session-03/ … session-10/  one page per session, built one week ahead of class
```

## Page anatomy

Header (traveling question) → the bridge from the Instructor Study page → lane chips + 10–15 idea cards → the Dealer → honesty note. The page is a generator, not a worksheet: nothing asks the student to answer or fill anything in.

Every card carries **two copy-ready prompts**: a *starter build* (the smallest version) and a *bigger build* (same idea, more ambitious — still one static page), each described in plain English on the card. The Dealer shuffles a territory object × an aspect of the week's idea × a reader action, then explains what the combination means and what it might produce, with the same two prompt tiers. Bigger-build prompts instruct the AI to work in stages — smallest core first, then one feature at a time — so ambitious builds stay finishable.

## Authoring a new session page

1. Copy `session-04/` to `session-0N/`.
2. Edit the header, byline, and bridge copy.
3. Replace the three marked script blocks: `EDIT HERE: CARDS` (the card array), `EDIT HERE: DEALER` (the three wheels).
4. Seed content for every session lives in the parent course folder's `trailheads-site-plan.md`.

Pages are fully self-contained — no fetch, no dependencies, no data folders; they work from `file://`.

## Preview & deploy

Open any `index.html` directly, or `python3 -m http.server 8000` from this folder. Deploy: create the GitHub repo, push, enable Pages (main branch root). Add `.nojekyll` before first deploy.
