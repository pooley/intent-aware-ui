# Design Principles

> Designing interfaces that assist without taking control.
>
> **Status:** Draft · **Version:** 0.1.0 · **Last Updated:** 2026-07-16

**[📚 Documentation Index](README.md)** · ← [Concept Map](concept-map.md) · [Accessibility](accessibility.md) →

This document describes the design principles behind Intent-Aware UI.

Unlike the Specification, which defines the interaction model, these principles provide practical guidance for designing predictable, accessible and trustworthy interfaces.

---

# 1. Assistance, Not Automation

The purpose of Intent-Aware UI is to reduce effort.

It is **not** to make decisions on behalf of the user.

An interface should assist interactions without replacing them.

The user must always remain responsible for the final action.

✓ Good

The interface subtly helps the user reach a target.

✗ Bad

The interface selects or activates a target automatically.

---

# 2. Predictability Over Efficiency

An interaction that is slightly slower but predictable is preferable to a faster interaction that surprises the user.

Users should always understand why an interface behaves the way it does.

If assistance becomes unpredictable, trust is lost.

---

# 3. Confidence Should Be Progressive

Intent is rarely binary.

Confidence should increase progressively as more evidence becomes available.

Avoid abrupt transitions.

✓ Good

A gradual visual response.

✗ Bad

A target suddenly jumps toward the pointer.

---

# 4. Movement Must Remain Minimal

Interactive elements should never travel large distances.

Movement exists only to reduce acquisition effort.

As a general guideline:

- translation should remain subtle
- scaling should remain subtle
- animations should remain calm

Motion should communicate confidence, not attract attention.

---

# 5. Preserve Spatial Memory

Users build a mental map of interfaces.

Large movements break this map.

Interactive elements should remain where users expect them to be.

Intent-Aware UI adapts interaction, not layout.

---

# 6. One Intent, One Target

At any given moment, assistance should focus on a single target.

Competing interactions create uncertainty.

Intent Fields should never overlap.

---

# 7. Safe Zones Matter

Empty space is not wasted space.

Neutral areas between interactive elements reduce:

- accidental activation
- ambiguity
- interaction conflicts

Safe Zones improve both usability and accessibility.

---

# 8. Feedback Should Explain

Users should understand that the interface has detected their intent.

Visual feedback should communicate confidence without becoming distracting.

Examples include:

- glow
- elevation
- subtle scaling
- gentle motion

Feedback should feel informative, not decorative.

---

# 9. Never Fight the User

The pointer must never feel trapped.

Users should always be able to:

- leave a target
- change their mind
- move toward another target

Intent-Aware UI should never resist user input.

---

# 10. Accessibility Is the Default

Intent-Aware UI is not an accessibility mode.

It is an interaction model designed to naturally reduce motor effort for everyone.

The same principles should benefit:

- expert users
- beginners
- older adults
- users with temporary impairments
- users with permanent motor disabilities

Accessibility should emerge from good interaction design.

---

# 11. Visual Calm

Assistance should remain almost invisible.

Users should notice that interactions feel easier.

They should not notice constant animations.

Good assistance disappears into the experience.

---

# 12. Respect Existing Standards

Intent-Aware UI complements existing design systems.

It does not replace:

- WCAG
- platform guidelines
- keyboard interactions
- focus management
- accessible sizing

Existing accessibility practices remain essential.

---

# 13. Design for Trust

Trust is the foundation of assisted interaction.

Users should never wonder:

> "Why did that happen?"

Every visual response should have an understandable cause.

Trust grows when interactions are:

- consistent
- reversible
- proportional
- predictable

---

# Summary

Intent-Aware UI is built on a simple philosophy:

- Understand before reacting.
- Assist before correcting.
- Reduce effort without removing control.
- Adapt to people instead of asking people to adapt.

Good interfaces are not those that move the most.

They are those that ask the least effort from the user.
