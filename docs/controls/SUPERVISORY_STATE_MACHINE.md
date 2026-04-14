# Supervisory State Machine

## Purpose

This document defines the baseline supervisory state-machine concept for
IX-Mirror.

The state machine exists to keep the architecture operationally disciplined.
IX-Mirror is not just a wall concept. It includes chambered shielding logic,
shelter activation logic, state awareness, and event-driven behavior. Without a
clear supervisory model, those features collapse into vague promises.

This document does **not** claim flight software readiness or a validated
embedded implementation. It defines the control logic posture that future
software, simulation, and hardware-in-the-loop work would need to follow.

## Control philosophy

IX-Mirror adopts the following control philosophy:

- explicit states are better than implied behavior
- crew protection logic must remain understandable under stress
- sensing and control support shielding architecture, but do not replace it
- the system must remain useful under partial failure
- event response must favor safe bounded behavior over clever complexity
- logs and observability matter because post-event ambiguity is a safety problem

This document keeps the disciplined parts of prior control-oriented work and
drops unsupported “field-effect” logic entirely.

## Supervisory scope

The IX-Mirror supervisory layer is responsible for:

- maintaining declared operating state
- interpreting radiation-event inputs and system-health inputs
- commanding transitions between nominal and shelter-oriented postures
- tracking whether commanded routing or configuration changes were achieved
- providing crew-facing status clarity
- supporting degraded-mode operation
- recording state transitions and major anomalies

The supervisory layer is **not** the radiation shield itself. It is the logic
that makes the rest of the architecture more usable and less error-prone.

## State model overview

The baseline IX-Mirror state model includes seven top-level states:

1. **Standby**
2. **Nominal**
3. **Advisory**
4. **Shelter Preparation**
5. **Shelter Active**
6. **Degraded Protection**
7. **Recovery and Review**

These states are intentionally simple at the top level. More detailed
substates may be added later, but the baseline repository should stay readable.

## State 1 — Standby

### Intent

Standby represents a pre-operations, low-activity, or initialization state.

### Typical use

- vehicle startup
- habitat startup
- subsystem initialization
- maintenance hold
- simulation or test initialization

### Expected conditions

- no active shelter event
- no commitment to reconfiguration
- system self-checks allowed
- sensor health and route-state checks may run
- crew-facing status should clearly indicate that the system is not in
  protective event mode

### Exit conditions

The system exits Standby when:

- initialization checks complete successfully
- a controlled transition to Nominal is authorized
- a significant fault requires direct move to Degraded Protection
- a verified event indication requires bypass to Advisory or Shelter Preparation

## State 2 — Nominal

### Intent

Nominal is the default operating state during normal mission activity.

### Expected conditions

- wall and chamber configuration are in baseline mission posture
- shelter volume exists but is not in emergency-use posture
- event monitoring remains active
- dosimetry and health telemetry remain active
- crew can perform ordinary work and habitation activities

### Typical behaviors

- maintain baseline chamber configuration
- monitor radiation-event indicators
- monitor chamber integrity and route integrity
- monitor occupancy-related context if available
- log significant state changes or system degradations

### Design rule

Nominal must still provide useful passive protective value even if no later
state transition succeeds.

### Exit conditions

Nominal exits to:

- **Advisory** when event indicators or warning sources cross defined thresholds
- **Degraded Protection** when a fault materially reduces expected protection
  posture or observability
- **Recovery and Review** only after a prior event or fault path has been closed

## State 3 — Advisory

### Intent

Advisory is the pre-event or possible-event awareness state.

It exists to avoid the false binary of “everything is normal” versus
“everyone shelter now.” Advisory gives IX-Mirror time to elevate awareness,
prepare the crew, and verify the system before committing to full shelter mode.

### Expected conditions

- elevated event concern exists
- crew awareness should increase
- shelter availability should be checked
- chamber and route status should be validated
- the system should prepare for rapid escalation if needed

### Typical behaviors

- increase telemetry priority
- run readiness checks on reconfiguration-capable elements
- confirm shelter zone availability
- confirm key sensors remain healthy
- elevate crew cues and event-status messaging
- pre-stage if mission rules allow

### Exit conditions

Advisory exits to:

- **Shelter Preparation** when event severity or confidence increases
- **Nominal** if the event concern is cleared and the system remains healthy
- **Degraded Protection** if required protective subsystems are not available

