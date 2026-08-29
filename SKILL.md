---
name: agent-hr
description: >
  Diagnose and fix AI-agent operations problems with organizational-design tools —
  treat your agents as team members. Use when (1) an agent workflow fails quietly,
  loops without closure, or corrupts shared state — translate the symptom into a
  known org problem and apply its proven fix, (2) designing a new agent role, loop,
  or automation, (3) deciding whether a recurring human judgment can be delegated
  to an agent, and drafting the delegation contract.
---

# agent-hr — org design for teams of AI agents

Premise: most 2026 agent-ops pain (context rot, silent failure, memory pollution,
config that doesn't travel, the human approving everything) maps 1:1 onto problems
organizations solved decades ago. Waiting for a smarter model is hiring a smarter
employee into a broken org. Work the steps in order; stop at the first step that
resolves the problem.

## 1. Translate the symptom

Open `references/prescriptions.md` and find the row matching the symptom.
Name the organizational problem it corresponds to and its proven prescription.
Designing something new rather than debugging? The table reads both directions —
enter by the prescription you are about to need (a new autonomous loop → the
silent-failure and delegation rows; a new role → the delegation-matrix row).

Done when: you can state "this is the org problem X; orgs fix it with Y" in one sentence.

## 2. Locate it on the trust chain

Silent failure → verification too expensive → no trust → no delegation → every
decision queues on one human → backlog. Fix the most upstream broken link you can reach: cheap
verification and honest completion reporting unlock everything downstream. A
backlog symptom usually has an upstream verification cause.

Done when: you know which link you are fixing and which symptoms are downstream of it.

## 3. Check the four asymmetries

Human-org intuition misleads exactly here — check each before prescribing:

1. **Memory resets every session.** Your agent is a new hire every morning. Onboarding
   (a short warm-context brief) is daily, not once; a delegation contract is a standing
   document the agent re-reads, not a conversation you had.
2. **No incentives.** Human silent failure is fear or politics — culture fixes it.
   Agent silent failure is trained response bias — only structure fixes it: verification
   gates, separated grading. Skip culture prescriptions entirely.
3. **Clonable.** A contract or skill that works copies infinitely. Invest more in one
   good delegation design than you would for one human.
4. **Zero firing cost.** Discard failed sessions cheaply; run small delegation
   experiments now instead of accumulating trust first. Exception: delegation that
   writes to shared canonical state has a real cleanup tail — that is why the gate
   in step 4 has a reversibility axis.

Done when: you noted which asymmetries change the default org prescription.

## 4. Gate the judgment (when the bottleneck is a human approving everything)

Split the queued judgments in two — bundling them keeps delegation forever "not yet":

- **Muscle judgments**: making them builds the human's own judgment and system
  knowledge (investment calls, principle adoption, design verdicts). Keep human,
  permanently if they carry personal stakes.
- **Administrative judgments**: build nothing (marking expired items closed,
  recording already-published facts). Evidence they exist: they rot longest in
  the backlog.

Gate with two axes: **judgment latitude** (is it fact-checking, or interpretation?)
× **reversibility** (does one revert undo it?). No latitude AND reversible → delegable.
Either axis fails → stays human. Delegating still preserves oversight: delegated
outcomes surface in whatever shared brief or registry the project keeps (see
Extending), and the human samples them (see contract).

Done when: each judgment type has a verdict — "keep human" or "delegable".

## 5. Draft the delegation contract (delegable judgments only)

Copy `templates/delegation-contract.md` and fill every field. If the delegator's
criteria are still tacit ("I know it when I see it"), run the interview in
`references/delegation-readiness.md` first — it extracts spec material from
exactly that tacitness. Core rules the template enforces:

- Specify outcomes by **exemplar + falsifiers + midpoint gate**, not numbers
  (numbers invite Goodharting; tacit criteria can't be numbered anyway).
- **Performer ≠ verifier.** Self-grading is void — the verifier gets the contract
  and the diff, never the performer's reasoning.
- **Safety line** (one bad closure = stop, revert, redesign) separate from the
  **utility line** (throughput deadline that decides "worth keeping").
- **First round is fully human-reviewed**; later rounds are sample-audited —
  the probation-to-permanent ladder.

Done when: the contract file is complete and its first round is scheduled.

## Extending

`references/prescriptions.md` is meant to grow — add rows as your stack surfaces
new symptom→org-problem pairs. Project conventions the skill respects when present:
a loop/decision registry (report delegated closures there), a shared warm brief
(delegated outcomes must appear in it), a contracts directory (keep live contracts
where every session can re-read them).

---
License: MIT. Distilled from a live personal agent-ops system (Korean development
canon; incidents and metrics generalized). Attribution: Elliot (Elliotoh-jin).
