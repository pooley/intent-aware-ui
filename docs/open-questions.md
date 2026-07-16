# Open Questions

> Intent-Aware UI is an open research initiative.
>
> **Status:** Draft · **Version:** 0.1.0 · **Last Updated:** 2026-07-16

**[📚 Documentation Index](README.md)** · ← [Roadmap](roadmap.md)

This document collects the questions that remain intentionally unanswered.

These are not missing features.

They are research opportunities.

---

# Interaction

## How should confidence be calculated?

The specification intentionally leaves confidence estimation undefined.

Possible approaches include:

- distance
- velocity
- trajectory
- pointer stability
- dwell time

Should every implementation use the same model?

Or should confidence remain implementation-specific?

---

## Should confidence be observable?

Should implementations expose confidence values?

Or should confidence remain an internal mechanism?

---

## Can confidence decrease?

Should confidence only increase?

Or should it continuously adapt when user intent changes?

---

# Motion

## How much movement is acceptable?

Movement may reduce acquisition effort.

Too much movement may reduce predictability.

Where is the balance?

---

## Should movement always be optional?

Should interfaces be allowed to disable movement entirely while remaining compliant?

---

## Is cursor guidance preferable to target movement?

Both approaches exist.

Should one be preferred?

Can both coexist?

---

# Intent Fields

## Should Intent Fields always have a fixed size?

Could they adapt to:

- context
- device
- density
- interaction history

---

## How should competing Intent Fields be resolved?

Several strategies are possible.

Should ownership depend on:

- distance
- trajectory
- confidence
- velocity

Or something else?

---

# Accessibility

## Should assistance adapt to individual users?

Would personalization improve usability?

Or would it reduce predictability?

---

## Should assistance be configurable?

Could users choose:

- assistance strength
- animation
- movement
- visual feedback

Without fragmenting the interaction model?

---

# Evaluation

## How should Intent-Aware UI be measured?

Possible metrics include:

- acquisition time
- error rate
- correction count
- motor effort
- user confidence
- perceived comfort
- cognitive load

Which metrics matter most?

---

## What defines success?

Would faster interactions be enough?

Or should the project primarily optimize:

- comfort
- accessibility
- trust
- predictability

---

# Platform Support

## Does the model translate to touch interfaces?

Touch introduces different interaction constraints.

Can Intent Fields exist without a cursor?

---

## Can the model apply to eye tracking?

Intent estimation becomes even more important.

Could explicit Activation prevent the Midas Touch problem?

---

## What about VR and AR?

Spatial interfaces introduce:

- depth
- gaze
- gestures
- hand tracking

Should the same principles apply?

---

# Future

Intent-Aware UI does not aim to answer all these questions today.

Instead, it aims to create a common framework within which these questions can be explored.

Contributions are welcome.