## State 4 — Shelter Preparation

### Intent

Shelter Preparation is the controlled transition state between normal operations
and active refuge posture.

### Expected conditions

- acute-event response is being initiated
- crew should be moving toward or preparing to move toward refuge
- local mass concentration and routing commands may be issued
- the system must determine whether commanded configuration changes were achieved

### Typical behaviors

- issue shelter-preparation command set
- request chamber-routing or chamber-lock state changes where supported
- confirm or estimate local protective-state readiness
- command crew-facing shelter indicators
- prioritize event-relevant dosimetry and health channels
- place nonessential functions into lower-priority posture if needed

### Important constraint

Shelter Preparation must not wait forever for perfection. If enough protective
value is already present and event urgency rises, the system should escalate to
Shelter Active even if some optimization actions remain incomplete.

### Exit conditions

Shelter Preparation exits to:

- **Shelter Active** when the refuge posture is sufficiently established or when
  the event timeline demands immediate occupation
- **Degraded Protection** when the architecture cannot reliably achieve intended
  shelter configuration and the crew must operate under reduced-confidence
  protection logic
- **Nominal** only if the event is clearly dismissed before full transition

## State 5 — Shelter Active

### Intent

Shelter Active is the acute-event refuge state.

This is the main crew-protection operating state during a declared SPE / SEP
response.

### Expected conditions

- crew is in or moving into the designated refuge volume
- local protection posture is stronger than nominal mission posture
- dosimetry and event awareness remain high priority
- the system favors survival and clarity over routine convenience

### Typical behaviors

- maintain or verify shelter configuration
- track crew occupancy confirmation if available
- monitor protective subsystem status
- track degraded conditions and communicate them clearly
- maintain event logging
- protect critical continuity functions needed during refuge occupancy

### Operational rule

Shelter Active should continue to provide clear indication of whether the
protective posture is:

- fully established
- partially established
- degraded
- uncertain

The system must not present uncertain protection status as though it were fully
verified.

### Exit conditions

Shelter Active exits to:

- **Recovery and Review** when the event is over and safe transition out of
  shelter posture is authorized
- **Degraded Protection** if the active refuge posture materially degrades during
  the event

## State 6 — Degraded Protection

### Intent

Degraded Protection exists for conditions where IX-Mirror still provides some
protective value, but not the intended full or best-known configuration.

This state is essential because real missions are not entitled to perfect
sensors, perfect routing, or perfect actuation.

### Conditions that may trigger entry

Examples include:

- one or more chamber segments unavailable
- route-state mismatch
- valve or actuator failure
- uncertain chamber fill status
- partial loss of dosimetry
- partial loss of occupancy sensing
- loss of enough observability that protection confidence drops
- structural or leakage condition that reduces expected local benefit

### Typical behaviors

- freeze or simplify control actions
- preserve known-safe protective configuration
- warn the crew about degraded confidence or reduced capability
- avoid oscillating between states
- continue logging
- maintain the best achievable refuge posture given current conditions

### Design rule

Degraded Protection is not system collapse.

It is the repository’s way of acknowledging that partial protection and honest
status are better than pretending the system still achieved a fully verified
configuration.

### Exit conditions

Degraded Protection exits to:

- **Shelter Active** if sufficient capability is restored during an event
- **Recovery and Review** if the event has passed and re-stabilization is safe
- **Nominal** only after explicit reset and health verification outside event
  conditions

## State 7 — Recovery and Review

### Intent

Recovery and Review is the post-event or post-anomaly stabilization state.

### Typical behaviors

- hold or gradually release shelter-related reconfiguration
- verify subsystem health before returning to Nominal
- record event summary and anomaly summary
- review route-state and integrity-state results
- identify whether post-event maintenance or inspection is required

### Exit conditions

Recovery and Review exits to:

- **Nominal** after health verification and safe reversion
- **Standby** for maintenance or reset
- **Degraded Protection** if new issues are discovered during review

## Top-level transition summary

The baseline intended transition structure is:

- Standby -> Nominal
- Standby -> Advisory
- Standby -> Degraded Protection

- Nominal -> Advisory
- Nominal -> Degraded Protection

- Advisory -> Nominal
- Advisory -> Shelter Preparation
- Advisory -> Degraded Protection

