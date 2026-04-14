# Claim Boundaries

## Purpose

This document defines the allowed and disallowed claim posture for IX-Mirror.

Its job is simple: prevent the repository from sounding more proven than it is.

IX-Mirror is intentionally ambitious, but it is not allowed to overstate its
technical status, its evidence level, or its safety implications. Every concept
in the repository must stay inside an explicit claim boundary.

## Core rule

No statement in IX-Mirror may imply a higher level of evidence than the concept,
model, source material, or test record actually supports.

If a statement would make a technically serious reader believe that a concept is
validated, flight-ready, crew-rated, medically proven, or broadly effective
against deep-space radiation when that has not been demonstrated, the statement
must be removed or rewritten.

## Allowed statement classes

IX-Mirror may use the following statement classes.

### 1. Framing statements

These describe why the problem matters or why a design question exists.

Examples:

- crew radiation protection is a systems problem
- GCR and SPE / SEP must not be treated as identical threats
- storm-shelter geometry can matter as much as material choice
- multifunctional shielding may reduce parasitic mass

These are allowed when they remain general, careful, and technically grounded.

### 2. Source-grounded statements

These summarize or restate what an external source reports.

Examples:

- a cited source reports a modeled reduction under defined conditions
- a cited source identifies hydrogen-rich materials as favorable in a given
  context
- a public patent describes a chambered or graded architecture
- a standard toolkit is commonly used for radiation transport modeling

These are allowed only when they remain faithful to the source and do not import
extra certainty.

### 3. Repository design statements

These describe what IX-Mirror is choosing to evaluate.

Examples:

- IX-Mirror prioritizes low-Z crew-wall logic
- IX-Mirror treats storm shelters as first-class architecture elements
- IX-Mirror evaluates chambered wall concepts
- IX-Mirror separates crew shielding from electronics shielding

These are allowed because they describe repository intent, not performance.

### 4. Labeled inference statements

These are reasoned engineering conclusions that are not directly measured inside
the repository.

Examples:

- a given architecture is expected to help more against SPE / SEP than GCR
- a heavy-metal-dominant crew wall likely introduces secondary-radiation risk
- a reconfigurable mass-routing concept may improve temporary shelter geometry

These are allowed only when they are clearly labeled as inferred, not observed
or validated.

### 5. Speculative branch statements

These document exploratory branches without pretending they are design-level
truth.

Examples:

- future magnetic augmentation may be worth evaluating
- a multifunctional wall may support both structural and shielding functions
- a novel chamber geometry may deserve transport-model screening

These are allowed only when the speculative status is explicit.

## Required evidence labels

Concept statements should use the following labels when appropriate:

- **Observed**
- **Modeled**
- **Inferred**
- **Speculative**

These labels are not decoration. They are claim-control devices.

Any section discussing performance, reduction, effectiveness, survivability, or
benefit should use one of these labels if the evidence level is not already
obvious.

## Disallowed claims

The following claim classes are prohibited unless future evidence fully justifies
them.

### 1. Full-solution claims

Prohibited examples:

- IX-Mirror solves space radiation
- IX-Mirror makes astronauts safe from GCR
- IX-Mirror eliminates deep-space radiation risk
- IX-Mirror provides comprehensive crew protection against all mission exposure

Reason:
These statements collapse a multi-domain, unsolved problem into an unsupported
promise.

### 2. Flight-readiness claims

Prohibited examples:

- flight-ready
- mission-ready
- operationally deployable
- crew-rated
- certifiable as presented
- aerospace-qualified as presented

Reason:
The repository is concept-stage and analysis-stage, not certification-stage.

### 3. Medical efficacy claims

Prohibited examples:

- prevents cancer
- prevents radiation sickness
- medically protects astronauts
- guarantees safe exposure

Reason:
Those are medical and human-outcome claims beyond repository scope.

### 4. Unsupported active-field claims

Prohibited examples:

- acoustic fields block GCR
- low-frequency resonance deflects SEP
- generic charged-frequency walls repel radiation
- vibrational shielding protects crew from ionizing space radiation

Reason:
These mechanisms are not established by the repository and must not be implied.

### 5. Material absolutism

Prohibited examples:

- this material is the best, period
- this stack is the answer
- tungsten walls protect crew better than low-Z systems
- more thickness always means better shielding

Reason:
Space-radiation response is threat-specific, geometry-dependent, and secondary-
dependent.

### 6. Simulation inflation

Prohibited examples:

