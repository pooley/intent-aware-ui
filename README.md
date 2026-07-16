# Intent-Aware UI

> Interfaces should understand intent, not just clicks.

**Intent-Aware UI is an open research initiative exploring the future of human-computer interaction through intent-aware interfaces.**

Instead of waiting for a click to react, interfaces progressively interpret the user's intention and subtly assist the interaction while preserving predictability and control.

The objective is simple:

> Reduce the motor precision required to interact without reducing user agency.

---

## Why?

Modern interfaces continue to evolve toward:

- smaller targets
- denser layouts
- floating controls
- contextual actions
- multi-device interactions

While visually efficient, these interfaces increasingly demand motor precision.

Intent-Aware UI explores another direction:

Instead of making targets larger,
make interactions smarter.

---

## The Idea

Every interactive element owns an invisible **[Intent Field](docs/glossary.md#intent-field)**.

```
+------------------------------------+
|                                    |
|         Intent Field               |
|                                    |
|      +------------------+          |
|      | Engagement Field |          |
|      |    +--------+    |          |
|      |    | Button |    |          |
|      |    +--------+    |          |
|      +------------------+          |
|                                    |
+------------------------------------+
```

As pointer [confidence](docs/glossary.md#confidence) increases, the interface progressively adapts — entering the **[Engagement Field](docs/glossary.md#engagement-field)** allows stronger assistance while preserving predictability.

Not to take control.

To reduce effort.

---

## Core Principles

Intent-Aware UI is built around six principles, defined in full in the [Specification](docs/specification.md).

- User Agency
- Predictability
- Progressive Assistance
- Accessibility by Design
- Reversibility
- Explicit Activation

---

## Interaction Lifecycle

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

[Activation](docs/glossary.md#activation) is the confirmation of an already understood intention — see the full [Interaction Lifecycle](docs/specification.md#3-interaction-lifecycle) in the Specification.

---

## Why not simply enlarge buttons?

Increasing target size helps — it's one of the best-established results in [HCI research](docs/research.md#fitts-law).

Intent-Aware UI complements existing accessibility practices rather than replacing them.

Instead of changing layouts, it dynamically adapts interaction according to user intent. See the [FAQ](docs/faq.md) for more questions like this one.

---

## Accessibility

Human motor precision is never constant — it varies with age, fatigue, stress, illness, and even the input device in hand. See [Accessibility](docs/accessibility.md) for the full reasoning, including concrete cases from Parkinson's to simply carrying a child.

The goal is not to create a special accessibility mode.

The goal is to build interfaces that naturally require less precision.

---

## Status

The interaction model is defined: documentation is frozen at **v0.1.0**, pending a working prototype.

See the [Roadmap](docs/roadmap.md) for what comes next (visual identity, prototypes, reference implementation) and [Open Questions](docs/open-questions.md) for what remains genuinely unresolved.

Feedback and discussion are welcome.

---

## Documentation

Start with the **[Documentation Index](docs/README.md)** for reading paths suited to different readers (newcomer, designer, researcher, implementer, contributor).

| Document | Description |
|----------|-------------|
| [Manifesto](docs/manifesto.md) | Why current interaction models are reaching their limits |
| [Glossary](docs/glossary.md) | Official terminology reference |
| [Architecture](docs/architecture.md) | The whole concept, in one page |
| [Specification](docs/specification.md) | Definition of the interaction model |
| [Concept Map](docs/concept-map.md) | How vocabulary, core concepts and principles relate |
| [Design Principles](docs/design-principles.md) | Rules for designing intent-aware interfaces |
| [Accessibility](docs/accessibility.md) | Motor variability and inclusive design |
| [FAQ](docs/faq.md) | Common questions |
| [Research](docs/research.md) | Scientific background and references |
| [Prior Art](docs/prior-art.md) | Catalog of related existing techniques |
| [Roadmap](docs/roadmap.md) | Planned milestones |
| [Open Questions](docs/open-questions.md) | What the project intentionally doesn't answer yet |

The Manifesto argues *why* change is needed. The Specification defines *how*. Neither depends on the other.

---

## Vision

Intent-Aware UI is not a component library.

It is a proposal for a new interaction paradigm — see the [Manifesto](docs/manifesto.md) for why, and the [Architecture](docs/architecture.md) for how it all fits together.

Just as responsive design adapted interfaces to screen sizes,

Intent-Aware UI aims to adapt interactions to human intention.

---

## Contributing

The project is currently in its conceptual phase.

Discussions, critiques and research references are highly encouraged — see [CONTRIBUTING](CONTRIBUTING.md).

---

## License

MIT
