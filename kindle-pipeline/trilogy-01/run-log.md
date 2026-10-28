# Run log: Trilogy 01

## 2026-10-28 · Agent 1, Market Research (manual run)
- **In:** category sapphic romance; trope of interest werewolf fated mates; constraints taken from the voice guide.
- **Out:** `00-brief/brief.md` with 3 concepts. Pick: A, *Moonbound*. Status: needs your decision.
- **What broke:**
  - The spec assumes a top-100 list is available. Amazon couldn't be reached from the cloud session, so web-search snapshots stood in for it. Fix: put "paste the live top 100" as a required step before the run, or allow the domain in the session's network settings.
  - "Count of the 100 per trope" can't be produced from snapshots. Fix: the prompt should allow a directional ranking when it gets fewer than 100 titles.
  - The inputs "tropes of interest" and "constraints" were blank. Fix: add defaults to the spec (heat level, world type) so the agent doesn't guess.

## 2026-10-28 · Checkpoint: concept chosen
- Aashrita chose concept A, *Moonbound*. Saved to `00-brief/chosen-concept.md`.

## 2026-10-28 · Agent 2, Series Planner, Part 1: world document (manual run)
- **In:** `chosen-concept.md` and the voice guide. Heat level is still assumed from the voice guide.
- **Out:** `01-world/world.md` (setting, 9 rules, factions, couple, pressures). Status: waiting for Aashrita's approval before Part 2.
- **What broke:**
  - The spec doesn't say who names the leads. The planner named them (Tamsin Rook and Senna Ashgrave). Fix: add a "name the couple" step, or names as an input.

## 2026-10-28 · Checkpoint: world approved
- Aashrita approved `world.md` and kept the names (Tamsin Rook, Senna Ashgrave) and the heat level (1-2 on-page love scenes per book).

## 2026-10-28 · Agent 2, Series Planner, Part 2: trilogy outline (manual run)
- **Out:** `02-outline/trilogy.md` (premise, 3 book outlines of 28/27/27 chapters, love scenes marked, cliffhangers) and `03-bible/bible.md` v1 seeded from the world doc. Status: done.
- **What broke:**
  - The story bible template needs character looks, but neither the world doc nor the outline step asks for them. The planner invented them while seeding the bible. Fix: add "looks" to the world doc's couple section.
  - The Drafter needs the voice sample, which doesn't exist yet. Fix: make writing the voice sample an explicit step (Planner or a human) before the Drafter.

## 2026-10-28 · Revision: simpler names (Aashrita's request)
- People: Tamsin Rook -> Cass Reed; Senna Ashgrave -> Mara; Maud -> Ruth; Rhoswen -> Lena; Penhallow -> Voss; Odile Marsh -> June; Bram Corrie -> Theo; Grisel -> Rhea; Hester Vane -> Agnes.
- Places and packs: Shale Reach -> the Reach; Vellmark -> Stonebridge; Ashgrave -> Highwood; Corrie -> the River pack; the Hollow is unchanged.
- Applied to world.md, trilogy.md, bible.md and chosen-concept.md. Earlier entries in this log keep the old names.
- **What broke:** the names were too ornate and there were too many of them. Fix: add a naming rule to the Planner spec: short, easy to pronounce, one name for minor characters, and place names in plain English.

## 2026-10-28 · Voice sample drafted
- `voice-sample.md`: one page (Book 1, chapter 2, at the Highwood gate). Status: waiting for Aashrita's approval before the Drafter runs.

## 2026-10-28 · Checkpoint: voice sample approved

## 2026-10-28 · Agent 3, Drafter + Agent 4, Continuity Keeper: Book 1, chapter 1 (manual run)
- **Out:** `04-drafts/book1/ch01.md` (2,493 words), `summaries.md`, bible v2, `03-bible/factsheet-b1-ch02.md`.
- **The Continuity Keeper caught 2 contradictions, both fixed:**
  - A full-form wolf was killed on open ground, which breaks the shifting rule. Changed to half-shifted.
  - "The old Highwood line lapsed last spring" contradicts the first-snow deadline. Changed to the separate east spur.
- **What broke:**
  - The first draft was 2,545 words, over the 2,500 limit, and had to be trimmed. Fix: tell the Drafter to aim for about 2,300 so revisions have room.
  - The Drafter spec's heat example ("one in book 2, a bigger payoff in book 3") doesn't match the outline, which puts a love scene in Book 1 chapter 21. Fix: align the spec with the outline, or confirm Book 1 has one.
  - The voice sample is actually chapter 2's scene. That's handy, but the Drafter needs a rule on whether to reuse it word for word.
