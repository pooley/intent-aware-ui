# Prior Art

> Intent-Aware UI builds upon decades of research and experimentation in Human-Computer Interaction.
>
> **Status:** Draft · **Version:** 0.1.0 · **Last Updated:** 2026-07-16

**[📚 Documentation Index](README.md)** · ← [Research](research.md) · [Roadmap](roadmap.md) →

This document acknowledges existing interaction techniques that explore similar challenges.

Intent-Aware UI does **not** claim to invent assisted interaction.

Instead, it proposes a framework that attempts to unify several ideas under a single interaction model centered around user intent.

---

# Why this document?

Many interaction techniques already explore ways to make target acquisition easier.

Some enlarge targets.

Some modify cursor behavior.

Others predict user intent.

Intent-Aware UI exists within this broader ecosystem.

Understanding prior work is essential to understanding the project itself.

This document deliberately stays at the level of named techniques, products and prototypes. Foundational scientific models — Fitts' Law, the Steering Law, the Midas Touch problem — are covered in [Research](research.md) instead, so the two documents don't overlap.

Full bibliographic entries for the citations below are collected in the [Research bibliography](research.md#bibliography).

---

# Bubble Cursor

Bubble Cursor (Grossman & Balakrishnan, 2005) introduced a dynamic pointing technique where the cursor's effective selection radius expands to reach the nearest target.

It reduces pointing difficulty without modifying interface layout.

Similarity:

- dynamic acquisition

Difference:

- Bubble Cursor adapts the cursor.

- Intent-Aware UI proposes adapting interaction confidence.

---

# Sticky Targets

Various interaction techniques introduce friction or attraction around interface elements.

Their objective is to make targets easier to acquire.

Similarity:

- assisted acquisition

Difference:

- Intent-Aware UI explicitly separates:

    - Intent Detection
    - Confidence
    - Assistance
    - Activation

rather than relying solely on physical attraction.

---

# Semantic Pointing

Semantic Pointing dynamically modifies pointer behavior depending on the surrounding interface.

Similarity:

- adaptive pointing

Difference:

- Intent-Aware UI does not prescribe cursor manipulation.

Cursor adaptation is only one possible implementation.

---

# Target Expansion

Numerous systems enlarge targets dynamically when interaction is likely (Zhai, Conversy, Beaudouin-Lafon & Guiard, 2003).

Similarity:

- dynamic target sizing

Difference:

Intent-Aware UI treats target expansion as one possible assistance strategy rather than a defining feature.

---

# Adaptive Menus

Adaptive menus reorder, resize or expose items according to predicted usage.

Similarity:

- adaptive interfaces

Difference:

Intent-Aware UI focuses on interaction mechanics rather than information architecture.

---

# Eye Tracking Research

Eye-tracking interfaces continuously estimate user attention.

This is also the context in which the [Midas Touch Problem](glossary.md#midas-touch-problem) was first identified — though the risk it names is general, not specific to gaze.

Similarity:

- continuous intent estimation

Difference:

Intent-Aware UI always requires explicit confirmation before activation, treating avoidance of the Midas Touch effect as a hard requirement (Specification §8) rather than a lesson borrowed from this prior art.

---

# Predictive Pointing

Several research projects investigate trajectory prediction and probabilistic pointing.

Similarity:

- predicting future interaction

Difference:

Intent-Aware UI intentionally leaves prediction algorithms unspecified.

The specification defines behavior, not implementation.

---

# Motor Accessibility Research

Many accessibility studies investigate:

- tremor compensation
- input filtering
- cursor stabilization
- adaptive gain
- enlarged targets

Intent-Aware UI seeks to complement these approaches rather than replace them.

---

# What Intent-Aware UI Adds

Intent-Aware UI does not introduce a new pointing device.

It does not introduce a new cursor.

It does not introduce a new accessibility technology.

Instead, it proposes an interaction model structured around four concepts:

- Intent Detection
- Confidence
- Progressive Assistance
- Activation

These concepts may be implemented using different technologies while remaining compatible with existing HCI research.

---

# This document is intentionally incomplete.

Human-Computer Interaction is an active research field.

Additional references, papers and interaction techniques will be added as the project evolves.

Contributions are welcome.
