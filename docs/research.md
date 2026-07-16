# Research

> Intent-Aware UI is built upon decades of research in Human-Computer Interaction (HCI), accessibility and motor behavior.
>
> **Status:** Draft · **Version:** 0.1.0 · **Last Updated:** 2026-07-16

**[📚 Documentation Index](README.md)** · ← [FAQ](faq.md) · [Prior Art](prior-art.md) →

This document summarizes the scientific concepts and interaction models that inspired the project.

Intent-Aware UI does not aim to replace these works.

Instead, it explores how they can be extended through intent-aware interaction.

---

# Human-Computer Interaction

Human-Computer Interaction (HCI) studies how people interact with digital systems.

For decades, researchers have explored ways to make interfaces:

- faster
- easier
- safer
- more accessible
- less physically demanding

Intent-Aware UI should be understood as part of this ongoing research effort.

---

# Fitts' Law

Paul Fitts demonstrated that the time required to acquire a target depends primarily on:

- the distance to the target
- the size of the target

This principle remains one of the foundations of interaction design.

It explains why larger targets are generally easier and faster to acquire.

Intent-Aware UI fully embraces Fitts' Law (Fitts, 1954).

Rather than replacing it, the project explores whether interaction behavior itself can also contribute to reducing acquisition effort.

---

# Steering Law

The Steering Law (Accot & Zhai, 1997) extends Fitts' Law to continuous movements.

It describes the difficulty of navigating constrained paths such as:

- cascading menus
- sliders
- drawing tools
- narrow interaction corridors

Intent-Aware UI may eventually explore whether adaptive assistance can reduce steering effort while preserving user control.

This remains an open research question.

---

# Dynamic Target Acquisition

A body of HCI research explores adapting cursor or target properties dynamically, rather than relying on fixed, static geometry — for example by resizing the effective pointing area, or by introducing friction or attraction near interactive elements.

Intent-Aware UI sits within this same broad direction. It explores a different underlying model, based on progressive intent estimation rather than purely geometric or physical adaptation.

Specific techniques within this space, and how each compares to Intent-Aware UI, are catalogued in [Prior Art](prior-art.md) rather than named here.

---

# The Midas Touch Problem

The *Midas Touch Problem*, originally described in gaze-based interaction research (Jacob, 1990), illustrates a broader challenge of implicit interaction: when a system reacts before the user has explicitly confirmed their intention.

Named after the myth of King Midas, whose touch turned everything to gold whether he intended it or not — a system exhibiting this effect acts on every apparent intention, whether the user meant to trigger it or not.

Although first studied in eye-tracking interfaces, the same principle applies to any interaction model where assistance risks becoming automatic — including gesture interfaces and, potentially, Intent-Aware UI itself if it isn't designed carefully.

This is precisely why Explicit Activation is a non-negotiable requirement of the Specification (§8), not a design preference: Intent-Aware UI treats avoiding a Midas Touch effect as a hard constraint, not an inspiration drawn from prior art.

---

# Motor Accessibility

Motor accessibility research explores interaction techniques for users experiencing:

- tremor
- reduced dexterity
- aging-related impairments
- neurological disorders
- temporary limitations

Many existing solutions rely on:

- larger targets
- slower interaction speeds
- input filtering
- operating system accessibility settings

Intent-Aware UI investigates whether interaction models themselves can contribute to reducing required precision.

---

# Adaptive Interfaces

Adaptive interfaces modify their behavior according to context.

Examples include adapting to:

- device capabilities
- screen size
- user preferences
- environmental conditions

Intent-Aware UI proposes extending this idea toward interaction itself.

Rather than adapting content or layout, it explores adapting the interaction process.

---

# Predictive Interaction

Several research areas investigate predicting user intent before actions are completed.

Examples include:

- predictive pointing
- trajectory prediction
- intent inference
- probabilistic interfaces

Intent prediction remains an active field of research.

Intent-Aware UI does not prescribe a specific prediction algorithm.

Any implementation should remain compatible with the core principles defined in the Specification.

---

# Accessibility Standards

Intent-Aware UI complements existing accessibility standards.

It does not replace them.

Relevant standards include:

- WCAG
- EN 301 549
- platform accessibility guidelines

Implementations should remain fully compliant with existing accessibility requirements.

---

# Open Questions

Several research questions raised by this document remain open. They are collected, expanded and organized by theme in [Open Questions](open-questions.md) rather than duplicated here.

---

# Related Work

This document intentionally stays at the level of scientific concepts and models (Fitts' Law, Steering Law, dynamic target acquisition, the Midas Touch problem) rather than naming specific products or prototypes. Named techniques (Bubble Cursor, Sticky/Magnetic Targets, Area Cursor, Semantic Pointing, Target Expansion, Predictive Pointing, adaptive menus, and others) are catalogued separately in [Prior Art](prior-art.md), so the two documents don't overlap.

---

# Bibliography

- Fitts, P. M. (1954). *The Information Capacity of the Human Motor System in Controlling the Amplitude of Movement.* Journal of Experimental Psychology, 47(6), 381–391.
- Jacob, R. J. K. (1990). *What You Look At is What You Get: Eye Movement-Based Interaction Techniques.* Proceedings of CHI 1990.
- Accot, J., & Zhai, S. (1997). *Beyond Fitts' Law: Models for Trajectory-Based HCI Tasks.* Proceedings of CHI 1997.
- Grossman, T., & Balakrishnan, R. (2005). *The Bubble Cursor: Enhancing Target Acquisition by Dynamic Resizing of the Cursor's Activation Area.* Proceedings of CHI 2005.
- Zhai, S., Conversy, S., Beaudouin-Lafon, M., & Guiard, Y. (2003). *Human On-line Response to Target Expansion.* Proceedings of CHI 2003.

This bibliography will grow as additional techniques are cited across the documentation. Every citation used in [Prior Art](prior-art.md) or elsewhere should have a corresponding entry here. Contributions are welcome.
