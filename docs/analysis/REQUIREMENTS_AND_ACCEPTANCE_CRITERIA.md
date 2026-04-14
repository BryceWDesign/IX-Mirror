# Requirements and Acceptance Criteria

## Purpose

This document defines the baseline requirements posture for IX-Mirror.

The goal is not to pretend the repository is a certified aerospace program. The
goal is to force each concept branch to answer the same disciplined questions so
weak ideas can be screened out early and stronger ideas can be compared on the
same frame.

These requirements are written for an analysis-stage, documentation-first
architecture repository focused on astronaut protection from:

- galactic cosmic rays (GCR)
- solar particle events / solar energetic particles (SPE / SEP)

## Requirement philosophy

IX-Mirror requirements are intentionally structured around four realities:

1. crew protection is the primary mission driver
2. acute-event protection and chronic-exposure mitigation are not the same task
3. architecture quality matters alongside material choice
4. a concept that cannot be tested, screened, or falsified is not mature enough

The requirements below define what a retained IX-Mirror concept must do, or at
minimum what it must credibly support.

## Requirement classes

IX-Mirror uses five requirement classes:

- mission relevance requirements
- architecture requirements
- materials and geometry requirements
- operations and control requirements
- verification and governance requirements

A concept that fails any critical requirement may still be documented as a
rejected branch, but it should not be treated as part of the retained baseline.

## MR-01 — Threat specificity

Every IX-Mirror concept shall state whether it is intended to address:

- GCR
- SPE / SEP
- both, with differentiated logic
- or neither

### Acceptance criteria

Accepted if the concept documentation explicitly names the target threat class
and does not blur GCR and SPE / SEP into one generic “radiation” claim.

Rejected if the concept uses broad protection wording without threat mapping.

## MR-02 — Crew-centered framing

Every retained baseline concept shall identify whether the claimed benefit is for:

- crew protection
- electronics protection
- both, with separate logic

### Acceptance criteria

Accepted if the concept clearly distinguishes crew shielding from hardware-local
shielding.

Rejected if electronics-local logic is silently presented as crew-protection
logic.

## MR-03 — Actionable acute-event relevance

The architecture baseline shall include at least one credible pathway for
materially improving crew posture during SPE / SEP conditions.

### Acceptance criteria

Accepted if the design contains a defined shelter, concentrated refuge logic, or
another bounded acute-event protection mechanism that is stronger than general
nominal occupancy protection.

Rejected if the architecture has no distinct acute-event behavior.

## MR-04 — Honest GCR posture

No retained baseline concept shall rely on a claim that passive material alone
fully resolves GCR risk.

### Acceptance criteria

Accepted if GCR language is bounded to terms such as partial mitigation, chronic
dose reduction candidate, weak-point reduction, or compatible-with-future
augmentation.

Rejected if the concept promises comprehensive GCR protection without evidence
commensurate to that claim.

## AR-01 — Layered architecture

The baseline IX-Mirror concept shall include more than one protection mechanism
class.

At minimum, the architecture shall include:

- a passive material and geometry component
- an acute-event shelter or concentration component
- an observability or operations component

### Acceptance criteria

Accepted if the architecture documentation shows these classes explicitly.

Rejected if the concept is just one material, one wall, or one unsupported field
idea.

## AR-02 — Chambered or geometry-aware mass logic

The retained baseline architecture shall explicitly account for how shielding
mass is distributed in space, not only how much of it exists.

### Acceptance criteria

Accepted if chambering, local concentration, refuge geometry, occupied-volume
awareness, or equivalent geometry logic is present.

Rejected if the architecture only states thickness or material name without
spatial logic.

## AR-03 — Shelter-first integration

The retained baseline architecture shall include a designated refuge concept that
is integrated into the larger vehicle or habitat architecture.

### Acceptance criteria

Accepted if a refuge volume, ingress logic, and local concentration strategy are
documented.

Rejected if the shelter is absent, undefined, or described as an afterthought.

## AR-04 — Graceful degradation

The architecture shall preserve some protective value under partial subsystem
failure.

### Acceptance criteria

