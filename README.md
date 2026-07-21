# Trailheads — Curiosity-Driven Paper-App Studio

A sister site to the [Instructor Study](https://buildlittleworlds.github.io/instructor-study/). One page per session, starting at Session 3: each takes the week's AI idea, restates it as a *traveling question*, and marks trailheads from it into six recurring interest lanes (living things, games & play, music & sound, stories & words, art & pictures, everyday life) plus a seventh lane that always points the idea back at the student's own app.

**Live site:** https://buildlittleworlds.github.io/paper-app-trailheads/ (repo `paper-app-trailheads`)

## Course boundary

Trailheads is possibility space, wider than the Instructor Study's demonstrations. Nothing here is an assignment: no card is required, and no page collects, exports, or aggregates anything a visitor does. Cards are invitations with vetted questions; the Bench (Session 5 onward) deals nothing — it only assembles prompts from what the student types about their own app, and nothing typed is saved or sent.

One honesty rule travels on every page, inherited from the course's "a transformer is not a cellular automaton" discipline: **analogies find questions, not answers** — the idea travels; the mechanism doesn't.

## Structure

```text
index.html                 hub: lanes, how to wander, session shelf
session-04/                Who writes the rules? (first built page; template for the pre-hinge shape)
session-03/ … session-10/  one page per session, built one week ahead of class
```

## Page anatomy

Header (traveling question) → the bridge from the Instructor Study page → lane chips + 10–15 idea cards → the Bench (Session 5 onward) → honesty note. The page is a generator, not a worksheet — with one deliberate exception: the Bench asks the student to type a few facts about their own app, then assembles prompts from those answers; nothing typed is saved, sent, or survives the tab.

Every card carries **two copy-ready prompts**. On the Session 3–4 pages these are a *starter build* and a *bigger build* (same idea, more ambitious — still one static page). From Session 5 on — the course's hinge into one deepening project — cards swap the bigger build for **Where it could go**: two or three branch questions showing how the small build could keep growing, some tagged with the future session that hands the student the tool (yardsticks in 6, repair in 7, naming in 8, order in 9, authorship in 10). Their two prompts are a *try-it* (build the smallest version now, then stop; the branch map rides along in the prompt so the same AI chat becomes the place to iterate) and a *branch prompt* (the AI interviews the student first, proposes three versions, and waits for a pick before writing any code). The Bench (Session 5 onward) starts from the student's own app instead of an authored card: what did you build, which knob did you pick without thinking, what do you predict a change would do — then it emits a build prompt and an interview prompt assembled from those answers, useless to anyone who didn't fill in the boxes. (The Dealer, which shuffled authored fragments into combinations, was removed on 2026-07-21; Sessions 3–4, being pre-hinge, now have cards only.) All build prompts instruct the AI to work in stages — smallest core first, then one addition at a time — so ambitious builds stay finishable.

## Authoring a new session page

1. Copy `session-05/` to `session-0N/` (for a pre-hinge starter/bigger page, copy `session-04/` instead).
2. Edit the header, byline, and bridge copy.
3. Replace the marked script blocks: `EDIT HERE: CARDS` (the card array) and `EDIT HERE: BENCH` (the Bench's two prompt builders).
4. Seed content for every session lives in the parent course folder's `trailheads-site-plan.md`.

Pages are fully self-contained — no fetch, no dependencies, no data folders; they work from `file://`.

## Preview & deploy

Open any `index.html` directly, or `python3 -m http.server 8000` from this folder. Deploy: create the GitHub repo, push, enable Pages (main branch root). Add `.nojekyll` before first deploy.
