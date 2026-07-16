# Architecture

> The conceptual architecture of Intent-Aware UI, in one page.
>
> **Status:** Draft · **Version:** 0.1.0 · **Last Updated:** 2026-07-16

**[📚 Documentation Index](README.md)** · ← [Glossary](glossary.md) · [Specification](specification.md) →

This is not a software architecture. There is no prescribed runtime, module boundary or file structure — that is intentionally left to implementations (Specification §15, Implementation Freedom).

This is the conceptual architecture: how the project's own ideas relate to each other.

---

```
                              Intent-Aware UI
                                     │
                 ┌───────────────────┼───────────────────┐
                 │                   │                   │
            Principles         Specification          Research
                 │                   │                   │
                 └───────────────────┼───────────────────┘
                                     │
                          Interaction Lifecycle
                                     │
                              Intent Field
                                     │
                               Confidence
                                     │
                       Progressive Assistance
                                     │
                                Activation
```

---

# Reading the diagram

The three top-level pillars each answer a different question, and each is its own document:

| Pillar | Question it answers | Document |
|---|---|---|
| Principles | How should this be designed? | [Design Principles](design-principles.md) |
| Specification | What is this, exactly? | [Specification](specification.md) |
| Research | What is this built on? | [Research](research.md) · [Prior Art](prior-art.md) |

All three converge on a single **Interaction Lifecycle** (Specification §3), which unfolds as a chain of concepts, each defined once in the [Glossary](glossary.md) and made normative in the Specification:

- **Intent Field** — where estimation begins (Specification §4)
- **Confidence** — the continuous signal derived from it (Specification §6)
- **Progressive Assistance** — what confidence is allowed to trigger (Specification §7, "Assistance")
- **Activation** — the only point where an action actually occurs, always by explicit confirmation (Specification §8)

Nothing above Activation ever performs an action by itself. That single constraint is the throughline of the entire architecture.

---

**[📚 Documentation Index](README.md)** · ← [Glossary](glossary.md) · [Specification](specification.md) →