Accepted if the design documentation identifies passive baseline benefit,
segmentation, degraded-mode use, or other means of avoiding total reliance on
one active pathway.

Rejected if failure of a single routing, sensing, or actuation element causes
the concept to lose all meaningful value.

## AR-05 — No unsupported physics dependency

No retained baseline concept shall depend on unsupported acoustic, resonance,
scalar, or generic “charged frequency” shielding claims.

### Acceptance criteria

Accepted if any such earlier ideas are either excluded, demoted to rejected
branches, or repurposed into support roles such as sensing and control.

Rejected if the architecture’s protective claim depends on those mechanisms.

## MG-01 — Low-Z / hydrogen-rich crew-wall bias

The baseline crew-wall architecture shall prioritize low-Z and hydrogen-rich
material logic unless a comparison study explicitly justifies an exception.

### Acceptance criteria

Accepted if the baseline layer stack favors water, water-equivalent media,
polyethylene-family materials, UHMWPE-class systems, hydrogels, or related
low-Z/hydrogen-rich candidates.

Rejected if dense high-Z materials dominate the baseline crew-wall stack without
a threat-specific and penalty-aware rationale.

## MG-02 — Restricted high-Z use

High-Z materials may appear only as local, comparison, or specialty elements
unless a future evidence package justifies broader use.

### Acceptance criteria

Accepted if dense materials are confined to electronics-local shielding,
comparison branches, or narrow graded-use cases.

Rejected if tungsten-, lead-, or similar high-Z-heavy layers silently become the
default crew-wall answer.

## MG-03 — Secondary-radiation awareness

Every retained materials branch shall explicitly identify whether secondary
radiation is a potential penalty.

### Acceptance criteria

Accepted if the documentation includes secondaries as a screening factor or
tradeoff term.

Rejected if material comparisons discuss only stopping power, density, or
thickness without any penalty awareness.

## MG-04 — Interior-facing low-Z logic

The crew-side boundary of the retained baseline wall shall preserve low-Z logic.

### Acceptance criteria

Accepted if the design includes a crew-side attenuation liner or equivalent
crew-facing low-Z boundary.

Rejected if the final crew-facing layer defaults to dense high-Z material
without strong justification.

## MG-05 — Reconfigurable or strategically placeable useful mass

The architecture should support use of already-carried mission mass where that
improves shelter geometry and does not compromise safety.

### Acceptance criteria

Accepted if the design supports use of water, retained-water systems, softgoods,
food, packaging, or other useful mass classes in intentional shelter logic.

Rejected if “useful mass” is invoked only rhetorically without any placement or
access logic.

## OC-01 — Event-state logic

The baseline architecture shall define at least two operational states:

- nominal mode
- shelter mode

### Acceptance criteria

Accepted if the documentation defines what changes between those states.

Rejected if the concept contains no stateful operational distinction.

## OC-02 — Ingress clarity

The shelter concept shall include a clear ingress logic suitable for acute-event
use.

### Acceptance criteria

Accepted if likely crew travel path, accessibility, and emergency-entry logic are
addressed at concept level.

Rejected if the refuge is theoretically strong but operationally ambiguous or
difficult to reach.

## OC-03 — Observability

The architecture shall include a concept-level strategy for knowing what state
the protection system is actually in.

### Acceptance criteria

Accepted if the design includes dosimetry, chamber-state awareness, route-state
awareness, occupancy confirmation, fault indications, or equivalent observability
logic.

Rejected if the architecture depends on reconfiguration without any credible way
to know whether it occurred.

## OC-04 — Control logic boundaries

The observability and control layer may improve response but shall not be framed
as a substitute for shielding mass and geometry.

### Acceptance criteria

Accepted if sensing and control are described as enabling layers.

Rejected if the concept claims that monitoring or logic alone provides
protection.

## OC-05 — Partial-failure operation

The control concept shall define what happens if reconfiguration only partially
succeeds.

### Acceptance criteria

Accepted if fallback behavior, degraded shelter use, or partial-state handling is
documented.

Rejected if the architecture assumes perfect actuation and perfect state
knowledge in all cases.

