# Materials Trade Study Framework

## Purpose

This document defines how IX-Mirror compares material and wall-stack candidates.

It exists to prevent a common failure mode in radiation-concept work: picking a
material because it sounds powerful, dense, advanced, or exotic without
screening it against the actual crew-protection problem.

IX-Mirror does not treat material choice as a beauty contest or a density
contest. It treats material choice as a structured trade involving:

- threat specificity
- areal density
- likely secondary-radiation penalties
- integration with chambered architecture
- structural usefulness
- fault tolerance
- habitability
- maintainability
- compatibility with shelter-first logic

This framework does **not** claim final ranking results. It defines how ranking
and screening are to be done.

## Why this framework exists

A technically serious shielding repository needs a disciplined answer to the
question:

**How do we decide whether one material direction is better than another for
IX-Mirror?**

The answer cannot be:

- “heavier must be better”
- “space-grade sounding must be better”
- “a patent mentions it, so use it”
- “it did well in an unrelated terrestrial radiation context”
- “it feels futuristic”

This framework forces each candidate to compete on the same ground.

## Scope

This framework applies to the following material or stack classes:

- candidate crew-wall materials
- chamber-fill media
- crew-side liners
- neutron-conscious support layers
- local specialty inserts
- multifunctional structural shielding materials
- retained-water and hydrogel media
- comparison-only dense-material branches

This framework applies to both **single material classes** and **multi-layer
stack concepts**.

## Primary trade-study question

The primary question is:

**Which material families and wall-stack combinations are most credible for
IX-Mirror’s shelter-first, low-Z-biased, crew-centered architecture under
explicit GCR and SPE / SEP claim boundaries?**

## Secondary trade-study questions

The framework should also help answer:

- Which materials are strongest candidates for chambered shelter architectures?
- Which materials help most against acute-event protection goals?
- Which materials look attractive at first but are penalized by secondaries,
  mass overhead, or poor crew-wall fit?
- Which materials are useful for local electronics protection but poor as a
  default crew-wall answer?
- Which materials are multifunctional enough to justify carrying them as part of
  the habitat structure?
- Which materials support graceful degradation, maintainability, and modularity?
- Which materials are compatible with consumables-aware sheltering?

## Material candidate classes

IX-Mirror organizes material candidates into the following broad classes.

### Class A — Low-Z hydrogen-rich polymers

Examples include:

- polyethylene-family materials
- HDPE-class systems
- UHMWPE-class systems
- hydrogen-rich polymer composites
- structural systems that preserve low-Z logic

These are baseline-priority classes.

### Class B — Water and retained-water media

Examples include:

- free water in controlled chamber systems
- water-equivalent media
- hydrogels
- retained-water polymer systems
- water-bearing modular packs

These are baseline-priority classes for chambered and shelter-focused concepts.

### Class C — Boron-aware and neutron-conscious support materials

Examples include:

- boron-containing polymer branches
- BN / BNNT-related branches
- neutron-conscious support layers
- boron-assisted composite directions

These are support-class candidates, not automatically bulk-wall defaults.

### Class D — Multifunctional structural shielding candidates

Examples include:

- structural composites with credible shielding relevance
- hybrid low-Z structural skins
- layered structural candidates that also support chamber integration
- materials that reduce parasitic mass by serving more than one role

These are strong candidates when they preserve crew-wall logic.

### Class E — High-Z or dense local-use candidates

Examples include:

- tungsten
- lead
- dense metallic foil stacks
- graded-Z local insert concepts
- dense local shielding tiles for hardware-only cases

These are restricted-use comparison candidates unless a branch explicitly
justifies a narrower local role.

### Class F — Exotic or speculative candidates

Examples include:

- novel composite chemistries not yet well characterized
- deployable shielding media with limited public evidence
- unusual layered stacks proposed mainly by inference
- active-field-compatible materials branches

These may remain in the repository, but they must be screened carefully and
must not silently enter the baseline.

## Baseline material philosophy

IX-Mirror uses the following material hierarchy by default.

### Baseline priority

Highest priority is given to candidates that are:

- low-Z
- hydrogen-rich
- crew-wall compatible
- useful in chambered architectures
- likely to help more for SPE / SEP than they hurt through penalties
- structurally or operationally useful where possible

### Secondary priority

Second priority is given to candidates that:

- improve neutron-conscious handling
- support multifunctional wall behavior
- improve shelter packaging
- strengthen maintainability or segmentation
- contribute to the total architecture without overwhelming it

