# Concept Map

> Vocabulary, Core Concepts and Principles are not the same thing. Here is how they relate, in one page.
>
> **Status:** Draft · **Version:** 0.1.0 · **Last Updated:** 2026-07-16

**[📚 Documentation Index](README.md)** · ← [Specification](specification.md) · [Design Principles](design-principles.md) →

Three layers, each answering a different question:

| Layer | Question it answers | Where it lives |
|---|---|---|
| Vocabulary | What does this word mean? | [Glossary](glossary.md) — a dictionary; core and supporting terms alike |
| Core Concepts | What are the paradigm's foundational concepts? | [Specification, Core Concepts](specification.md#core-concepts) — a frozen subset of 8 |
| Principles | What must every implementation guarantee? | [Specification §2](specification.md) — constraints on how those concepts behave, not concepts themselves |

```
Vocabulary
    │
    ▼
Core Concepts
    │
    ▼
Principles
```

A Core Concept is a noun. A Principle is a rule about that noun's behavior. Neither replaces the Glossary, which remains the single source of truth for what each term means.

---

# The chain, and what governs it

```
Intent                            Governed by
   │
   ▼
Intent Field
   │
   ▼
Confidence                        User Agency
   │                              Predictability
   ▼                              Accessibility by Design
Progressive Assistance            Reversibility
   │
   ▼
Activation
```

The five concepts on the left are the Interaction Lifecycle, in order (Specification §3). The four principles on the right constrain how every step in that chain is allowed to behave — they are not additional steps.

Two Core Concepts aren't shown as chain steps, because they aren't sequential: **Engagement Field** is a zone inside the Intent Field, not a separate step (§5). **Safe Zone** is a spacing rule between fields, not a lifecycle step (§11).

Two Specification principles aren't repeated on the right, because they'd be redundant: **Progressive Assistance** and **Explicit Activation** already name the "Progressive Assistance" and "Activation" steps directly on the left.

---

**[📚 Documentation Index](README.md)** · ← [Specification](specification.md) · [Design Principles](design-principles.md) →