## VG-01 — Evidence label discipline

Performance-affecting statements shall be labeled or framed in a way that makes
their evidence level clear.

### Acceptance criteria

Accepted if statements are clearly presented as observed, modeled, inferred, or
speculative where appropriate.

Rejected if performance language drifts into proof claims without evidence labels
or equivalent bounding language.

## VG-02 — Falsifiability

Every retained subsystem concept shall identify at least one way it could be
shown inadequate.

### Acceptance criteria

Accepted if the documentation states at least one failure condition, rejection
condition, or disqualifying benchmark.

Rejected if the concept is written so vaguely that no failure condition can be
identified.

## VG-03 — Comparison readiness

Any baseline or retained branch shall be documentable in a way that supports
future comparison through transport modeling, geometry comparison, or structured
review.

### Acceptance criteria

Accepted if the branch can be expressed with a defined material class, geometry
logic, occupancy logic, and claim boundary.

Rejected if the concept is too vague to benchmark.

## VG-04 — Source and interpretation separation

External findings, patents, references, and public prior art shall be separated
from IX-Mirror’s own interpretation.

### Acceptance criteria

Accepted if the repository distinguishes source-grounded statements from inferred
design conclusions.

Rejected if source citations are used to smuggle in conclusions they do not
actually state.

## VG-05 — Non-claim preservation

Any retained baseline file shall remain compatible with the repository-wide
non-claim posture.

### Acceptance criteria

Accepted if a file does not imply:

- flight qualification
- medical efficacy
- full GCR resolution
- comprehensive astronaut safety
- proven mission readiness

Rejected if any of those implications appear without evidence that would support
them.

## Baseline acceptance gate

A concept branch may be called **retained baseline** only if it satisfies all of
the following:

- MR-01
- MR-02
- MR-03
- MR-04
- AR-01
- AR-02
- AR-03
- AR-04
- AR-05
- MG-01
- MG-02
- MG-03
- MG-04
- OC-01
- OC-02
- OC-03
- VG-01
- VG-02
- VG-05

A branch may remain in the repository as a comparison or rejected branch even if
it fails this gate, but it may not be presented as the baseline architecture.

## Desired but non-gating qualities

The following qualities are strongly preferred but not absolute baseline gates at
this stage:

- MG-05
- OC-04
- OC-05
- VG-03
- VG-04

These may mature later as the repository becomes more detailed.

## Evaluation checklist

A reviewer can use the following quick screening checklist.

### Threat and mission relevance

- Does the concept name its target threat?
- Does it separate crew protection from electronics protection?
- Does it provide an acute-event protection pathway?

### Architecture quality

- Is there a layered architecture rather than a single magic answer?
- Does geometry or chambering matter in the concept?
- Is there a real shelter concept?
- Does some value remain under partial failure?
- Is unsupported physics removed from the main claim?

### Material and geometry quality

- Is the crew-wall baseline low-Z / hydrogen-rich?
- Are high-Z materials controlled rather than dominant?
- Are secondary-radiation penalties acknowledged?
- Is the crew-facing boundary aligned with low-Z logic?

### Operations and control quality

- Are nominal mode and shelter mode both defined?
- Can the crew realistically reach the refuge?
- Can the system know what state it is in?
- Is there degraded behavior if reconfiguration is imperfect?

### Governance quality

- Are claims bounded?
- Could the concept be falsified?
- Is the file compatible with the repo’s non-claim posture?

## Rejection triggers

A concept should be rejected from baseline consideration immediately if it does
any of the following:

- treats GCR and SPE / SEP as one undifferentiated problem
- promises full passive GCR protection
- makes crew-protection claims from electronics-only evidence
- relies on unsupported acoustic or resonance shielding
- uses dense high-Z material as default crew-wall logic without penalty analysis
- lacks a shelter
- lacks a plausible operational mode distinction
- cannot define how it would be benchmarked or falsified

## Final statement

IX-Mirror requirements exist to force discipline before the repository earns the
right to make stronger claims.

A concept that cannot survive these requirements should not survive in the
baseline.
