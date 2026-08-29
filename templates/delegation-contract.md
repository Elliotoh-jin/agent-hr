# Delegation contract — template (v1)

Copy per contract. One page maximum — agents re-read this every session (memory
resets), so brevity is a functional requirement, not style. Keep live contracts in
a directory every session can reach; list them in a small index with status.

```markdown
### Contract ID · version · date
### Delegator / Performer / Verifier   ← performer = verifier voids the contract

### A. Delegation gate — may this judgment be delegated at all?
- Judgment latitude? (interpretation/preference involved, vs pure fact-checking)  Yes/No
- Irreversible? (cannot be cheaply undone — revert, republish)                    Yes/No
→ Any Yes: keep it human. Both No: proceed.

### B. Outcome specification (numbers only as a supplement)
- Exemplars: one "like this" artifact (path/quote) / one "never like this"
- Falsifiers: "it failed if…" list — the verifier's rubric is this list, nothing else
- Midpoint gate: ~20% checkpoint + who reviews it
  (recurring work: replace with a fully-reviewed first round)

### C. Authority & scope: exactly which files/actions; everything unlisted is off-limits.
   Per-round cap on volume.

### D. Grading structure
- Verifier receives the contract and the diff only — never the performer's reasoning.
  A failed item is reverted, not argued.
- Human sampling: cadence and rate (e.g., weekly, one random closed item)

### E. Reporting: where outcomes surface (commit + shared brief + one-line round summary)

### F. Kill criteria — safety and utility are separate lines
- Safety line: instant-stop condition (e.g., one wrong closure → stop, revert, redesign)
- Utility line: throughput floor + verdict date ("not worth keeping" is a valid outcome)

### G. Feedback: criteria discovered mid-work (verifier findings, midpoint gates) are
   folded back as falsifier additions with a version bump. The contract is a growing
   document, not a finished one.
```

## Worked example — registry expiry-closure (generalized)

A personal ops registry accumulated open items whose premises had died (a binary
catalyst resolved months ago still marked "imminent"). Closing them is pure
fact-checking — the classic administrative judgment that rots longest.

- **Gate**: latitude No (premise-death is a fact with a source), irreversible No
  (registry is in git). → Delegable.
- **Exemplar**: "closed with `[expired 2026-08-29: catalyst voided by X (date, link);
  surviving concern re-registered separately]`" / **Never**: "closed as 'done' with
  no source" (the incident that motivated the falsifier list).
- **Falsifiers**: ① closure without source ② expiry reason is interpretation, not
  fact ③ edits outside the target item ④ item that merely needs a new date dressed
  up as expired ⑤ fact-recording that crosses into verdict-making.
- **Grading**: separate verifier agent gets contract + diff; human samples one
  closed item weekly. First round fully human-reviewed.
- **Kill**: safety = one wrong closure → stop; utility = backlog halved in 4 weeks,
  else "not worth keeping".
- **Observed effects, first round**: 1 valid closure; 2 candidates *held* because
  evidence showed their premises still alive — the gate preventing wrong closures
  is the contract working, and held-with-evidence is a success outcome.

License: MIT.
