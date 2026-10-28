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
