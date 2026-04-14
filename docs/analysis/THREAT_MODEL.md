# Threat Model

## Purpose

This document defines the radiation threat model used by IX-Mirror.

It exists to prevent scope drift, material-selection mistakes, and false claims.
The repository should not discuss “space radiation” as though it were one
uniform problem. Different sources, particle populations, energies, time scales,
and operational consequences require different responses.

IX-Mirror uses a **threat-matched** model.

## Primary threats

IX-Mirror centers on two primary crew-radiation threats:

1. **Galactic Cosmic Rays (GCR)**
2. **Solar Particle Events / Solar Energetic Particles (SPE / SEP)**

These are treated as distinct hazards rather than interchangeable labels.

## Secondary / contextual threat classes

The following are relevant context but are not the primary design driver for the
baseline architecture:

- trapped radiation belts
- mission-phase transitions through trapped regions
- secondary radiation generated inside shielding
- local electronics upsets and subsystem vulnerability
- mission-duration accumulation effects
- mixed-field exposure inside habitats and vehicles

## Threat 1: Galactic Cosmic Rays (GCR)

### What GCR means in this repository

GCR refers to the chronic deep-space background of high-energy charged particles
originating outside the solar system.

For IX-Mirror, GCR is treated as the **hard problem**.

### Why GCR matters

GCR is difficult because:

- particles are highly energetic
- shielding benefit is limited compared with intuition
- incoming ions can generate secondary radiation in shielding and tissue
- mass penalties rise quickly
- design choices that help against one component may worsen another
- the mission is exposed for long durations rather than short bursts

### Architectural consequence

IX-Mirror does **not** assume that passive mass alone will “solve” GCR.

Instead, the repository treats GCR mitigation as a combination of:

- partial passive reduction
- weak-point elimination
- occupied-volume optimization
- localized material selection
- operational dose awareness
- architecture that remains compatible with future active augmentation

### Design posture for GCR

For GCR, the project should prioritize:

- honest non-claims
- hydrogen-rich and low-Z logic where justified
- careful treatment of secondaries
- realistic geometry and areal-density discussion
- protection of most-occupied volumes
- separation between crew-wall logic and electronics-vault logic

## Threat 2: Solar Particle Events / Solar Energetic Particles (SPE / SEP)

### What SPE / SEP means in this repository

SPE / SEP refers to acute solar radiation events that can rapidly elevate crew
exposure during transit or surface operations.

For IX-Mirror, SPE / SEP is treated as the **actionable protection problem**.

### Why SPE / SEP matters

SPE / SEP matters because:

- exposure can rise quickly
- event warning and event response affect outcome
- sheltering can materially reduce risk
- reconfigurable mass placement can matter
- operational procedures can buy real safety margin
- a system can be designed to become stronger during an event

### Architectural consequence

IX-Mirror assumes that real crew-risk reduction is most likely to be achieved
first against SPE / SEP through:

- storm-shelter concentration
- chambered shielding walls
- consumables-aware mass routing
- occupancy-aware safe-mode logic
- dosimetry-driven event response
- disciplined ingress / egress procedures

### Design posture for SPE / SEP

For SPE / SEP, the project should prioritize:

- fast shelter access
- useful mass near crew occupancy
- practical reconfiguration paths
- robust event detection and decision logic
- low-friction emergency operation
- compatibility with habitat and life-support constraints

## Why GCR and SPE / SEP are separated

A recurring failure mode in radiation-concept work is pretending that one design
choice helps all threats equally.

IX-Mirror rejects that approach.

The repository assumes from the start that:

- a concept may help strongly against SPE / SEP and only weakly against GCR
- a concept may help electronics more than crew
- a concept may help a shelter core more than a full vehicle shell
- a concept may introduce a penalty through secondaries
- a concept may be operationally valuable even if material benefit is modest

This separation is mandatory for honest analysis.

## Threat-to-response map

### GCR
Expected best response class in IX-Mirror:
- partial passive mitigation
- geometry optimization
- hydrogen-rich materials where justified
- weak-point control
- long-duration dose awareness
- possible future magnetic augmentation branch

