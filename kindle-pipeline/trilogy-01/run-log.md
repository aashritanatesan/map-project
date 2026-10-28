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

## 2026-10-28 · Agents 3 + 4: Book 1, chapters 2 to 28 (manual run, whole book in one go at Aashrita's request)
- **Out:** chapters 2 to 28 in `04-drafts/book1/`, the compiled `book1-full-draft.md` (about 58,000 words, 28 chapters, each 2,000 to 2,500 words), `summaries.md` for every chapter, bible v29.
- **Love scene:** Book 1, chapter 21, kept as Aashrita asked.
- **The Continuity Keeper caught and fixed about 20 contradictions** (all listed in the bible's contradiction log). They fall into these groups:
  - Powers the bond doesn't have, which the draft kept slipping into: telepathy, sharing scent, a "missing" compass.
  - Shifting rules: wolves shown unable to shift on their own ground.
  - Moon and day timeline.
  - Counts and distances: cairn counts, bridge length vs chain length, Cass's age and years of training.
  - Logic of the deadline: what "first snow" means. Resolved with the oath-card definition, which is now canon.
- **Outline changes made while drafting** (the Planner should fold these into `trilogy.md`):
  - The last chain-length is at the true Nine on the way back down, not at Thirty-One.
  - The second surveyor is named Ambrose Holt.
  - Theo's mother leads the River council.
  - The Hollow elder gives Cass a brass link marked J.M.
  - Lena's team rebuilds the false cairns.
- **What broke:**
  - Drafts kept coming in about 300 to 400 words short and needed a second pass. Fix: the Drafter prompt should ask for about 2,400 and list the scenes.
  - Repeated phrases built up across chapters ("very still" 18 times, "for a long moment" 17). A cleanup pass cut them to 6 and 7. Fix: the Continuity Keeper should check repeated phrases every 5 chapters, not only facts.
  - The bond's rules (feelings yes, thoughts no) were the most common slip. Fix: add an explicit "what the tether can't do" list to the world doc.
  - Doing a full bible update after every chapter was slow, so updates were batched every 4 to 7 chapters. Each chapter still has its own facts entry. Fix: allow batching in the Continuity Keeper spec.
- **Next:** Agent 5, the Editor (a full read, at most two rounds, a short report), then your final read.

## 2026-10-28 · Agent 5, Editor: Book 1 (manual run)
- **In:** all 28 chapters (read in full), bible v29, voice guide, outline.
- **Round 1:** 12 continuity and plot fixes, about 8 repetition fixes, one scene reordered (ch18). No cuts for pacing.
- **Round 2:** every fix re-checked in context, plus the global checks (names, tell timing, lengths). Clean.
- **Out:** `05-edited/book1/manuscript.md`, per-chapter files, `report.md`. Status: waiting for Aashrita's final read.
- **What broke:**
  - The Continuity Keeper missed day-count errors in dialogue ("two days ago" and the like). Fix: the bible needs a day-by-day timeline table, and the Keeper should check every relative time phrase against it.
  - Scene order inside a chapter (ch18) isn't checked by anyone. Fix: add an in-chapter chronology check to the Editor's round 1.