### Restricted priority

Lowest priority is given to candidates that:

- primarily win on density rather than architecture fit
- appear better suited to electronics shielding than crew shielding
- raise obvious secondary-radiation concerns
- require excessive justification to fit the baseline
- add mass without enough multifunctional value

## Evaluation dimensions

Each candidate or stack concept should be screened against the following
dimensions.

### 1. Threat relevance

Questions:

- Is the candidate mainly relevant to GCR mitigation, SPE / SEP sheltering, or
  both?
- Is the benefit likely broad or highly situational?
- Does the candidate help crew protection directly or mainly hardware
  protection?

### 2. Secondary-radiation penalty awareness

Questions:

- Is the candidate likely to create a penalty through secondaries?
- Is the penalty modest, severe, unknown, or strongly geometry dependent?
- Does the candidate worsen crew-wall suitability even if it helps locally in
  another context?

### 3. Areal-density efficiency

Questions:

- Does the candidate plausibly buy useful protection without excessive mass?
- Does it create a realistic path to concentration around a shelter?
- Does it encourage “mass everywhere” instead of “mass where it matters”?

### 4. Low-Z / hydrogen relevance

Questions:

- Is the candidate aligned with crew-wall low-Z logic?
- Does it contain meaningful hydrogen-bearing or equivalent favorable chemistry?
- If not, is the deviation justified by a restricted local use case?

### 5. Chamber compatibility

Questions:

- Can the candidate function naturally in segmented cells, liners, packs, or
  chambered modules?
- Does it support reconfigurable geometry?
- Does it resist becoming a monolithic non-serviceable slab?

### 6. Structural and multifunctional value

Questions:

- Can this candidate serve more than one mission function?
- Does it support habitat structure, packaging, shielding, or maintainability at
  once?
- Does it reduce parasitic mass or merely add to it?

### 7. Shelter compatibility

Questions:

- Is the candidate especially useful near the refuge volume?
- Can it be concentrated locally?
- Does it support acute-event logic better than general shell logic alone?

### 8. Crew-environment compatibility

Questions:

- Is the candidate compatible with crew habitability and interior use?
- Does it introduce contamination, brittleness, toxicity, awkward packaging, or
  maintenance issues?
- Can it be realistically placed near occupied volume?

### 9. Fault tolerance and serviceability

Questions:

- Does the candidate support segmentation, modular replacement, or graceful
  degradation?
- Does a local failure ruin the whole wall?
- Can the architecture continue to benefit from it after partial damage?

### 10. Integration burden

Questions:

- Does the candidate require extreme handling, thermal control, isolation, or
  support burden?
- Does it impose routing complexity or manufacturability penalties that weaken
  its practical value?
- Is it plausible for early concept screening or already burdened by obvious
  operational friction?

## Evaluation labels

Each candidate should be assigned the following labels where possible.

### Threat label

- GCR-oriented
- SPE / SEP-oriented
- mixed but bounded
- electronics-local
- not clearly relevant

### Architecture-fit label

- baseline-compatible
- comparison-only
- local-use-only
- deferred
- rejected

### Evidence label

- source-grounded
- modeled
- inferred
- speculative

A candidate with weak evidence can still be screened, but its label must be
honest.

## Screening matrix

Each candidate should be summarized in a matrix with the following fields:

- candidate name
- material class
- proposed role
- target threat
- low-Z / hydrogen relevance
- likely secondary-radiation posture
- chamber compatibility
- shelter compatibility
- structural usefulness
- serviceability
- habitability compatibility
- evidence level
- baseline recommendation
- major penalty
- major open question

This matrix is intended to keep the repository readable and prevent fuzzy
comparisons.

## Baseline candidate families for IX-Mirror

The following candidate families should be screened early as baseline contenders.

### Family 1 — Polyethylene / UHMWPE-class crew-wall systems

Reason for inclusion:

- strong alignment with low-Z / hydrogen-rich crew-wall logic
- credible role in liners, structural composites, and modular packs
- good fit with baseline architecture

### Family 2 — Water-dominant chambered systems

Reason for inclusion:

- strong fit with chambered and shelter-first design
- useful dual-role mission mass
- strong relevance to concentrated refuge logic

### Family 3 — Hydrogel or retained-water chamber systems

Reason for inclusion:

- likely improved containment behavior versus uncontrolled free fluid
- good chamber compatibility
- strong shelter relevance

### Family 4 — Boron-assisted low-Z support systems

Reason for inclusion:

