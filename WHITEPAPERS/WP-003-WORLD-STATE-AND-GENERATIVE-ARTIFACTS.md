# Everett Portal White Paper WP-003

## World State and Generative Artifacts

**Status:** Draft  
**Version:** 0.1  
**Project:** Everett Portal  
**Class:** Architecture / Continuity

> **LLMs render artifacts; they do not own the world's historical state.**

---

## Abstract

The largest technical risk in Everett Portal is continuity failure.

If every newspaper, interview, song, and radio broadcast is generated directly by a stochastic language or media model, the alternate world will rewrite itself every time it is queried.

This paper separates the system into two layers:

1. a persistent, reproducible **World State**;
2. probabilistic **Artifact Generators** that render views of that world.

The newspaper does not create the history.

The newspaper reports a history that already exists.

---

## 1. The Architectural Separation

### World Layer

Responsible for:

- entities;
- dates;
- relationships;
- causal links;
- canonical events;
- branch parameters;
- world seed;
- generator version;
- provenance;
- artifact identity.

### Artifact Layer

Responsible for rendering:

- music;
- radio;
- interviews;
- newspapers;
- magazines;
- posters;
- paintings;
- advertisements;
- narrative documents.

The artifact layer may be stochastic.

The world layer must remain stable.

---

## 2. Deterministic World Query

Conceptually, a world-state query has the form:

`G(world_seed, branch, coordinate, causal_graph, ruleset_version) → state`

A coordinate may include:

- time;
- place;
- domain;
- entity;
- scale.

The same inputs under the same frozen ruleset must reproduce the same structural result.

---

## 3. Lazy Causal Simulation

The project does not simulate the whole Earth in advance.

A requested artifact opens only the causal region required to support it.

For example:

`1994 / Manchester / music / interview`

may require the system to resolve:

- the band’s formation;
- its members;
- earlier releases;
- influences;
- tours;
- conflicts;
- local scene history.

Unrelated regions remain latent.

This is **lazy causal simulation**.

---

## 4. Persistent Canon

Once a structural fact is accepted, it enters canon.

Canon must be queryable by later generators.

If a 1988 radio broadcast establishes that a band has three members, a 1994 magazine cannot silently invent a fourth founding member.

Contradictions must be:

- rejected;
- explicitly explained as later changes;
- or introduced through a versioned correction process.

---

## 5. Generator Versioning

A deterministic seed is not enough.

If the ruleset changes, the same seed may produce a different world.

Therefore world identity includes at least:

`World = seed + branch + ruleset_version`

Major revisions create a new world version rather than silently mutating the old one.

Git history should preserve the evolution of the rules.

---

## 6. Creative Generation

When the World Layer opens a creative window, it provides constraints such as:

- creator;
- date;
- location;
- social context;
- active influences;
- prior works;
- available technologies;
- current cultural field;
- unresolved creative degrees of freedom.

A music or language model may then generate several candidates.

Candidates are not yet history.

---

## 7. Novelty Gate

Before acceptance, a candidate passes through a Novelty Gate.

The gate checks:

1. duplication;
2. excessive similarity;
3. contradiction with canon;
4. causal plausibility;
5. provenance completeness;
6. identity collision with existing artifacts.

Only accepted candidates become canonical artifacts.

---

## 8. Artifact Identity

An artifact must not be identified only by:

- title;
- date;
- genre;
- filename;
- performer label.

Identity should include structural and causal features.

A useful conceptual form is:

`Artifact Identity = structure + semantics + causal origin + birth event`

This prevents metadata changes from manufacturing false novelty.

---

## 9. Provenance

Every portal artifact should carry both human-visible and machine-readable provenance.

Human-visible:

- Ǝ portal mark;
- branch label;
- date;
- origin class.

Machine-readable:

- world version;
- artifact ID;
- causal parents;
- generator/version;
- canonical status;
- generation record.

Future versions may add cryptographic signatures or robust content credentials.

---

## 10. Checkpoints and Caching

The world generator does not need to recompute the entire branch from the POD for every query.

It may preserve compact checkpoints:

- state vectors;
- graph snapshots;
- canonical event sets.

These are acceleration structures.

They do not replace the world-generation rules.

---

## 11. The Core Continuity Rule

A generated newspaper may be rewritten.

A generated radio script may be rendered in another voice.

A song may receive another mix.

But none of these operations may silently rewrite the historical state they refer to.

---

## 12. Core Statement

> **The world is upstream of the artifact.**

This ordering is what allows independently generated fragments to belong to the same alternate Earth.
