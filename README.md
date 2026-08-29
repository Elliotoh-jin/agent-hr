# agent-hr

**HR for your AI agents.** A Claude Code skill that diagnoses agent-operations
problems with the tools of organizational design — written by an HR practitioner,
not an engineer.

---

## Why an HR person is publishing an agent skill

I work in human resources — organizational design, governance, the unglamorous
craft of making groups of capable people actually function. I also run a personal
multi-agent stack: a memory loop shared across surfaces, scheduled agent routines,
an ops registry that agents and I both write to.

And I kept hitting the exact walls the dev community posts about: an agent that
reports *"completed successfully"* while silently degraded for weeks. Context
that rots as it grows. A registry that only ever fills because every closure
waits on me. Summaries that quietly corrupt facts. The standing answer —
*wait for a smarter model* — never sat right with me.

Then it clicked: **none of these problems are new. They are the oldest problems
in my field, wearing new clothes.**

An agent that reports success while failing is the *"everything's on track"*
status culture every manager learns to distrust. Context rot is hour six of a
meeting forgetting hour one. Memory pollution is the telephone game that
corrupts any minutes kept without sources. And a human who approves everything
while the backlog grows — that is the founder who never wrote a delegation-of-
authority matrix. I have spent my career on these. So instead of waiting for a
better model, I did what my field does: **I treated my agents as a team, and
designed the organization around them.**

## The lens

> Your agent stack is an organization. Its failures are organizational failures.
> Most of them were solved decades ago — you just have to translate.

| What engineers report | What HR sees | The proven fix |
|---|---|---|
| Better models don't fix the workflow | Hiring smarter people into a broken org | Design the org (harness, contracts, gates), not the hire |
| Context rot | Onboarding docs nobody absorbs; hour-6 meetings | Hard-capped briefs; rules at the point of work |
| Agent says "done", artifact says otherwise | Status-report culture; report ≠ deliverable | Definition of Done; verify the diff, not the claim |
| Memory grows, retrieval and truth decay | Transcript graveyards instead of decision logs | Decisions **plus rationale and source**, nothing more |
| Everything queues on the human | Founder-approves-everything; no delegation of authority | Graduated, contract-based delegation |
| Delegated work comes back wrong | Self-graded homework | Segregation of duties: performer ≠ verifier |
| One frontier model for every task | The CEO attends every meeting | A delegation matrix by difficulty |

## The theory underneath

I did not want this to be vibes-with-a-metaphor, so the skill is anchored in the
bodies of knowledge HR actually runs on:

- **Principal–agent theory** (Jensen & Meckling, 1976). Every delegation is a
  principal–agent contract. The twist that makes AI different: an agent has no
  self-interest, so the *incentive-alignment* half of the theory drops out and
  only the *monitoring/structure* half remains. This is why culture prescriptions
  ("be honest in your reports") do nothing for agents, and why verification
  gates and separated grading do everything.
- **Management by Objectives** (Drucker) — delegate outcomes, not tasks — tempered
  by **Goodhart's law**: any numeric target an agent optimizes stops measuring
  what you meant. So the contract specifies outcomes by *exemplars and
  falsifiers*, with numbers only as a supplement.
- **Tacit knowledge** (Polanyi's "we know more than we can tell"; Nonaka &
  Takeuchi on externalization). "I know it when I see it" is not a delegation
  blocker — it is spec material. You externalize it the way creative fields
  always have: a mood board. One *"like this"*, one *"never like this"*.
- **Segregation of duties**, from the internal-control tradition: the performer
  never grades their own work. My first real incident was an agent scoring its
  own deliverable 8-for-8 against a spec it hadn't met — not dishonesty,
  response bias. Only structure fixes that.
- **High-reliability organizations** (Weick & Sutcliffe): no news is *not* good
  news. Dead-man switches and liveness logs are the agent translation of a
  preoccupation with failure.
- **Probation-to-permanent ladders**, the most ordinary HR mechanism there is:
  the first delegated round is fully human-reviewed; later rounds are
  sample-audited. Trust is not a prerequisite for delegation — **trust is what
  delegation, properly structured, produces.**

And, just as important, the four places the analogy **breaks** — where org
instinct will mislead you: agents reset memory every session (onboarding is
daily; contracts are standing documents), have no incentives (skip culture,
build structure), are clonable (over-invest in one good design), and cost
nothing to fire (run cheap delegation experiments now, don't accumulate trust
first).

## What the skill does

Five steps, in order, stopping at the first that resolves the problem:

1. **Translate** the symptom into its org problem (`references/prescriptions.md`)
2. **Locate** it on the trust chain — silent failure → costly verification →
   no trust → no delegation → human bottleneck. Fix upstream.
3. **Check the four asymmetries** before prescribing
4. **Gate** each queued judgment: judgment latitude × reversibility →
   "stays human" or "delegable"
5. **Contract** the delegable ones (`templates/delegation-contract.md`), running
   the `references/delegation-readiness.md` interview when the delegator's
   criteria are still tacit

## Does it work? (one live data point, honestly reported)

This framework runs my own stack. The first delegated contract — closing
expired items in an ops registry — produced, in round one: **one valid closure,
and two candidates *held* because the evidence showed their premises were still
alive.** The gate refusing to close what shouldn't be closed is the contract
working; a wrong closure would have been the failure. The utility verdict
(did delegation actually shrink the backlog?) has its own deadline. One pilot
is a data point, not proof — the skill ships with its falsifiers for a reason.

## Install

```bash
git clone https://github.com/Elliotoh-jin/agent-hr.git
# personal (all projects):
cp -r agent-hr ~/.claude/skills/agent-hr
# or per-project:
cp -r agent-hr your-repo/.claude/skills/agent-hr
```

Claude Code loads it automatically; it triggers on agent-ops debugging, agent
role/loop design, and "can I delegate this?" questions — or invoke `/agent-hr`.

## Extending

`references/prescriptions.md` is built to grow — PRs adding
symptom → org-problem → prescription rows are welcome, especially from people
who, like me, come from the org side rather than the engineering side. Our
field has been load-testing these mechanisms on humans for a century; the
agents are new, the problems aren't.

## License

MIT — see [LICENSE](LICENSE). Distilled from a live personal agent-ops system;
incidents generalized, metrics anonymized. — Elliot
([@Elliotoh-jin](https://github.com/Elliotoh-jin))
