# Run log: Trilogy 01

## 2026-10-28 · Agent 1, Market Research (manual run)
- **In:** category sapphic romance; trope of interest werewolf fated mates; constraints taken from the voice guide.
- **Out:** `00-brief/brief.md` with 3 concepts. Pick: A, *Moonbound*. Status: needs your decision.
- **What broke:**
  - The spec assumes a top-100 list is available. Amazon couldn't be reached from the cloud session, so web-search snapshots stood in for it. Fix: put "paste the live top 100" as a required step before the run, or allow the domain in the session's network settings.
  - "Count of the 100 per trope" can't be produced from snapshots. Fix: the prompt should allow a directional ranking when it gets fewer than 100 titles.
  - The inputs "tropes of interest" and "constraints" were blank. Fix: add defaults to the spec (heat level, world type) so the agent doesn't guess.
