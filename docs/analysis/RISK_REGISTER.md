# Risk Register

## Purpose

This document records the major risks currently visible in IX-Mirror.

It exists for one reason: a serious crew-protection repository should not wait
until late-stage modeling or late-stage hardware work to admit what can go
wrong. IX-Mirror is a concept-stage and analysis-stage project, but it still
needs a disciplined map of failure pressure.

This register is not a theatrical hazard list. It is a screening tool used to:

- expose where the architecture is vulnerable
- prevent false confidence
- guide what deserves modeling first
- guide what deserves rejection early
- preserve honest claim boundaries

## Risk posture

IX-Mirror treats risk in five broad categories:

1. radiation-physics risks
2. materials and stack risks
3. architecture and geometry risks
4. operations and control risks
5. program and evidence-discipline risks

Each risk entry includes:

- a risk identifier
- a short title
- the affected subsystem or design area
- why the risk matters
- likely consequence if ignored
- preferred treatment path
- current posture

## Status labels

The following status labels are used in this register:

- **Open** — the risk is active and not yet meaningfully reduced
- **Tracked** — the risk is understood and tied to a defined analysis path
- **Partially Mitigated** — some containment exists, but not enough to close it
- **Deferred** — known but intentionally postponed with documented reason
- **Rejected by Design** — contained by baseline design rule or scope rule

These labels describe repository posture, not final aerospace certification.

## Treatment labels

IX-Mirror uses the following treatment paths:

- **Design Rule** — controlled through architecture or governance rule
- **Trade Study** — controlled through candidate comparison
- **Modeling** — controlled through transport or geometry analysis
- **Controls Review** — controlled through state and operations review
- **Future Test** — reserved for later bench or physical checking
- **Scope Rejection** — removed from baseline architecture

## Risk matrix summary

At current stage, the highest-priority risk cluster is:

- overclaiming GCR benefit
- choosing poor crew-wall materials due to density intuition
- misusing local high-Z logic as a global shielding answer
- building shelter logic that is too operationally slow or vague
- trusting active reconfiguration too much without degraded-mode value

Those are the risks most likely to make the repository look stronger than it is.

---

## R-01 — False confidence from “more mass everywhere” intuition

**Category:** radiation-physics / architecture  
**Affected area:** wall-stack selection, general shielding philosophy  
**Status:** Tracked  
**Treatment:** Design Rule + Trade Study + Modeling

### Why this matters

A common intuitive mistake is assuming that simply adding more dense material
everywhere around the crew automatically produces a better radiation outcome.

### Consequence if ignored

- poor crew-wall material choices
- inflated mass without proportional safety value
- possible increase in secondary-radiation penalties
- confusion between “heavier” and “better”

### IX-Mirror response

The baseline architecture rejects density-only reasoning. Comparison branches may
still include dense stacks, but only as controlled trade-study or negative-
control branches.

---

## R-02 — Overstating GCR protection

**Category:** radiation-physics / claim discipline  
**Affected area:** repository-wide language, baseline architecture claims  
**Status:** Tracked  
**Treatment:** Design Rule + Modeling

### Why this matters

GCR is the hardest threat in the repository. It is easy to drift from “partial
mitigation candidate” into “crew-protection solution” language.

### Consequence if ignored

- false repository posture
- loss of technical credibility
- claim inflation disconnected from evidence
- confusion between acute-event benefit and chronic-risk closure

### IX-Mirror response

All GCR statements must remain bounded. The baseline architecture may discuss
partial mitigation, weak-point reduction, shelter-local benefit, or future
active augmentation compatibility, but not full GCR resolution.

---

## R-03 — Misusing high-Z materials as a crew-wall default

**Category:** materials and stack  
**Affected area:** baseline layer stack, wall-material selection  
**Status:** Tracked  
**Treatment:** Design Rule + Trade Study + Modeling

### Why this matters

Dense materials such as tungsten or lead can feel intuitively protective and may
have narrow local value, but they are not automatically suitable for broad crew-
wall use.

### Consequence if ignored

