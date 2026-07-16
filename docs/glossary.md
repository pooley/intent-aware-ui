# Glossary

> Shared terminology for the Intent-Aware UI specification.
>
> **Status:** Draft · **Version:** 0.1.0 · **Last Updated:** 2026-07-16

**[📚 Documentation Index](README.md)** · ← [Manifesto](manifesto.md) · [Architecture](architecture.md) →

This glossary defines the official vocabulary used throughout the project.

Each term has a single meaning and should be used consistently across documentation, implementations and discussions.

Eight of these terms are marked **★ Core Concept** — they form the frozen list defined in the [Specification](specification.md#core-concepts). Every other entry is supporting vocabulary, free to grow as the project needs it.

---

# A

## Activation

★ **Core Concept**

The moment an interaction is confirmed and the intended action is executed.

In most graphical interfaces, activation occurs through a click, tap or keyboard action.

Intent-Aware UI does not replace activation; it assists the path leading to it.

---

## Assistance

A subtle adaptation of an interface intended to reduce the effort required to acquire an interactive target.

Assistance must never replace user intent or automatically trigger actions.

Examples include:

- slight target movement
- progressive scaling
- cursor guidance
- dynamic hit area adjustment
- visual feedback

---

# C

## Confidence

★ **Core Concept**

A continuous value representing how likely the system believes the user intends to interact with a specific target.

Confidence is not binary.

It progressively evolves throughout the interaction.

Higher confidence may enable stronger forms of assistance.

---

## Confidence Curve

The progression of confidence over time as the user's interaction evolves.

Rather than immediately switching between states, confidence should increase and decrease smoothly.

---

# E

## Engagement Field

★ **Core Concept**

The inner area surrounding an interactive target.

Entering this area indicates a high probability of user intent.

Within the Engagement Field, stronger assistance may be applied while preserving predictability.

---

# I

## Intent

★ **Core Concept**

The user's probable objective before an interaction is confirmed.

Intent exists before activation and may evolve continuously during pointer movement.

---

## Intent Confidence

See **Confidence**.

---

## Intent Detection

The process of estimating user intent from interaction signals.

Possible signals include:

- pointer trajectory
- direction
- speed
- stability
- proximity
- dwell time

Intent detection never guarantees user intention.

It only estimates probability.

---

## Intent Field

★ **Core Concept**

The invisible area surrounding an interactive element used to estimate user intent.

The Intent Field represents the first level of interaction awareness.

It is responsible for detecting intent before engagement occurs.

---

## Intent Ownership

The principle stating that every point within an interface belongs to a single dominant Intent Field.

Intent Fields must never compete for ownership of the same interaction space.

This prevents ambiguity and unstable assistance.

---

## Interaction Model

The complete set of rules describing how an interface reacts to user input.

Intent-Aware UI proposes an interaction model based on continuous intent estimation rather than binary events.

---

# M

## Midas Touch Problem

The risk that a system reacts as soon as it detects apparent intent, before the user has actually decided to act.

Named after the myth of King Midas, whose touch turned everything to gold whether he intended it or not.

First studied in gaze-based interaction research (see [Research](research.md#the-midas-touch-problem)), but the risk applies to any interaction model where assistance could become automatic — Intent-Aware UI included.

Avoiding this effect is a hard requirement, not a design preference: see [Activation](specification.md) (Specification §8).

---

# P

## Predictability

A fundamental principle stating that interface behaviour must always remain understandable.

Users should be able to anticipate how an interface will react.

Predictability always takes priority over aggressive assistance.

---

## Progressive Assistance

★ **Core Concept**

The principle that assistance increases gradually as confidence grows.

Interfaces should never abruptly change behaviour.

Transitions must remain smooth, predictable and reversible.

---

# S

## Safe Zone

★ **Core Concept**

A neutral area separating two or more interactive elements.

Safe Zones contain no interaction assistance.

They reduce ambiguity, prevent accidental activation and improve interaction clarity.

---

## Snap

A sudden attraction toward a target.

Intent-Aware UI discourages abrupt snapping in favour of progressive assistance.

---

# T

## Target

Any interactive element capable of receiving user input.

Examples include:

- buttons
- links
- checkboxes
- switches
- sliders
- menu items
- tabs
- resize handles

---

## Target Acquisition

The process of successfully reaching an intended interactive target.

Reducing the effort required for target acquisition is one of the primary goals of Intent-Aware UI.

---

# U

## User Agency

★ **Core Concept**

The principle that users always remain in control of their interactions.

Intent-Aware UI assists interaction without making decisions on behalf of the user.

Activation must always remain intentional.

---

# V

## Visual Feedback

Visual information communicating the system's current understanding of interaction.

Examples include:

- glow
- halo
- scale
- elevation
- subtle motion

Visual feedback should communicate confidence without distracting the user.

---

# Terminology Principles

Throughout this project:

- **Intent** is never certainty.
- **Confidence** is always continuous.
- **Assistance** never replaces control.
- **Activation** always requires user confirmation.

These principles form the common language of the Intent-Aware UI specification.
