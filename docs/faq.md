# FAQ

> This FAQ is built around the questions a designer, developer or HCI researcher is likely to ask first — including the skeptical ones.
>
> **Status:** Draft · **Version:** 0.1.0 · **Last Updated:** 2026-07-16

**[📚 Documentation Index](README.md)** · ← [Accessibility](accessibility.md) · [Research](research.md) →

---

## Isn't this just Bubble Cursor?

No, but it is related, and that is expected.

Bubble Cursor (Grossman & Balakrishnan, 2005) dynamically expands the *cursor's* selection radius. Intent-Aware UI does not prescribe cursor manipulation at all — it proposes a broader interaction model built around Intent Detection, Confidence, Progressive Assistance and Activation, of which cursor adaptation is only one possible strategy among several.

See [Prior Art](prior-art.md) for a full technique-by-technique comparison.

---

## Why not simply make buttons bigger?

Enlarging targets remains one of the best-established ways to reduce acquisition time (Fitts, 1954), and Intent-Aware UI does not argue against it.

The project explores a different, complementary lever: adapting interaction *behavior* rather than layout — useful precisely when geometry can't be changed (dense toolbars, mobile UI, floating controls).

---

## Doesn't moving UI break muscle memory?

This is a real risk, and the [Specification](specification.md) and [Design Principles](design-principles.md) are written specifically to guard against it.

The Specification's Motion section requires movement to remain physically plausible and reversible, and states motion MUST NOT reduce precision. Design Principle 4 ("Movement Must Remain Minimal") and Principle 5 ("Preserve Spatial Memory") exist for exactly this reason: interactive elements should stay where users expect them to be.

---

## Why not just use operating system accessibility settings?

Those settings remain essential, and Intent-Aware UI does not replace them (see [Accessibility](accessibility.md#existing-accessibility-standards)).

The difference is that OS-level accessibility settings are typically an explicit mode a user opts into. [Accessibility](accessibility.md#motor-variability) starts from the observation that motor precision varies moment to moment for everyone, not only for users who have identified as needing an accessibility mode — so the project explores whether some of that adaptation can emerge from the interaction design itself.

---

## Does Intent-Aware UI rely on artificial intelligence?

Not necessarily. The [Specification](specification.md#15-implementation-freedom) deliberately does not prescribe a confidence algorithm — heuristics based on pointer distance, velocity, direction stability and dwell time are enough to implement the model described in the Specification.

---

## Does this require machine learning?

No. Machine learning models are explicitly listed as [out of scope](specification.md#16-out-of-scope) for this version of the specification. A future version may explore it, but the current model is defined independently of any particular estimation technique.

---

## Is this compatible with WCAG?

That's the intent. The Specification states implementations MUST NOT replace accessible sizing, keyboard navigation, screen reader support, focus management or existing accessibility standards (Section 14). [Accessibility](accessibility.md) frames the whole project as complementary to WCAG and EN 301 549, not a substitute for them.

---

## Can it be disabled?

The Specification doesn't mandate a global on/off switch in v0.1 — that's an implementation detail, not yet formalized. What *is* mandated is User Agency (Section 9): the interface must never trap the pointer, and the user must always be able to leave a target, change their mind, or reach another one. An implementation MAY expose a user preference or accessibility setting allowing assistance to be adjusted or disabled. Whether that should become a MUST in a future revision of the Specification is an open question.

---

## Isn't this just "magnetic buttons"?

That was one of the earliest ideas explored during the project's conception. The concept quickly evolved into a broader interaction model — Intent Field, Confidence, Assistance, Activation — that doesn't prescribe magnetism, translation, or any specific effect. Abrupt attraction ("Snap", see [Glossary](glossary.md)) is in fact discouraged in favor of progressive assistance.

---

## Doesn't this create unpredictable interfaces?

Predictability is treated as a non-negotiable principle, not an afterthought: it's one of the six core principles in the Specification (Section 2), the subject of Design Principle 2 ("Predictability Over Efficiency"), and its own Glossary entry. Assistance must remain proportional to confidence, transitions must stay smooth, and activation always requires explicit confirmation — the model is built to fail toward "nothing happens" rather than toward a surprising one.

---

## Isn't this over-engineering?

Possibly.

Intent-Aware UI deliberately explores a more expressive interaction model than traditional pointer-based interfaces.

Whether the additional complexity is justified depends on measurable outcomes such as reduced motor effort, improved acquisition accuracy, perceived comfort and user trust. The project therefore considers empirical evaluation essential before advocating widespread adoption — see [Roadmap](roadmap.md#phase-4--user-research).

---

## Why define a specification before building a prototype?

The project aims to explore an interaction paradigm rather than a single implementation.

Defining the vocabulary, principles and constraints first allows different implementations to be compared against the same conceptual model.

The prototype should validate the specification — not define it.

---

## Where should I go next?

- New to the project? Start with the [README](../README.md) and the [Manifesto](manifesto.md).
- Want the rules? Read the [Specification](specification.md).
- Want to know how it relates to existing work? Read [Prior Art](prior-art.md) and [Research](research.md).
- Have a question not covered here? Open a GitHub Discussion — see [Contributing](../CONTRIBUTING.md).