- local success in hardware shielding gets overgeneralized
- crew-wall logic drifts away from low-Z / hydrogen-rich priorities
- possible worsening of mixed-field penalty behavior
- mass burden rises rapidly

### IX-Mirror response

High-Z materials remain restricted to local-use or comparison-only roles unless
later analysis provides a very narrow justified exception.

---

## R-04 — Secondary-radiation penalties hidden by simplified writeups

**Category:** radiation-physics / materials  
**Affected area:** trade studies, material summaries, stack comparisons  
**Status:** Open  
**Treatment:** Trade Study + Modeling

### Why this matters

A material can look favorable if described only by density, stopping intuition,
or one narrow exposure context while its secondary-radiation penalties are
ignored.

### Consequence if ignored

- biased material ranking
- misleading crew-wall recommendations
- false confidence in “strong-looking” dense stacks

### IX-Mirror response

Every retained material branch must explicitly state whether secondaries are a
known, likely, unknown, or potentially disqualifying penalty term.

---

## R-05 — Shelter geometry that looks good on paper but fails real use

**Category:** architecture and geometry  
**Affected area:** shelter placement, refuge sizing, ingress logic  
**Status:** Open  
**Treatment:** Architecture Review + Modeling + Future Test

### Why this matters

A refuge concept can look compact and well-shielded while being too hard to
reach, too cramped, badly placed, or too dependent on unrealistic crew posture.

### Consequence if ignored

- excellent theoretical shielding with poor actual survivability
- slow ingress during acute events
- crew operational friction at the worst time

### IX-Mirror response

No shelter concept is acceptable unless it is tied to realistic occupancy,
ingress, and systems-continuity assumptions.

---

## R-06 — Reconfiguration dependence without graceful degradation

**Category:** operations and control  
**Affected area:** chamber routing, shelter activation logic, supervisory states  
**Status:** Tracked  
**Treatment:** Controls Review + Design Rule

### Why this matters

IX-Mirror gains value from reconfigurable mass and shelter mode, but any concept
that becomes useless when one actuator, valve, or route fails is too fragile.

### Consequence if ignored

- all-or-nothing protection posture
- dangerous operational dependence on perfect subsystem behavior
- false readiness during actual event conditions

### IX-Mirror response

The architecture must retain meaningful passive benefit in nominal mode and
remain useful in degraded mode.

---

## R-07 — Unknown state reported as healthy state

**Category:** operations and control  
**Affected area:** sensing, state-machine logic, crew cues  
**Status:** Tracked  
**Treatment:** Controls Review + Design Rule

### Why this matters

If the system loses knowledge of chamber status, route state, or protection
readiness and still reports success, the crew receives a false picture of their
actual protection posture.

### Consequence if ignored

- dangerous decision-making under uncertainty
- invalid confidence in shelter readiness
- post-event ambiguity that hides real failure

### IX-Mirror response

The state machine explicitly treats unknown as different from healthy. Reduced
visibility must remain visible to the crew and to logs.

---

## R-08 — Chamber complexity exceeds its value

**Category:** architecture and geometry  
**Affected area:** chambered wall concept, modular panel design  
**Status:** Open  
**Treatment:** Trade Study + Architecture Review

### Why this matters

Chambering is central to IX-Mirror, but it can become decorative complexity if
it adds routing, maintenance burden, leak paths, or packaging cost without
meaningful protection improvement.

### Consequence if ignored

- architecture bloat
- maintenance burden
- failure points multiplied without enough gain
- loss of credibility from complexity theater

### IX-Mirror response

Chambering must justify itself through geometry, shelter value, modularity,
fault isolation, or useful-mass placement. If it cannot, it should be simplified
or rejected.

---

## R-09 — Water or retained-water systems introduce containment burden

**Category:** materials and stack / architecture  
**Affected area:** chamber media, hydrogel concepts, refuge-local mass  
**Status:** Open  
**Treatment:** Trade Study + Future Test

### Why this matters

Water-rich media are promising, but containment, leakage, freeze/thaw behavior,
mass distribution, and serviceability can become serious design burdens.