- possible benefit in mixed-field handling
- strong fit as support layer rather than dominant wall class

### Family 5 — Multifunctional low-Z structural composites

Reason for inclusion:

- potential to reduce parasitic mass
- good fit with structure-plus-shielding philosophy
- likely strong architecture value if penalties are controlled

## Comparison candidate families

The following should be included for comparison even if they are unlikely to win
the baseline.

### Comparison Family A — Dense metallic foil stacks

Purpose:

- benchmark against naive “more metal must help” intuition
- test whether density-centric designs underperform once penalties and crew-wall
  logic are included

### Comparison Family B — High-Z local inserts

Purpose:

- retain value for electronics-local and hotspot-local logic
- prevent accidental overgeneralization from local-use success to crew-wall
  baseline use

### Comparison Family C — Speculative hybrid stacks

Purpose:

- explore whether a novel combined stack offers unusual value
- force speculative branches into structured comparison rather than hype

## Disqualification triggers

A material or stack should be rejected from baseline consideration if it does any
of the following:

- depends on unsupported acoustic, resonance, or generic charged-layer shielding
  claims
- is better suited to electronics-local shielding but is presented as a crew-wall
  default
- raises obvious secondary-radiation concerns without adequate offsetting value
- cannot be integrated into a chambered or shelter-first architecture
- creates major operational penalties with no strong architecture upside
- cannot be described clearly enough to model, compare, or falsify

## Scoring posture

This framework allows scoring, but IX-Mirror should avoid fake precision.

A simple tiered scoring system is preferred over a theatrical decimal ranking.

Recommended qualitative scale:

- **Strong**
- **Moderate**
- **Weak**
- **Unknown**
- **Disqualifying**

Each major dimension may be scored this way.

If a numerical rollup is ever used, the rollup must be secondary to the written
justification.

## Weighting logic

When a rollup is useful, IX-Mirror should weight categories approximately in the
following order:

1. crew threat relevance
2. shelter compatibility
3. low-Z / hydrogen-rich alignment
4. secondary-radiation penalty posture
5. chamber compatibility
6. multifunctional value
7. fault tolerance and serviceability
8. integration burden
9. habitability compatibility

This weighting reflects IX-Mirror’s priorities.

A candidate that scores beautifully on density but poorly on crew-wall logic
should still lose.

## Comparison examples

### Example 1 — Water chamber vs dense foil stack

A water chamber may win on:

- shelter concentration value
- crew-wall compatibility
- dual-use mission mass
- chamber fit

A dense foil stack may lose on:

- crew-wall logic
- likely penalties
- poor chamber flexibility
- poor multifunctional value

### Example 2 — UHMWPE liner vs tungsten liner

A UHMWPE liner may win on:

- crew-side low-Z logic
- habitability and interior compatibility
- baseline architecture fit

A tungsten liner may remain useful only for:

- narrow local hardware-protection cases
- specialty comparison studies

### Example 3 — Boron-assisted support layer vs pure dense sublayer

A boron-assisted support layer may win when:

- it supports low-Z logic
- it helps mixed-field handling without dominating mass
- it integrates cleanly with the rest of the stack

A dense sublayer may lose if:

- it adds mass without enough crew-side value
- it increases local penalties
- it is being used mainly because it sounds powerful

## Required outputs of a trade study

A completed IX-Mirror trade study should produce:

- a candidate matrix
- a retained-baseline set
- a comparison-only set
- a rejected set
- a short written rationale for each retained candidate
- a short written rejection reason for each rejected or demoted candidate
- explicit open questions for future modeling or source review

## Relationship to future modeling

This framework is intended to feed later modeling and benchmark work.

It should help define:

- which stacks deserve OLTARIS or transport-model screening
- which branches are worth geometry comparison
- which candidates belong in shelter-local studies
- which materials should be reserved for electronics-local studies only

The framework is therefore not the end of analysis. It is the gate that decides
what deserves deeper analysis.

## Non-claim rules for trade-study output

A winning trade-study candidate may be described as:

- retained baseline
- strongest current candidate
- best current fit for IX-Mirror architecture
- preferred branch for further modeling

A winning trade-study candidate may **not** be described as:

- proven best material
- final answer to space radiation
- validated astronaut shield
- mission-ready shielding solution

This rule remains in force even after comparison results exist.

## Final statement

IX-Mirror does not pick materials by intimidation, density, or novelty.

It picks them by whether they actually fit the crew-protection architecture the
repository is trying to build.
