# Symptom → org problem → prescription

Extensible catalog. Each row: what you observe in an agent stack, the organizational
problem it corresponds to, and the org-proven fix translated back into agent-ops
mechanics. Add rows as your stack surfaces new pairs — keep the three-column shape.

## Translation table

| Agent-ops symptom | Organizational problem | Prescription (org → agent translation) |
|---|---|---|
| Better models don't fix the workflow | Hiring smarter people into a broken org | Design the layer around the model first: harness, protocols, context — not model upgrades |
| Context rot — early instructions lose force as context grows | Hour-6 of a meeting forgets hour-1 agreements; onboarding docs nobody absorbs | Hard cap on the warm layer (short brief + expiry); put standing rules at the point of work (checklists/hooks), not in long documents |
| Memory grows but retrieval fails; summaries drift | Recording everything (transcript graveyards) instead of decisions | Decision log discipline (ADR): keep the decision **plus one line of rationale and source** — decision-only compression breeds telephone-game corruption |
| Config/setup doesn't travel between clients or machines | Transferring teams resets your tools, permissions, context | Single source of truth that crosses every boundary (one repo all surfaces read). Shadow cost: structural single point of failure — one broken generator/hook hits every surface at once; stage structural changes (canary) |
| Agent reports "ok" while degraded or dead | "Going well!" status culture; report ≠ artifact | Definition of Done as machine-checked eval; demo over report (verify the diff, not the claim); dead-man switches and liveness logs (no news is NOT good news) |
| One frontier model does every task, cost blows up | The CEO attends every meeting | Delegation matrix by difficulty: cheap models for routine (≈80%), frontier for hard calls (≈20%); pin models per job so routing can't silently drift |
| Rules keep being violated despite being written down | Policy memos lose to habit | Move the rule from prose into the system: hooks/gates that fire at the point of action. If a written rule is violated twice, it needs a machine |
| Every decision waits on one human; backlog grows | Founder-approves-everything, zero delegation-of-authority | Graduated delegation: risk-tiered authority, probation round, sample audits (see the delegation contract template) |
| Delegated work comes back wrong despite instructions | Delegation without acceptance criteria; self-graded homework | Separate performer and verifier; grade against explicit falsifiers; specification by exemplar (see delegation-readiness) |
| Centralized standard breaks every team at once | HQ process defect propagates to all branches simultaneously | Version-pin shared structure; canary structural changes on one surface before all; keep an independent second memory as an audit trail, not redundancy |

## The trust chain

```
silent failure → verification too expensive → no trust → no delegation
→ every judgment queues on one human → backlog / closure rate collapses
```

Fix upstream first. The backlog (rightmost) is almost never solved at the backlog.
The two highest-leverage upstream fixes: make verification cheap (diff-based,
machine-checked) and make completion reporting honest (DoD evals, dead-man switches).

## Where the analogy breaks (checklist)

| Asymmetry | Wrong org instinct | Correct agent-ops move |
|---|---|---|
| Memory resets per session | "We onboarded them already" | Daily warm brief; contracts as standing documents |
| No incentives | Psychological safety, culture change | Structural gates only (verification, separated grading) |
| Clonable | Invest per-head cautiously | Over-invest in one good design; it replicates for free |
| Zero firing cost | Rehabilitate the failing run | Discard and restart; run cheap delegation experiments early — except where shared canonical state makes failure sticky |