### Consequence if ignored

- chamber failure
- maintenance headaches
- protection loss after local damage
- architecture burden disproportionate to benefit

### IX-Mirror response

Water and retained-water candidates stay in the baseline candidate set, but they
must later face containment and segmentation reality, not just shielding
intuition.

---

## R-10 — Boron-aware support layers get oversold

**Category:** materials and stack / claim discipline  
**Affected area:** support layers, mixed-field handling logic  
**Status:** Tracked  
**Treatment:** Design Rule + Trade Study

### Why this matters

Boron-aware or neutron-conscious layers may be useful, but it is easy to drift
into “cleanup layer solves the rest” language.

### Consequence if ignored

- magic-layer narrative
- false sense of mixed-field control
- weak support material turned into repository-wide miracle claim

### IX-Mirror response

These layers are treated as support-class candidates, not dominant wall classes
and not universal cleanup claims.

---

## R-11 — Electronics-local success contaminates crew-wall decisions

**Category:** architecture / materials  
**Affected area:** local specialty shielding modules, comparison studies  
**Status:** Tracked  
**Treatment:** Design Rule + Trade Study

### Why this matters

A dense local insert may be perfectly reasonable for electronics or detectors and
still be a poor choice for the human crew wall.

### Consequence if ignored

- hardware-focused logic masquerades as crew protection
- inappropriate scaling of local-use materials
- confusion in outside readers about what the architecture is optimizing for

### IX-Mirror response

Every branch must identify whether it is crew-facing, electronics-local, or both
with separate logic.

---

## R-12 — Shelter activation is too slow or too ambiguous

**Category:** operations and control  
**Affected area:** event response, ingress, supervisory transitions  
**Status:** Open  
**Treatment:** Controls Review + Architecture Review

### Why this matters

A strong shelter concept still fails if warning, transition, or ingress logic is
too slow, unclear, or operationally messy.

### Consequence if ignored

- avoidable acute-event exposure
- missed value from otherwise credible architecture
- high cognitive load under stress

### IX-Mirror response

The state-machine and shelter documents require explicit nominal mode, advisory
mode, shelter-preparation mode, and shelter-active mode distinctions.

---

## R-13 — Negative-control branches are removed too early

**Category:** evidence discipline  
**Affected area:** comparison studies, baseline argument strength  
**Status:** Open  
**Treatment:** Design Rule

### Why this matters

Some weak ideas are still useful in the repo because they prove why the baseline
is stronger. If all negative controls are removed too early, the architecture
can start to look unchallenged simply because weak alternatives vanished.

### Consequence if ignored

- weaker comparative reasoning
- less transparent baseline selection
- easier drift into self-congratulating documentation

### IX-Mirror response

Selected comparison branches should remain long enough to show why they lost.

---

## R-14 — Modeling theater replaces architecture thinking

**Category:** evidence discipline / modeling  
**Affected area:** future OLTARIS and Geant4 studies, result interpretation  
**Status:** Tracked  
**Treatment:** Modeling + Design Rule

### Why this matters

A polished model graphic can create more confidence than the underlying
assumptions deserve.

### Consequence if ignored

- simulation treated as proof
- hidden assumptions drive visible confidence
- repository grows prettier without growing stronger

### IX-Mirror response

All modeling output must state assumptions, preserve penalties, and avoid proof
language. Model results may support screening, not mission-readiness claims.

---

## R-15 — Patent prior art is mistaken for validation

**Category:** evidence discipline  
**Affected area:** external-source interpretation, architecture justification  
**Status:** Tracked  
**Treatment:** Design Rule

### Why this matters

Patents can be useful idea maps, but they are not proof that a concept works
well enough for astronaut safety.

### Consequence if ignored

- inflated confidence from disclosed concepts
- poor branch retention based on novelty instead of evidence
- hidden gap between prior art and real performance

### IX-Mirror response

Patents may inform architecture branches, but they must remain distinct from
validated modeling or test evidence.

---

## R-16 — Multifunctionality becomes an excuse for weak shielding