### SPE / SEP
Expected best response class in IX-Mirror:
- storm shelter
- fast reconfiguration
- local mass concentration
- chambered walls
- event warning and response
- dosimetry-linked operations

### Trapped radiation
Expected response class:
- mission planning
- trajectory / time-in-region awareness
- subsystem hardening
- local shielding logic
- phase-specific operational constraints

### Secondary radiation
Expected response class:
- material selection discipline
- low-Z bias for crew shielding
- selective use of graded-Z rather than blanket heavy metal
- explicit analysis of penalty terms

## Crew-protection objective hierarchy

IX-Mirror uses the following protection hierarchy:

1. prevent avoidable acute exposure during SPE / SEP
2. reduce chronic mission exposure where practical
3. eliminate preventable architectural weak points
4. avoid making things worse through poor material intuition
5. keep the system testable, auditable, and operable under mission constraints

## What is being protected

The baseline concern is **human crew**, not only vehicle hardware.

That means the threat model must account for:

- occupied volume
- crew posture and dwell time
- sleep location
- work location
- shelter ingress time
- medical contingency burden
- habitability penalties introduced by shielding mass and layout

Electronics and avionics protection matter, but they are not allowed to replace
crew-centered design logic.

## Mission contexts assumed by default

Unless a document states otherwise, IX-Mirror assumes the following mission
contexts are relevant:

- cis-lunar transit
- deep-space transit
- Mars-class transit
- long-duration crew habitation outside low Earth orbit
- exposure environments where atmospheric and geomagnetic protection are absent
  or strongly reduced

## Exposure logic

IX-Mirror treats risk as a product of more than just “how much material exists.”

The project assumes exposure outcome depends on:

- particle environment
- mission phase
- areal density
- material composition
- geometry
- crew position
- time
- event timing
- secondaries
- operational response

Therefore, any design that only states thickness without addressing geometry,
occupancy, or event response is incomplete.

## Rejected simplifications

The following simplifications are rejected for this repository:

- “more metal is always better”
- “any shielding layer helps all radiation equally”
- “one wall thickness is enough to describe crew protection”
- “crew protection and electronics protection are the same problem”
- “modeled reduction equals solved risk”
- “vibration or generic frequency effects count as shielding without evidence”
- “an eye-catching structure is evidence of performance”

## Threat model implications for materials

This threat model pushes IX-Mirror toward:

- hydrogen-rich materials
- low-Z crew-wall bias
- boron-assisted or related neutron-conscious approaches where justified
- multifunctional materials that provide shielding plus useful structural or
  operational value
- limited and intentional use of high-Z materials for local cases rather than as
  crew-wall default

## Threat model implications for architecture

This threat model pushes IX-Mirror toward:

- chambered wall systems
- reconfigurable shielding mass
- shelter-first interior planning
- distributed dosimetry
- fault-tolerant operations
- subsystem integration with consumables and logistics
- compatibility with future active-magnetic concepts without depending on them

## Analysis labels used in this repository

To keep claims clean, IX-Mirror should label statements using one of the
following tags where appropriate:

- **Observed** — directly measured in referenced work or future IX-Mirror tests
- **Modeled** — produced by transport or geometry models
- **Inferred** — reasoned from accepted physical behavior but not yet directly
  tested in the repository
- **Speculative** — concept branch not yet supported enough for design-level
  confidence

## Early screening rule

A concept survives early screening only if it answers all of the following:

1. Which threat does it target: GCR, SPE / SEP, both, or neither?
2. Is the claimed effect material, geometric, operational, or control-based?
3. Does it help crew, electronics, or both?
4. What penalty does it introduce?
5. Could it generate harmful secondaries or mass penalties?
6. What would falsify the claim?

If those questions cannot be answered, the concept is not mature enough for
serious inclusion.

## Final statement

IX-Mirror does not treat GCR and SPE / SEP as one problem.

It treats them as two different enemies that require different layers of
defense.
