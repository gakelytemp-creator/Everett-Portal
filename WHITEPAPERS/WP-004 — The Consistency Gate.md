# WP-004 — The Consistency Gate

**Status:** Open problem (this paper states a problem; it does not solve it)
**Provenance:** OUR SIDE
**Depends on:** WP-001, WP-002, WP-003

---

## Why this paper exists

The working agreement rests on one component it has so far treated as given: the **gate** that decides which candidate artifact may enter canon — checking it for consistency with established history and for novelty against everything already born.

Almost every other guarantee sits *downstream* of this gate:

- "The newspaper reads history" holds only if the gate reliably rejects a rendering that contradicts established state.
- "Reject the second original" holds only if the gate reliably recognises that two artifacts share a birth.
- "Facts are discrete, influence propagates continuously" is a clean picture — but a fact still enters the world *through the gate*, and if the gate admits a contradicting fact, discreteness does not save us.

So the gate is not one component among many. It is the load-bearing organ, and it is the part we have not solved. This paper's job is to say exactly what it must do, where it is tractable, and where it is not — so that no one downstream mistakes it for solved.

## What the gate must do

Given a candidate and the current world state, the gate performs two semantic operations:

1. **Consistency check** — does the candidate contradict any established fact in the relevant causal region?
2. **Novelty / identity check** — is this a genuinely new artifact, or a re-instance of one already born (a duplicate original, as opposed to a legitimate cover or remix that points back to a first birth)?

Both are judgments over *meaning*: entailment for the first, similarity for the second.

## Why it is hard

At the scale and richness of an alternate history, both operations are approximate and fallible:

- **Global consistency is not cheaply decidable.** Checking a candidate against *all* established state is intractable; checking against a *bounded* region is tractable but unsound — a contradiction outside the checked region leaks.
- **"Novelty" has no crisp boundary.** Two songs, two events, two arguments can be near-duplicates by any number of partial measures with no natural threshold.
- **A fallible judge leaks in proportion to its error rate.** If the gate is an LLM — or any statistical judge — contradictions and duplicate-originals enter at some rate, and *every guarantee above degrades with that rate.* The soundness of the whole architecture is bounded by the reliability of this one organ.

## What helps — and what it does not fix

A **structured, typed canon** (propositions as typed triples rather than free prose) makes a *subset* of the consistency check computable: some contradictions become graph-constraint violations that can be detected exactly and cheaply, without semantic entailment.

This is real and worth pursuing. But it must be stated honestly: **structure makes the check cheaper, not sound.** It does not make global consistency decidable, it does not make "novelty" crisp, and it only covers the fraction of real cultural consistency that is expressible as typed constraints. The irreducibly semantic remainder stays fallible.

## Candidate directions (open — not answers)

Each of these is a direction to investigate, with its own unresolved question:

- **Bounded causal-neighborhood checking.** Check consistency within a scoped region of the causal graph rather than globally. *Open:* how large a neighborhood is "enough," and what class of contradiction can still escape it?
- **Typed canon + computable local checks.** Push as much consistency as possible into exact graph constraints. *Open:* how much of real cultural consistency is expressible this way, and how do we characterise what is left?
- **Graded confidence instead of a binary verdict.** Let the gate emit an admission *confidence*, so canon carries the uncertainty of its own admission rather than hiding it behind a yes/no. *Open:* how does downstream generation consume a confidence-weighted canon, and how is the confidence calibrated?
- **Human backstop for low-confidence or high-stakes admissions** (the "skeptics" role). *Open:* reactive, not preventive — what triggers escalation, and who adjudicates?
- **Layered gate.** Cheap structural checks first; expensive semantic checks only when the cheap ones pass. Engineering, not a resolution — but it bounds cost.

## What would count as progress

Not "a perfect gate" — that is not on offer. Progress is:

1. A precise map of which consistency properties are **computable** versus **irreducibly semantic**.
2. A **measured** error rate against a benchmark of planted contradictions and planted near-duplicates — so the gate's reliability is a number, not a hope.
3. A **graded, calibrated** admission output rather than a binary one.
4. A **defined escalation path** for low-confidence or high-consequence cases.

Each of these is falsifiable. That is the point: turn the gate from an assumed component into a measurable research program.

## The line for the working agreement

> The consistency/novelty gate is an open problem. Its reliability bounds every guarantee above it. It is not yet a solved component.

---

*This paper does not claim to close the problem. It claims to name it correctly. Break any part of the framing that is wrong — especially the computable/semantic boundary, which is where the real leverage is.*