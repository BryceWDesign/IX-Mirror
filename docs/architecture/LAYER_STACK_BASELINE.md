# Baseline Layer Stack

## Purpose

This document defines the baseline physical layer-stack logic for IX-Mirror.

It is not a manufacturing drawing, not a certified material schedule, and not a
flight-ready laminate recipe. Its purpose is to establish a disciplined
reference architecture for analysis, trade studies, and future model
comparison.

The stack defined here is intended to support the repository’s central design
posture:

- crew protection is threat-specific
- low-Z and hydrogen-rich logic should dominate crew-wall decisions
- geometry and mass placement matter alongside material choice
- selective local high-Z use may be valid, but it must not drive the baseline
  crew-wall architecture
- shielding performance must be interpreted together with structural,
  operational, and maintenance consequences

## Design intent

The baseline IX-Mirror stack is built around six functional zones arranged from
outside to inside:

1. outer survivability skin
2. structural support and integration layer
3. chambered shielding-media layer
4. neutron-conscious transition / support layer
5. crew-side attenuation liner
6. interior interface and habitability layer

These zones may map to more than six physical plies or sublayers in a future
design, but the functional order matters.

## Layer 1: Outer survivability skin

### Role

The outer survivability skin is the first external barrier.

Its purpose is to:

- provide a durable external surface
- support environmental exposure tolerance
- enable integration with vehicle or habitat structural packaging
- serve as the front mechanical boundary for the shielded wall assembly
- remain compatible with MMOD-aware and serviceable outer-shell strategies

### Desired properties

This layer should favor:

- structural plausibility
- abrasion and handling tolerance
- compatibility with bonded or mechanically attached inner assemblies
- manageable mass overhead
- clean interface behavior with the next layer

### Non-claim posture

This layer is not treated as the primary radiation shield. It may contribute to
total areal density, but IX-Mirror does not allow this layer alone to carry a
crew-protection claim.

## Layer 2: Structural support and integration layer

### Role

This layer binds the wall into the larger system.

Its purpose is to:

- carry structural loads associated with panel integration
- provide mounting and interface logic for chambered media modules
- support maintainability and modular replacement concepts
- reduce the temptation to treat shielding mass as structurally dead weight

### Desired properties

This layer should favor:

- multifunctionality
- compatibility with low-Z or hydrogen-rich system logic where practical
- mechanical robustness
- tolerance for localized penetrations, fittings, routing, and service points
- compatibility with segmented chambering behind or within it

### Rationale

A system that uses structure and shielding separately for no reason carries more
parasitic mass than one that extracts value from the same mass twice.

## Layer 3: Chambered shielding-media layer

### Role

This is the primary IX-Mirror shielding architecture zone.

Its purpose is to place useful shielding media in controllable geometry around
occupied space. This layer exists because IX-Mirror assumes that the same total
mass can produce different protection results depending on where and how it is
distributed.

### Candidate media classes

The baseline media classes for this layer are:

- water
- water-equivalent retained media
- hydrogel or gel-supported water systems
- hydrogen-rich polymers
- low-Z filler systems compatible with serviceable cell architecture
- mission-useful consumable mass where routing and safety allow

### Desired properties

This layer should favor:

- high usefulness per unit mass
- low-Z or hydrogen-rich composition
- chambering and segmentation
- puncture tolerance
- serviceability
- compatibility with nominal mode and shelter mode
- compatibility with crew-occupancy-informed mass concentration

### Why chambering matters

IX-Mirror does not assume one uniform wall thickness everywhere is the best use
of mass. Chambering allows:

- local concentration near shelter zones
- modularity
- fault isolation
- reconfiguration
- integration with already-carried mission mass
- design flexibility around occupied geometry

### Rejected alternative

The baseline stack rejects all-metal foil logic as the primary chamber content
for crew protection. Dense metallic stacks may be compared in trade studies, but
they are not the starting point for the main wall.

## Layer 4: Neutron-conscious transition / support layer

### Role

This layer exists to support the transition between upstream shielding media and
the crew-side boundary.

Its purpose is to strengthen the wall’s handling of mixed-field effects and to
support material strategies that are aware of secondary-particle consequences.

### Candidate direction

This layer may include:

- boron-aware chemistry
- BN / BNNT-related composite branches
- neutron-conscious polymer systems
- supporting transition materials that improve the total wall response without
  dominating the bulk architecture

### Desired properties

This layer should favor:

- compatibility with low-Z crew-wall logic
- multifunctional behavior where useful
- avoidance of gratuitous density
- compatibility with liners and inner structural packaging
- limited thickness relative to the chambered bulk layer

### Claim limit

This layer is not allowed to carry exaggerated “cleanup” language. It may be
modeled as a supporting contributor, not as a magic sublayer that neutralizes
all secondary radiation.

## Layer 5: Crew-side attenuation liner

### Role

This is the final crew-facing shielding layer before the interior interface.

Its purpose is to ensure that the last material the radiation field encounters
before occupied space remains aligned with crew-shielding logic.

### Candidate direction

This layer should prioritize:

- polyethylene-class logic
- UHMWPE or related hydrogen-rich polymers
- low-Z attenuation liners
- crew-compatible modular liners
- replaceable or inspectable interior shielding modules where useful

### Desired properties

This layer should favor:

- low-Z composition
- high hydrogen relevance
- interior compatibility
- low contamination burden
- maintainability
- modular installation or replacement where practical

### Why this layer matters

The crew-side boundary matters because a poor last layer can undercut the
benefit of upstream design choices. IX-Mirror therefore refuses to treat the
inner wall as a decorative trim layer.

## Layer 6: Interior interface and habitability layer

### Role

This is the interior-facing interface between the shielding assembly and the
crew environment.

Its purpose is to support:

- interior packaging
- cleanable and serviceable surfaces
- habitability integration
- softgoods, racks, or modular interior fittings
- the ability to shape a true shelter zone rather than a theoretical wall only

### Desired properties

This layer should favor:

- low operational friction
- compatibility with crew movement and ingress
- maintainability
- non-obstruction of shelter function
- compatibility with sensors, dosimeters, and interior-mounted modules

### Important distinction

This layer may contribute to the total protection system through what is mounted
to it or stored against it, but its primary role is not to compensate for poor
upstream material choices.

## Functional cross-section summary

From outside to inside, the baseline IX-Mirror cross-section follows this logic:

- protect the assembly mechanically
- make the wall structurally useful
- place most useful shielding mass in chambered low-Z form
- add neutron-conscious support where justified
- finish with a crew-side low-Z liner
- integrate with an operable interior shelter environment

That is the default order unless a comparison study defines a different stack
for explicit benchmarking.

## Baseline material direction

The baseline stack favors the following general direction:

### Preferred classes

- hydrogen-rich polymers
- water and retained-water media
- UHMWPE / HDPE / polyethylene-family candidates
- multifunctional composites that do not betray crew-shielding logic
- boron-aware support chemistries where justified

### Restricted-use classes

- tungsten
- lead
- dense generic metal foils
- high-Z dominated stacks
- decorative conductor stacks marketed as “field” layers

These are not prohibited from existence in the repository, but they require
explicit justification and should default to local-use comparisons, not baseline
crew-wall placement.

## Why lead and tungsten are not baseline

Dense materials can look intuitively protective because they stop many familiar
forms of radiation well in terrestrial settings.

IX-Mirror treats that intuition as incomplete for crew deep-space shielding.

The repository assumes from the start that:

- density alone is not the right optimization metric
- secondary-radiation penalties matter
- crew-wall logic is not identical to electronics-vault logic
- a heavier layer is not automatically a safer crew layer
- local high-Z use may still have value when narrowly targeted

Therefore, dense high-Z material is not the baseline answer.

## Wall-thickness posture

This document intentionally does not assign a single fixed thickness.

Areal density and thickness must later be expressed together with:

- mission context
- material composition
- crew geometry
- shelter geometry
- whether the wall is baseline habitat wall or concentrated shelter wall
- whether the configuration is nominal or event-driven

IX-Mirror rejects single-number thickness theater.

## Nominal mode versus shelter mode

The baseline stack must be understood in two configurations.

### Nominal mode

In nominal mode, the wall distributes shielding and useful mass in a way that
supports ordinary habitation, system integration, and chronic exposure
management.

### Shelter mode

In shelter mode, the architecture is allowed to concentrate additional useful
mass around a designated refuge volume. This can change the effective protection
without requiring the entire vehicle shell to become uniformly heavier.

The same physical wall family may therefore serve both a general protective role
and an event-focused shelter role.

## Local specialty inserts

The baseline stack allows local specialty inserts only under controlled rules.

Examples of acceptable local specialty use include:

- electronics-vault shielding
- detector or instrument-local protection
- narrow graded-Z comparison branches
- test coupons included only for benchmark contrast

These inserts must remain explicitly local. They must not silently become the
crew-wall default.

## Failure-aware design logic

The layer stack should still produce useful passive benefit if active
reconfiguration is unavailable.

Therefore the baseline stack should favor:

- passive usefulness in default configuration
- segmented cells over single continuous vulnerable volume
- limited dependence on one actuator path
- graceful degradation
- inspectable interfaces
- realistic maintenance logic

## Comparison branches allowed by this stack

The baseline stack is intended to support later comparison branches such as:

- all-polymer low-Z wall
- water-dominant chambered wall
- hydrogel-retained chamber system
- boron-enhanced chambered wall
- hybrid crew-wall with local electronics shielding islands
- shelter-thickened wall branch
- future active-magnetic-compatible habitat branch

The value of the baseline stack is that all of those branches can be compared
against a common architectural frame.

## What this document does not claim

This document does not claim:

- an optimal final material recipe
- a validated layup schedule
- a flight-ready stack
- a solved GCR problem
- a universal wall thickness
- a complete MMOD solution
- a complete thermal-control solution

It defines a disciplined starting stack, nothing more.

## Final statement

The IX-Mirror baseline wall is not a metal fortress.

It is a layered, low-Z-biased, chamber-centered protection system built to make
useful mass work where crew survival actually depends on it.