- the model proves the design works
- transport output validates the concept
- benchmark agreement confirms operational effectiveness
- a single run demonstrates crew safety

Reason:
Modeling supports screening and comparison. It does not replace validation.

### 7. Patent laundering

Prohibited examples:

- patented means validated
- patented means effective
- public patent = engineering proof
- prior art confirms mission readiness

Reason:
Patents show disclosed concepts, not performance proof.

## Required wording discipline

The repository should prefer wording like:

- is being evaluated
- is intended to examine
- may help
- is expected to be more useful for
- is screened as a candidate
- is modeled under specific assumptions
- is included as a concept branch
- does not yet establish
- remains unvalidated in this repository

The repository should avoid wording like:

- proves
- guarantees
- solves
- fully protects
- definitively prevents
- operationalizes today
- closes the problem
- is mission-ready

## Threat-specific claim rules

### GCR claim rule

Any claim about GCR must be conservative by default.

Allowed examples:

- partial mitigation
- chronic dose reduction candidate
- geometry-sensitive improvement
- compatibility with future augmentation
- weak-point reduction

Disallowed examples:

- full GCR shield
- robust GCR immunity
- complete GCR deflection
- practical total GCR protection using passive mass alone

### SPE / SEP claim rule

SPE / SEP claims may be stronger than GCR claims, but only when they remain
clearly bounded.

Allowed examples:

- storm-shelter architecture may materially improve acute-event protection
- local mass concentration is expected to help during SPE / SEP
- event-driven reconfiguration is a plausible risk-reduction strategy

Disallowed examples:

- guaranteed SPE survival
- universal event protection
- no-risk solar event operations

## Architecture claim rules

### Chambered walls

Allowed:
- may improve mass distribution flexibility
- may support reconfigurable shelter logic
- may integrate shielding with consumables

Disallowed:
- inherently superior in all missions
- proven best architecture
- intrinsically radiation-deflecting by geometry alone

### Hydrogen-rich materials

Allowed:
- are prioritized for screening in crew shielding
- are consistent with low-Z shielding logic
- may offer better crew-wall tradeoffs than heavy-metal dominance

Disallowed:
- completely solve mixed-field exposure
- negate all secondary radiation
- guarantee acceptable deep-space lifetime exposure

### Heavy-metal or graded-Z sublayers

Allowed:
- may be useful for local electronics or selected subproblems
- require careful penalty analysis for crew shielding

Disallowed:
- should dominate crew-wall architecture by default
- are automatically better because they are denser

### Dosimetry and control logic

Allowed:
- may improve operational response
- may reduce avoidable acute exposure through earlier shelter action
- may strengthen observability and fault response

Disallowed:
- replaces shielding
- substitutes for habitat design
- guarantees protection without adequate mass and geometry

## Figure and diagram rule

A figure may illustrate:

- architecture layout
- subsystem relationships
- concept branches
- material stack logic
- operational flow
- threat mapping

A figure may not imply:

- validated performance
- certified field behavior
- measured protection unless that measurement is explicitly shown and sourced
- realistic engineering maturity unless the maturity level is labeled

## Naming rule

The repository name **IX-Mirror** is allowed as a project identity.

The name may not be used to imply literal mirror-like reflection of space
radiation unless a specific mechanism is demonstrated.

Therefore, phrasing such as "radiation mirror" or "reflective radiation wall"
should be avoided unless explicitly scoped as metaphor or rejected concept
history.

## Benchmark and test rule

A benchmark, simulation, or model comparison may support statements such as:

- under the stated assumptions, concept A outperformed concept B
- the model suggests a tradeoff between areal density and flexibility
- the candidate remains viable for additional study

A benchmark, simulation, or model comparison may not support statements such as:

- the concept is validated for crewed mission deployment
- the design has been proven safe
- the architecture is now established as the best available

## External-source integration rule

When external sources are included:

- quote narrowly
- paraphrase honestly
- preserve source context
- separate source facts from repository interpretation
- state when a conclusion is an inference rather than source language

IX-Mirror must not smuggle extra claims into an external citation.

## Commit and review rule

A maintainer should reject or revise any commit that:

- upgrades a concept from inferred to observed without evidence
- blurs GCR and SPE / SEP into one claim
- turns a trade-study result into a solution claim
- treats visualization as validation
- uses dramatic wording to hide uncertainty
- frames low-confidence ideas as baseline architecture truth

## Final rule

IX-Mirror is allowed to argue for a design direction.

It is not allowed to pretend the argument is already proven.
