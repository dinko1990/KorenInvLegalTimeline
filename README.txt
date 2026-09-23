Koren Constructor Timeline & Evidence – v4

Open index.html in a modern browser (double-click works, no server needed).

New in v4:
- Data now lives in data.js (plain JS/JSON), separate from index.html, so it's easy to
  hand-edit and diff in git. index.html loads it with <script src="data.js"></script>.
- Every timeline event now has a "type": legal | contractor | defects | payment | general.
  Colour-coded pills at the top of the Timeline tab filter by type; each event card is
  colour-coded on its left border to match.
- "Milestone" is a separate flag (not a type) so any event -- a payment, a legal letter,
  a signed agreement -- can be starred as an important milestone. All settlement-related
  dates (12 Dec 2025 meeting, 5/7/19 Jan 2026 signing chain, the 13 May 2026 legal letter,
  the 3 Jul 2026 warranty claim) are marked this way. Use the "Milestones only" pill to
  see just those.
- Events are now fully editable, not just addable: click "Edit" on any event card to
  change its date/type/title/text/milestone flag, or delete it.
- Added ~20 new events and 9 new evidence files pulled from the Gmail threads supplied
  after v3 (E-REDES payment, the Jan 2026 settlement-signing chain, the Aguas do Porto
  vistoria request/scheduling/correction chain, the Apr 2026 "Reiteracao de Prazo" legal
  letters, the May 2026 lawyer-to-lawyer letter over invoice FP 2026/1, the ACDC and
  Coordenada Logica warranty declarations, and the Jul 2026 urgent warranty complaint).
  Cross-checked against existing v3 events to avoid duplicating the same underlying issue.
- New evidence source PDFs are under /evidence with the same names referenced in data.js.

Working locally / pushing to GitHub:
- Everything is static (HTML + JS + files under /evidence, /thumbs) -- this works as-is
  on GitHub Pages. Just push the whole folder to a repo and enable Pages on it.
- To edit data day-to-day: either use the in-app "+ Add event" / "Edit" UI (changes save
  to your browser's localStorage immediately), or edit data.js directly in a text editor.
- To turn browser edits into something you can commit: click "Download data.js" in the
  Timeline toolbar -- it writes out the current in-app state (including anything you
  added/edited/deleted) as a ready-to-commit data.js file. Replace the repo's data.js
  with it and push.
- "Backup JSON" / "Import JSON" still work for quick round-trips of the whole dataset
  (events + evidence + payments) if you prefer JSON over JS.
- "Reset edits" clears localStorage and reverts to whatever is currently in data.js.

Evidence source files remain under /evidence.
