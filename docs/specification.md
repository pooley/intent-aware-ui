# Intent-Aware UI Specification

> **Status:** Draft · **Version:** 0.1.0 · **Last Updated:** 2026-07-16

**[📚 Documentation Index](README.md)** · ← [Architecture](architecture.md) · [Concept Map](concept-map.md) →

This document defines the normative interaction model for Intent-Aware UI.

Terminology used in this document follows the [Glossary](glossary.md).

## Conformance Language

This specification uses the terms **MUST**, **MUST NOT**, **SHOULD**, **SHOULD NOT** and **MAY** to distinguish mandatory requirements from recommendations and optional behaviors.

## Core Concepts

The following concepts are defined in the [Glossary](glossary.md) and form the conceptual foundation of Intent-Aware UI. Eight of them form the stable core of this specification — everything else in this document exists to define how they relate to each other:

1. Intent
2. Intent Field
3. Engagement Field
4. Confidence
5. Progressive Assistance
6. Safe Zone
7. Activation
8. User Agency

This list is frozen by design. Adding a ninth core concept should require strong justification, not incremental convenience. Supporting terms (see the [Glossary](glossary.md)) may still be introduced freely: they clarify these eight, they don't join them.

---

# 1. Purpose

Intent-Aware UI defines an interaction model where interfaces progressively estimate user intent before an interaction is confirmed.

Unlike traditional interaction models that react only after activation, Intent-Aware UI introduces a continuous interaction phase between pointer movement and activation.

Its objective is to reduce the motor precision required to acquire interactive targets while preserving user agency.

---

# 2. Principles

The following principles define how the Core Concepts above must behave. They are constraints on the system, not concepts in themselves. Every implementation MUST respect them.

- User Agency
- Predictability
- Progressive Assistance
- Accessibility by Design
- Reversibility
- Explicit Activation

These principles take precedence over implementation details.

---

# 3. Interaction Lifecycle

Every interaction follows the same lifecycle.

```
Idle

↓

Intent Detection

↓

Confidence Estimation

↓

Progressive Assistance

↓

Activation

↓

Completed
```

No implementation SHOULD skip a phase.

---

# 4. Intent Field

Every interactive target MUST define exactly one Intent Field.

The Intent Field is an invisible area surrounding the target.

Its purpose is to estimate the probability that the user intends to interact with the associated target.

Entering an Intent Field MUST NOT trigger activation.

Entering an Intent Field MAY trigger subtle visual feedback.

---

# 5. Engagement Field

The Engagement Field is a subset of the Intent Field.

It represents a high-confidence interaction zone.

Within this field, implementations MAY apply stronger assistance.

Examples include:

- slight scaling
- slight translation
- increased effective hit area
- enhanced visual feedback

Implementations MUST preserve predictability.

---

# 6. Confidence

Confidence represents the estimated probability that a target is the user's intended destination.

Confidence MUST be continuous.

Confidence MUST NOT be binary.

Confidence SHOULD evolve smoothly over time.

Confidence MAY decrease if user behaviour indicates a change of intent.

---

# 7. Assistance

Assistance MAY begin only after intent has been detected.

Assistance MUST remain proportional to confidence.

Assistance MUST never prevent the user from reaching another target.

Possible assistance includes:

- visual emphasis
- target scaling
- target translation
- cursor guidance
- dynamic hit area adaptation

Implementations MAY introduce other forms of assistance provided they respect the core principles.

---

# 8. Activation

Activation always requires explicit user confirmation.

Intent-Aware UI MUST NOT automatically activate a target solely because confidence reaches its maximum.

Intent-Aware UI MUST avoid introducing a Midas Touch effect: reacting as if intent were confirmed before the user has actually decided to act (see [Glossary](glossary.md#midas-touch-problem)).

Examples of valid activation events include:

- mouse click
- touch release
- keyboard confirmation
- assistive technology activation

---

# 9. User Agency

The user MUST remain in control at all times.

Implementations MUST NOT:

- hijack cursor movement
- prevent leaving an Intent Field
- activate targets automatically
- surprise the user

Users MUST always be able to interrupt or reverse an interaction.

When behavior is ambiguous, an implementation MUST fail toward inaction rather than unintended action.

---

# 10. Intent Ownership

Every point within the interface MUST belong to at most one Intent Field.

Intent Fields MUST NOT overlap.

When two potential targets compete for ownership, implementations MUST resolve the conflict before assistance begins.

Implementations MAY choose their own conflict-resolution strategy.

---

# 11. Safe Zones

Interfaces SHOULD preserve neutral areas between adjacent Intent Fields.

Safe Zones reduce:

- accidental activation
- ambiguity
- interaction conflicts

Safe Zones SHOULD increase as interaction density increases.

---

# 12. Visual Feedback

Visual feedback SHOULD communicate confidence.

Visual feedback MUST remain subtle.

Recommended examples include:

- glow
- elevation
- opacity
- scale
- halo

Visual feedback MUST never distract from the primary task.

---

# 13. Motion

Motion SHOULD support comprehension.

Motion MUST remain physically plausible.

Motion MUST remain reversible.

Motion MUST NOT reduce precision.

Large translations SHOULD be avoided.

---

# 14. Accessibility

Intent-Aware UI complements existing accessibility guidelines.

It MUST NOT replace:

- accessible sizing
- keyboard navigation
- screen reader support
- focus management
- existing accessibility standards

Intent-Aware UI enhances interaction.

It does not replace accessibility.

---

# 15. Implementation Freedom

This specification intentionally does not prescribe:

- confidence algorithms
- physics models
- animation libraries
- rendering technologies
- implementation frameworks

Different implementations MAY explore different strategies provided they remain compliant with this specification.

---

# 16. Out of Scope

This specification does not define:

- machine learning models
- eye tracking
- gesture recognition
- haptic feedback
- operating-system integrations

Future versions MAY extend the specification.

---

# 17. Compliance

An implementation may claim compliance with Intent-Aware UI only if it satisfies all mandatory requirements defined in this specification.

Optional behaviors remain implementation-specific.