- Shelter Preparation -> Shelter Active
- Shelter Preparation -> Degraded Protection
- Shelter Preparation -> Nominal

- Shelter Active -> Recovery and Review
- Shelter Active -> Degraded Protection

- Degraded Protection -> Shelter Active
- Degraded Protection -> Recovery and Review
- Degraded Protection -> Nominal

- Recovery and Review -> Nominal
- Recovery and Review -> Standby
- Recovery and Review -> Degraded Protection

## Trigger categories

IX-Mirror supervisory logic should treat triggers as belonging to one of four
categories:

### 1. Event triggers

Examples:

- external radiation warning input
- local dose-rate trend threshold
- declared SPE / SEP event state
- event escalation or event clear signal

### 2. Configuration triggers

Examples:

- route-state confirmation
- chamber-fill confirmation
- local shelter posture achieved
- route-state mismatch
- protected-volume readiness confirmed

### 3. Health triggers

Examples:

- sensor failure
- chamber leak indication
- valve or routing fault
- communications loss in the protection network
- structural or subsystem health alarms relevant to protection posture

### 4. Human / operations triggers

Examples:

- crew acknowledgment
- crew shelter occupancy confirmation
- manual safe-mode request
- manual inhibit or maintenance lock
- mission-control or command-authority override

## Command classes

The supervisory layer may issue the following classes of command:

- status-display commands
- shelter-state commands
- route or chamber configuration commands
- mode-transition commands
- logging and record commands
- subsystem-health interrogation requests
- degraded-mode freeze or simplify commands

These command classes are intentionally generic at this stage.

## Required observability

The state machine is only useful if the system can observe enough truth to avoid
fiction.

At concept stage, IX-Mirror expects observability in the following areas where
supported:

- radiation event state
- local dosimetry trend
- chamber health or chamber integrity
- route-state confirmation
- protective configuration achieved / not achieved / unknown
- crew occupancy confirmation where practical
- alarm and fault state
- ability to distinguish sensor loss from safe state

## Unknown-state rule

A critical IX-Mirror rule is:

**unknown is not the same as healthy**

If the system loses visibility into a protection-critical variable, it should
not silently report success. It should move to or remain in a state that makes
the uncertainty visible.

## Manual override rule

Manual control may exist, but it must be bounded.

The system should allow controlled manual intervention for:

- maintenance
- test
- contingency override
- mission-rule-based command authority

Manual override should not erase logs, bypass uncertainty reporting, or conceal
degraded status.

## Anti-oscillation rule

The supervisory logic should avoid rapid state thrashing.

Possible means include:

- dwell timers
- event-confidence hysteresis
- minimum confirmation windows
- lockout intervals after major transitions
- explicit operator acknowledgment for selected reversions

The exact implementation can be refined later, but the design principle is
required now.

## Logging requirements

At minimum, the state machine should log:

- state entry time
- state exit time
- transition cause
- event trigger source
- major fault declarations
- route-state mismatch events
- occupancy confirmation events where available
- degraded-protection entry reason
- recovery-complete declaration

These logs are valuable for both technical review and safety accountability.

## Failure-aware examples

### Example 1 — Advisory with route uncertainty

If an event warning arrives but the chamber-route verification path is partially
offline, the system should still elevate to Advisory rather than pretending
everything is fine. It may then enter Shelter Preparation with explicit reduced
confidence.

### Example 2 — Shelter command with incomplete chamber response

If shelter routing is commanded and only part of the desired concentration
changes succeed, the system should not claim full shelter readiness. It should
declare either partial readiness within Shelter Active or move to Degraded
Protection depending on severity.

### Example 3 — Event clears during shelter occupancy

If event status clears after the crew has sheltered, the system should not jump
straight back to Nominal. It should pass through Recovery and Review.

## Relation to other IX-Mirror documents

This state machine is coupled to:

- the threat model
- the baseline layer stack
- the storm-shelter concept
- the requirements and acceptance criteria
- future verification planning
- future risk register work

If those documents change materially, the state machine should be reviewed.

## Out-of-scope claims

This document does not claim:

- certified fault tolerance
- verified software implementation
- exact event thresholds
- final sensor selection
- final actuator architecture
- final command authority structure
- mission-ready automation

It defines disciplined supervisory behavior at architecture level only.

## Final statement

The IX-Mirror state machine exists for one reason:

during a real radiation event, confusion is a design failure.
