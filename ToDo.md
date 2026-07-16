# To Do

Roadmap derived from the concept discussion in [conv.md](conv.md). The project is treated as an RFC-style research initiative rather than a quick component library, so documentation comes before implementation.

---

## Phase 1 — Documentation

- [x] `README.md` — concept pitch, core principles, interaction model, documentation index
- [x] `LICENSE` — MIT
- [ ] `CODE_OF_CONDUCT.md`
- [ ] `CONTRIBUTING.md`
  - Contribution rules for a conceptual-phase project: discussions, critiques, research references welcome
- [ ] `docs/manifesto.md`
  - Why current interfaces are hitting their limits: Fitts' Law, UI densification, aging population, motor fatigue
  - Why "click" is a 40-year-old interaction model
- [ ] `docs/specification.md` — the normative document
  - Define: Intent Field, Engagement Field, Confidence (0–1 scale), Assistance, Activation, Safe Zone, Intent Ownership, Conflict Resolution
  - Precise enough that an independent implementation is possible
- [ ] `docs/design-principles.md`
  - DO / DON'T list, e.g.:
    - A target must never travel more than ~8px
    - Two Intent Fields must never overlap
    - The user must never lose control of the pointer
- [ ] `docs/accessibility.md`
  - How the paradigm complements (not replaces) existing accessibility practices (RGAA, WCAG)
  - Impact for Parkinson's, essential tremor, age-related motor decline, trackpad fatigue
- [ ] `docs/research.md`
  - Scientific background: Fitts' Law, Steering Law, Hick's Law, Midas touch problem, relevant HCI papers
- [ ] `docs/faq.md`
- [ ] `docs/roadmap.md`
  - Public version of this file's phases

## Phase 2 — Visual identity

- [ ] `assets/logo.svg`
- [ ] `assets/intent-field.svg` — diagram of the two-layer field model (Intent Field / Engagement Field)
- [ ] `assets/interaction-model.svg` — diagram of the Detect → Predict → Assist → Confirm → Activate flow
- [ ] Optional short animation/GIF demonstrating glow intensity + micro-attraction + scale-up

## Phase 3 — First prototype (HTML/CSS/JS)

- [ ] `examples/basic-button/` — single button demonstrating glow + micro movement + scale
- [ ] `examples/toolbar/` — dense controls, tests non-overlapping Intent Fields
- [ ] `examples/dense-ui/` — compact layout stress test
- [ ] `examples/motor-accessibility/` — scenario tuned for reduced-precision / tremor use case
- [ ] Instrumentation to measure: acquisition time, error rate, trajectory corrections, perceived fatigue

## Phase 4 — NPM package

- [ ] Scaffold `@intent-aware/core`
- [ ] `IntentField` primitive (wraps any interactive element, not just buttons — "Target Aware")
- [ ] `IntentButton` as a convenience wrapper over `IntentField`
- [ ] Expose configuration primitives: `assist-strength`, `magnetic-radius`, `snap-threshold`, `tremor-filter`
- [ ] Conflict resolution logic for adjacent targets (trajectory/velocity/angle/dwell-time weighting)

## Phase 5 — Public presentation

- [ ] Write an article (Medium / Dev.to / LinkedIn) introducing the concept
- [ ] Publish the repo publicly and gather feedback from HCI/accessibility/dev communities

---

## Open questions to resolve while writing the spec

- [ ] Exact confidence formula (inputs: distance, velocity, direction stability, dwell time)
- [ ] Falloff curve for the Intent Field (exponential vs. linear)
- [ ] How Intent Fields partition the viewport when targets are close (Voronoi-like exclusivity)
- [ ] Default numeric ranges: max translation (2–8px), max scale (1.03–1.08), safe gap between targets
