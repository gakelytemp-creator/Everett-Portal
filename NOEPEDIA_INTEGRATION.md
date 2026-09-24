# Everett Portal + Noepedia

> **Short description:** Noepedia is the planned live structured world-state, provenance, and relational-search layer for Everett Portal. It allows branch facts, causal relations, artifacts, births, versions, and open regions to remain addressable without forcing the alternate world into one giant prompt or one flat document archive.

Everett Portal is a particularly demanding Noepedia domain because several incompatible histories may occupy the same field.

The key rule is:

> **Canonical in a branch does not mean observed in our world.**

Every branch relation must remain connected, through ordinary SPO paths, to the branch/time/version/provenance context in which it holds.

---

## Division of responsibility

### Everett Portal

Everett defines the domain rules:

- shared trunk;
- Point of Divergence;
- causal morphing;
- branch time;
- LATENT / CANDIDATE / CANON progression;
- one-birth identity;
- world versions;
- generator versions;
- transmitted artifacts;
- portal provenance;
- lazy opening of world regions.

### Noepedia

Noepedia is intended to store and retrieve the structured world state:

~~~text
objects
relations
causal parents
world / branch scope
time / interval
world version
ruleset version
artifact identity
birth events
canon commitment
admission history
uncertainty
OPEN regions
raw artifact references
revision history
~~~

### Socratic Daimonion

Everett clients and generators do not directly rewrite persistent branch state.

The Daimonion mediates the transaction, retrieves the relevant branch cut, invokes domain-specific checks, preserves provenance, and controls admission or revision.

### Everett Consistency Gate

The Consistency Gate is **not** the Daimonion itself.

It is a domain-specific service used by the Daimonion when a candidate event or artifact seeks entry into branch canon.

It may combine:

~~~text
exact typed constraints
causal-neighborhood retrieval
identity / one-birth checks
semantic contradiction checks
novelty checks
confidence estimation
human or model escalation
~~~

The gate remains fallible and measurable.

---

## Branch context without changing the triplet format

Noepedia does not need an Everett-specific tuple.

The same storage form remains:

~~~text
SUBJECT ── PREDICATE ──> OBJECT
~~~

World, branch, time, version, provenance, and canon status are themselves objects and predicates in the same homoiconic field.

For example:

~~~text
NETWORK_41 → VALID_IN → EVERETT_BRANCH
NETWORK_41 → VALID_DURING → INTERVAL_1994
NETWORK_41 → USES_WORLD_VERSION → WORLD_V7
NETWORK_41 → HAS_STATUS → CANON
NETWORK_41 → HAS_PROVENANCE → ADMISSION_88
~~~

Every line is another SPO triplet.

The network handle is itself an object, so the field can describe the conditions of its own relations without adding metadata columns or an extended tuple.

This is what prevents **branch leakage** while preserving one homogeneous data model.

---

## Canon and confidence are different

Everett canon is an operational commitment inside one world version.

Noepedia should keep two different states:

~~~text
BRANCH COMMITMENT
    latent / candidate / canon / superseded

EPISTEMIC ADMISSION STATUS
    evidence / confidence / conflict / review / uncertainty
~~~

A branch may be committed to an event while preserving uncertainty about the process that admitted it.

A later correction creates a new world version rather than silently rewriting the old one.

---

## One birth and derivation

Every original artifact needs one addressable birth.

Derived objects should point back to it:

~~~text
ARTIFACT ── BORN_AT ──> BIRTH_EVENT

COVER / REMIX / TRANSLATION / REMASTER
        ── DERIVED_FROM ──> ORIGINAL_ARTIFACT
~~~

This lets Noepedia distinguish legitimate derivation from a duplicate "second original."

---

## Lazy world opening

Most of the alternate world should remain unopened.

A request such as:

~~~text
1994 / Manchester / music / interview
~~~

should retrieve or resolve only the causal region required to support that coordinate.

Unopened space remains OPEN.

It is not fabricated in advance.

The Daimonion can generate requirements for missing causal predecessors and then return a bounded branch-specific semiotic cut to the artifact generator.

---

## Search examples

Noepedia should eventually let Everett ask:

~~~text
Show this person in both branches at the same date.

Which facts support this newspaper?

Which later artifacts depend on this event?

What changed after the POD in this city?

Is this candidate a second original?

Which events were admitted with low confidence?

What remains OPEN around this coordinate?

Which world-version correction invalidated this artifact?
~~~

Search results must never silently merge different branches.

---

## GitHub and Noepedia

GitHub remains valuable for:

- white papers;
- protocols;
- human-readable design history;
- public review;
- exported branch snapshots;
- reproducible world/version manifests.

Noepedia is intended to become the **live structured world-state and search layer**.

The two roles are complementary.

The detailed pilot requirements are maintained in Noepedia:

[Noepedia Pilot: Everett Portal](https://github.com/gakelytemp-creator/Noepedia/blob/main/PILOT_EVERETT_PORTAL.md)

---

## Short formula

> **Everett defines the worlds.**
>
> **Noepedia preserves their structure and the ordinary relational paths that locate each branch in context.**
>
> **The Consistency Gate checks branch admission.**
>
> **The Daimonion guards the transaction and prevents silent world mixing.**