**Category:** architecture / trade study  
**Affected area:** structural-shielding composites, dual-use mass logic  
**Status:** Open  
**Treatment:** Trade Study + Architecture Review

### Why this matters

A material that does many jobs badly can still look attractive on paper because
it appears efficient.

### Consequence if ignored

- weak shielding hidden under “multifunctional” language
- weak structure hidden under “shielding” language
- no subsystem actually performs strongly enough

### IX-Mirror response

Multifunctionality is a bonus, not an exemption from shielding and architecture
performance screening.

---

## R-17 — Habitability gets treated as secondary paperwork

**Category:** architecture / operations  
**Affected area:** shelter design, interior layers, refuge occupancy  
**Status:** Open  
**Treatment:** Architecture Review + Future Test

### Why this matters

A crew refuge must still be occupiable, breathable, tolerable, and usable under
stress.

### Consequence if ignored

- refuge concept that is technically dense but practically unusable
- poor mission integration
- avoidable crew burden during already-dangerous conditions

### IX-Mirror response

Shelter evaluation must include occupancy, access, continuity, and interior
function rather than shielding geometry alone.

---

## R-18 — Unsupported exotic branches re-enter through vague language

**Category:** governance / claim discipline  
**Affected area:** future contributions, branch retention, repository language  
**Status:** Tracked  
**Treatment:** Scope Rejection + Design Rule

### Why this matters

Ideas based on unsupported acoustic shielding, generic resonance shielding,
scalar-field language, or vague charged-layer effects can reappear if the repo
allows fuzzy wording.

### Consequence if ignored

- baseline contamination
- reduced trust from technical readers
- loss of architecture clarity

### IX-Mirror response

These ideas may remain only as rejected-history context or as repurposed sensing
and controls inspiration. They may not return as baseline protective mechanism
claims.

---

## R-19 — Local leaks, punctures, or segment faults create hidden weak zones

**Category:** materials and stack / architecture  
**Affected area:** chambered media, modular walls, service seams  
**Status:** Open  
**Treatment:** Future Test + Architecture Review

### Why this matters

Segmented walls improve fault isolation, but they also create interfaces, seams,
and local states that may become weak points if not acknowledged.

### Consequence if ignored

- localized loss of protection
- hidden degradation
- service complexity
- false area-averaged confidence

### IX-Mirror response

Later modeling and physical checks should preserve directional and local weak-
spot awareness rather than relying only on average wall descriptions.

---

## R-20 — Repository coherence decays as files accumulate

**Category:** program and evidence discipline  
**Affected area:** entire repository  
**Status:** Open  
**Treatment:** Design Rule + Review Discipline

### Why this matters

A repository can begin strong and then slowly contradict itself as more files are
added.

### Consequence if ignored

- mismatched threat language
- duplicated claims with different limits
- accidental contradiction between architecture, controls, and modeling files
- weaker outside-reader trust

### IX-Mirror response

Each major new file should be checked against the charter, threat model, claim
boundaries, architecture overview, requirements, and verification roadmap before
it is accepted.

---

## Priority shortlist

At the current stage, the highest-priority risks to address first are:

1. **R-02 — Overstating GCR protection**
2. **R-03 — Misusing high-Z materials as a crew-wall default**
3. **R-05 — Shelter geometry that looks good on paper but fails real use**
4. **R-06 — Reconfiguration dependence without graceful degradation**
5. **R-12 — Shelter activation is too slow or too ambiguous**
6. **R-14 — Modeling theater replaces architecture thinking**
7. **R-18 — Unsupported exotic branches re-enter through vague language**

These are the risks most likely to break IX-Mirror early.

## Closure rule

A risk should not be marked closed merely because it was mentioned.

A risk may be considered meaningfully reduced only if one of the following
happens:

- the architecture contains it through explicit design rule
- a trade study shows why the weaker branch lost
- a model comparison reduces uncertainty in a bounded way
- a controls review defines safe degraded behavior
- future physical testing grounds the open assumption

## Final statement

IX-Mirror is stronger when its risks are visible.

Hidden risk is just undisclosed weakness.
