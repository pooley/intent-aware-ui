# Intent-Aware UI

> Interfaces should understand intent, not just clicks.

Intent-Aware UI is an interaction paradigm that introduces **intent-aware targets**.

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

Every interactive element owns an invisible **Intent Field**.

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

As pointer confidence increases, the interface progressively adapts.

Not to take control.

To reduce effort.

---

## Core Principles

Intent-Aware UI is built around a few principles.

- Intent before action
- Progressive assistance
- Predictable interactions
- No surprise behaviours
- User always remains in control
- Accessibility by design
- Assistance should remain subtle

---

## Interaction Model

```
Pointer movement

↓

Intent detection

↓

Confidence estimation

↓

Progressive assistance

↓

Click confirmation

↓

Action
```

The click becomes the confirmation of an already understood intention.

---

## Why not simply enlarge buttons?

Increasing target size helps.

Intent-Aware UI complements existing accessibility practices rather than replacing them.

Instead of changing layouts, it dynamically adapts interaction according to user intent.

---

## Accessibility

Intent-Aware UI has the potential to improve interactions for users experiencing:

- Parkinson's disease
- Essential tremor
- Age-related motor decline
- Temporary motor impairments
- High-density professional interfaces
- Trackpad fatigue

The goal is not to create a special accessibility mode.

The goal is to build interfaces that naturally require less precision.

---

## Status

⚠️ This project is currently a research initiative.

The interaction model is being defined before any implementation.

Feedback and discussion are welcome.

---

## Documentation

| Document | Description |
|----------|-------------|
| Manifesto | Why interaction models should evolve |
| Specification | Definition of the interaction model |
| Design Principles | Rules for designing intent-aware interfaces |
| Accessibility | Motor accessibility considerations |
| Research | Scientific background and references |
| FAQ | Common questions |
| Roadmap | Planned milestones |

---

## Vision

Intent-Aware UI is not a component library.

It is a proposal for a new interaction paradigm.

Just as responsive design adapted interfaces to screen sizes,

Intent-Aware UI aims to adapt interactions to human intention.

---

## Contributing

The project is currently in its conceptual phase.

Discussions, critiques and research references are highly encouraged.

---

## License

MIT
