# To Do

Roadmap derived from the project's early concept discussions. The project is treated as an RFC-style research initiative rather than a quick component library, so documentation comes before implementation.

The repo distinguishes three things: **theory** (`docs/`), **implementations** (`examples/`, `prototypes/`) and **assets** (`assets/`). `examples/` shows how to use the system once it exists; `prototypes/` is where we explore ideas (confidence curves, field shapes, assistance models) before they're stable enough to become an example.

- [x] Scaffold the full repository tree (`docs/`, `examples/`, `assets/`, `prototypes/`, `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`, `CHANGELOG.md`)

**Doc-versioning convention:** every file in `docs/` (including `roadmap.md`, which carries the same version in its "Current Status" section) opens with `**Status:** Draft · **Version:** 0.1.0 · **Last Updated:** 2026-07-16` in its top blockquote — semver, to match the `[0.1.0]` tag already used in `CHANGELOG.md`. Bump these independently per document as each evolves — they track document maturity, not the project's overall version.

**Navigation convention:** every document in `docs/` (including `roadmap.md`, excluding the index itself) carries a one-line nav right after its status block: `**[📚 Documentation Index](README.md)** · ← [Prev](prev.md) · [Next](next.md) →`. The canonical reading order is grouped — Foundation (Manifesto → Glossary → Architecture → Specification) → Guidance (Design Principles → Accessibility → FAQ) → Background (Research → Prior Art) → Project (Roadmap → Open Questions) — see `docs/README.md` for the full index and profile-based reading paths. File names stay unprefixed; numbering is conceptual, shown only in `docs/README.md`.

**Research vs. Prior Art, division of labor:** `research.md` stays at the level of scientific concepts and models (Fitts' Law, Steering Law, the Midas Touch problem, dynamic target acquisition as a general notion) and never names a specific product or prototype. `prior-art.md` is where named techniques (Bubble Cursor, Sticky Targets, Semantic Pointing, Target Expansion, etc.) live, each compared against Intent-Aware UI. Research still comes first in reading order only because Prior Art cites its Bibliography — the two are otherwise peers, not a hierarchy.

**Posture shift from `research.md` onward:** the Manifesto, Specification and Design Principles state the project's own ideas. Starting with Research, the tone changes to state-of-the-art only — no claims, no invention. Use hedged verbs (*explores, investigates, proposes, hypothesizes, aims to, may, could, seeks to*) instead of asserting unproven effects (*extends, improves, reduces*) whenever "Intent-Aware UI" is the subject. Frame the project as an *original synthesis built upon existing HCI research*, never as inventing adaptive/assisted interaction from scratch — every named prior technique gets a real citation (added to `research.md`'s Bibliography), never a vague or invented one.

---

## Phase 1 — Documentation ✅ complete

Each sub-phase builds on the previous one — later documents reference earlier ones instead of redefining terms.

### 1a. Foundation

- [x] `README.md` — concept pitch, "open research initiative" positioning, core principles, interaction model, documentation index
- [x] `LICENSE` — MIT
- [x] `docs/manifesto.md` — authored by the project owner
  - Convinces the reader a problem exists (precision as hidden cost, non-constant human capability, click-as-only-certainty, accessibility as exceptional rather than intrinsic) without naming use cases or mechanics
  - Closes on a "We believe" statement of values, in the spirit of a founding text
- [x] `docs/glossary.md` — authored by the project owner
  - Single source of truth for normative, operational terms only: Activation, Assistance, Confidence, Confidence Curve, Engagement Field, Intent, Intent Detection, Intent Field, Intent Ownership, Interaction Model, Predictability, Progressive Assistance, Safe Zone, Snap, Target, Target Acquisition, User Agency, Visual Feedback
  - Every other document links here instead of redefining a term
  - **Awareness** is deliberately excluded — it names the paradigm's philosophy, not an operational concept, so it stays in README / Manifesto / the Specification's introduction only
  - Deliberately deferred: **Intent Score** (only if it turns out to be distinct from Confidence) and **Motor Profile** (would be an extension of the paradigm, not its core) — to surface naturally while writing the specification

### 1b. Core

- [x] `docs/specification.md` — the central, normative document, v0.1 Draft
  - 17 sections: Purpose, Principles, Interaction Lifecycle, Intent Field, Engagement Field, Confidence, Assistance, Activation, User Agency, Intent Ownership, Safe Zones, Visual Feedback, Motion, Accessibility, Implementation Freedom, Out of Scope, Compliance
  - Written in normative language (MUST / SHOULD / MAY), defined in its own "Conformance Language" section rather than by citing RFC 2119 — keeps the project's vocabulary self-contained
  - Deliberately stays a "constitution" (rules, not implementations) — algorithms, curves and heuristics belong in later, separate documents
  - Links to `glossary.md` instead of redefining terms
  - Section 9 (User Agency) now includes: "When behavior is ambiguous, an implementation MUST fail toward inaction rather than unintended action" — promoted from a FAQ answer into a normative rule
  - Redundant trailing "# Version" section removed now that Status/Version/Last Updated lives in the top blockquote (see doc-versioning convention below)

### 1c. Rules

- [x] `docs/design-principles.md` — 13 principles + summary
  - DO / DON'T guidance building on the Specification: assistance vs. automation, predictability over efficiency, progressive confidence, minimal movement, spatial memory, one-intent-one-target, safe zones, explanatory feedback, never fighting the user, accessibility as default, visual calm, respect for existing standards, design for trust

### 1d. Research

- [x] `docs/research.md` — state-of-the-art only, no claims, no named products
  - Covers: HCI framing, Fitts' Law, Steering Law, Dynamic Target Acquisition (generic notion, no product names), the Midas Touch problem, Motor Accessibility, Adaptive Interfaces, Predictive Interaction, Accessibility Standards
  - Written entirely in hedged language (see posture-shift note above); points to `prior-art.md` for named techniques and to `open-questions.md` for open research questions instead of duplicating either
  - **Revised:** the former "Bubble Cursor" and "Sticky Targets" sections were merged into one generic "Dynamic Target Acquisition" section — those product names now live solely in `prior-art.md`, per the Research/Prior-Art division of labor above

### 1e. Prior Art

- [x] `docs/prior-art.md` — protects the project's credibility
  - Per-technique similarity/difference comparison: Bubble Cursor, Sticky Targets, Semantic Pointing, Target Expansion, Adaptive Menus, Eye Tracking Research, Predictive Pointing, Motor Accessibility Research
  - Closes with "What Intent-Aware UI Adds" (Intent Detection, Confidence, Progressive Assistance, Activation) so a "this looks like X" issue can be answered by linking here
  - Explicitly disclaims inventing assisted interaction ex nihilo
  - Cited so far: Bubble Cursor (Grossman & Balakrishnan, 2005), Target Expansion (Zhai et al., 2003) — cross-referenced in `research.md`'s Bibliography
  - **Still needs real citations**: Sticky Targets, Semantic Pointing, Adaptive Menus, Eye Tracking Research, Predictive Pointing — add only once a verified reference is found, per the posture note above
  - **Revised:** dropped its own "Fitts' Law" section (duplicated `research.md`); "Explicit Activation" renamed to "Activation" to match the Core Concepts list

### 1f. Accessibility

- [x] `docs/accessibility.md` — reframed around **Motor Variability**
  - Central thread: human motor ability is never constant (age, fatigue, stress, illness, medication, input device, environment) — avoids framing accessibility as "us" (able users) vs. "them" (a special-needs minority)
  - Sections: Motor Variability, Accessibility Benefits Everyone, Accessibility Is Not a Mode, Existing Accessibility Standards, Motor Impairments, Temporary Limitations, User Agency, Predictability, Accessibility by Design, Research Not Replacement, Looking Forward
  - Concrete cases (Parkinson's, essential tremor, temporary limitations like carrying a child) appear only as illustrations of the broader thread, not as the document's framing
  - Complements (never replaces) WCAG / EN 301 549 / platform accessibility APIs
  - (Deliberately absent from the manifesto, which stays universal)

### 1g. Remaining docs

- [x] `docs/roadmap.md` — authored by the project owner
  - 7 phases (Foundation → Visual Language → Interactive Prototypes → User Research → Reference Implementation → Design System Integration → Platform Exploration) plus Future Research and Community sections
  - Phase 1 (Foundation) checked off, mirroring this file's own Phase 1 status
- [x] `docs/faq.md` — pre-empts the objections the project will actually get
  - Answers 12 anticipated questions (Bubble Cursor, bigger buttons, muscle memory, OS accessibility settings, AI/ML, WCAG, opt-out, "magnetic buttons", predictability, over-engineering, spec-before-prototype) by linking back to Specification / Design Principles / Prior Art / Accessibility / Glossary rather than re-arguing them
  - No internal-only references (e.g. `conv.md`) — anything a public reader can't open gets rephrased instead of linked
- [x] `CODE_OF_CONDUCT.md`
- [x] `CONTRIBUTING.md` — contribution rules for a conceptual-phase project: discussions, critiques, research references welcome
- [x] `SECURITY.md` — documentation-only for now; points to GitHub private vulnerability reporting once implementations exist
- [x] `CHANGELOG.md` — tracks concept/documentation maturity (not a package release)
- [x] `docs/open-questions.md` — intellectual honesty as a feature
  - Organized by theme: Interaction, Motion, Intent Fields, Accessibility, Evaluation, Platform Support
  - `research.md`'s own "Open Questions" section now just points here instead of duplicating a shorter list — single source of truth, same pattern as Glossary/Prior Art

### 1h. Navigation

- [x] `docs/architecture.md` — the whole concept on one page
  - Single ASCII diagram: Principles / Specification / Research converge on the Interaction Model, which unfolds Intent Field → Confidence → Progressive Assistance → Activation
  - Inserted into the reading order right after Glossary (needs its vocabulary) and before Specification (which it bridges into) — this pushed the doc count from 10 to 11
  - Not a software architecture doc — explicitly defers to Specification §15 for implementation freedom
- [x] `docs/README.md` — the documentation hub (also what GitHub shows by default when browsing the `docs/` folder)
  - Profile-based reading paths (newcomer, interaction-model reader, research reader, implementer, contributor) plus a conceptually-numbered 01–11 full index, grouped into **Foundation / Guidance / Background / Project**
  - File names stay unprefixed on purpose — numbering lives only in this index, per the project owner's note that GitHub directory listings shouldn't be cluttered with `01-...md`
  - Groups per the project owner: Foundation (01–04: Manifesto, Glossary, Architecture, Specification), Guidance (05–07: Design Principles, Accessibility, FAQ), Background (08–09: Research, Prior Art), Project (10–11: Roadmap, Open Questions)
- [x] Per-document prev/next nav added to all 11 docs (`**[📚 Documentation Index](README.md)** · ← Prev · Next →`), right after each doc's status block — updated when Accessibility/FAQ and Research/Prior Art swapped position for the group reshuffle
- [x] Root `README.md` Documentation table: rows now hyperlink to `docs/*.md`, Architecture row added, links to the new `docs/README.md` index
- [x] `docs/specification.md` — new unnumbered **Core Concepts** section (right after Conformance Language, before §1, so the existing 17 section numbers don't shift): the 8 concepts are frozen — Intent, Intent Field, Engagement Field, Confidence, Progressive Assistance, Safe Zone, Activation, User Agency. A 9th requires strong justification, not convenience
  - `docs/glossary.md` marks the matching 8 entries with **★ Core Concept** and links back to this section; everything else in the glossary is supporting vocabulary, free to grow

## Consistency pass & fact-check (before Phase 2)

Full re-read of all 14 docs, cross-references and citations. Citations verified by web search: Fitts (1954), Accot & Zhai (1997), Grossman & Balakrishnan (2005), Zhai et al. (2003) — all accurate.

Fixed:
- [x] Root `README.md` Documentation table still had the pre-reshuffle order — reordered to match Foundation/Guidance/Background/Project
- [x] `docs/architecture.md` cited "Interaction Model (Specification §3)" and "Progressive Assistance (Specification §7)" — §3 is actually titled "Interaction Lifecycle" and §7 "Assistance"; fixed the prose, the diagram box, and the table
- [x] `docs/specification.md`'s Core Concepts note claimed Open Questions lists "candidates" for a 9th concept — it doesn't; removed the overclaim
- [x] "The Midas Touch Problem" was stated as fact in `research.md`/`prior-art.md`/`open-questions.md` with **no citation**, unlike Fitts'/Steering Law, violating the Bibliography's own rule. Verified origin (Jacob, 1990, CHI '90) and added it to `research.md`'s Bibliography
- [x] `docs/roadmap.md`'s Phase 1 Goals checklist predated Architecture/FAQ/Open Questions and didn't list them as done — added
- [x] `CONTRIBUTING.md` had its own 7-step "Roadmap" section that duplicated and had drifted from `docs/roadmap.md` (missing Glossary, Architecture, Prior Art, FAQ, Open Questions entirely) — replaced with a pointer to `docs/roadmap.md`

Resolved (project owner's call): the three lists — Glossary (Vocabulary: "what does this word mean?"), Specification Core Concepts (a frozen 8-item subset: "what are the foundational concepts?"), Specification §2 Principles (6 behavioral constraints: "what must every implementation guarantee?") — are **not** to be merged; they answer different questions and form a natural hierarchy (Vocabulary → Core Concepts → Principles). Instead they're now explicitly cross-referenced:
- [x] `docs/specification.md`: Core Concepts now opens with "defined in the Glossary and form the conceptual foundation"; §2 Principles now opens with "define how the Core Concepts above must behave"
- [x] `docs/glossary.md` already pointed to Specification's Core Concepts (no change needed)
- [x] `docs/concept-map.md` — new one-pager visualizing the hierarchy: the 5-step concept chain (Intent → Intent Field → Confidence → Progressive Assistance → Activation, i.e. the Interaction Lifecycle) alongside the 4 principles that govern it (User Agency, Predictability, Accessibility by Design, Reversibility); explicitly notes why Engagement Field/Safe Zone aren't chain steps and why Progressive Assistance/Explicit Activation aren't repeated on the governing side
  - Inserted into Foundation at position 05 (after Specification, before Design Principles) — doc count is now 12; nav chain and both indexes updated accordingly

**Midas Touch refinement (post-freeze correction, not new scope):** the project owner corrected the framing — Jacob's gaze-based origin is real, but the *problem itself* is general (any implicit interaction can exhibit it), and it shouldn't read as "prior art we drew from." Applied:
- [x] `docs/research.md` — reworded to state the gaze-based origin explicitly, then generalize, then explain why Explicit Activation exists because of it
- [x] `docs/specification.md` §8 (Activation) — added an explicit MUST: "avoid introducing a Midas Touch effect," elevating it from background research to a named anti-pattern the spec itself guards against
- [x] `docs/glossary.md` — new **M** section, "Midas Touch Problem" (supporting term, not a Core Concept — it's a risk/anti-pattern, not one of the frozen 8)
- [x] `docs/prior-art.md`'s "Eye Tracking Research" entry reworded to say gaze interaction is where the term was *first identified*, not that it's an eye-tracking-specific concept, and links to the new Glossary entry

**Documentation frozen at v0.1.** Per the project owner: no further spec/doc changes until a prototype exists and produces real feedback (expect ~10-15% of the Specification to change after that — normal for a concept → implementation → refinement cycle). Next work is Phase 2 (assets) then Phase 3 (first HTML/CSS/JS prototype); the spec is revisited only after that, informed by what building it actually revealed.

## Pre-push QA pass (2026-07-16)

Before the first public push. All checks performed, not assumed:

- [x] Every link in root `README.md` (13 targets) verified to resolve to an existing file
- [x] Every internal link across all of `docs/` + root files programmatically checked (path + anchor) — 0 broken, except two literal `ToDo.md`-only issues below
- [x] All 11 anchor links (`file.md#slug`) verified against actual heading text and GitHub's slug algorithm (including the em-dash edge case in `roadmap.md#phase-4--user-research`) — all correct
- [x] Terminology casing swept for "Intent Field", "Engagement Field", "User Agency", "Safe Zone", "Core Concept(s)", "Intent-Aware UI" — zero inconsistent variants found; lowercase "user agency" in README/Specification §1/Accessibility is a deliberate recurring rhetorical phrase, not a slip
- [x] `ToDo.md` linked to `conv.md`, which the project owner has since deleted from disk (and removed from `.gitignore`) ahead of the push — fixed the dead link and the self-contradiction (ToDo.md's own rule says internal-only files shouldn't be linked)
- [x] Version headers standardized: every doc said `Version: 0.1`, while `CHANGELOG.md` already used the `[0.1.0]` tag — bumped all 12 docs (11 blockquotes + `roadmap.md`'s "Current Status") to `0.1.0` to match

**Flagged for the project owner, not acted on:**
- `.gitignore` is now empty (the `./conv.md` line was removed along with the file). The untracked `.claude/settings.json` (local tool permissions, not project content) will get swept into a `git add -A` unless re-ignored — worth deciding before staging.
- `origin` remote is `github.com/pooley/intent-aware-ui`; current branch is `develop` (a `main` branch also exists) — confirm that's the intended push target.

## Root README refresh (post-push, 2026-07-16)

The project owner flagged the root `README.md` as outdated — it predated the terminology freeze and the Motor Variability reframe. Fixed:

- [x] "Core Principles" was a casual 7-bullet paraphrase that didn't match Specification §2 (6 named principles, missing Reversibility entirely) — replaced with the actual 6, linked to the Specification
- [x] "Interaction Model" heading/diagram used the pre-freeze step names ("Pointer movement", "Click confirmation", "Action") and the wrong term — this is the **Interaction Lifecycle** (Specification §3); "Interaction Model" is a different, broader Glossary term. Retitled and aligned the diagram to the spec's actual steps
- [x] "Accessibility" section still listed conditions (Parkinson's, Essential tremor, etc.) as its framing — the exact "us vs. them" framing the Manifesto and `docs/accessibility.md` deliberately moved away from. Replaced with the Motor Variability framing and a link out
- [x] "Status" section said the interaction model was "being defined" — stale now that it's frozen at v0.1.0; updated to point at Roadmap/Open Questions
- [x] Added inline links throughout (Intent Field, Confidence, Engagement Field, Activation, Interaction Lifecycle, Fitts' Law, Manifesto, Architecture, CONTRIBUTING) per the project owner's request while already editing

**Bug caught and fixed at the source:** the 8 "★ Core Concept" glossary headings (e.g. `## Intent Field — ★ Core Concept`) produced fragile, ugly GitHub anchors (`#intent-field---core-concept`, triple-hyphen from the stripped em-dash and star) — almost shipped broken anchors in the README before catching it. Moved the `★ **Core Concept**` badge out of the heading and onto its own line below, so anchors are back to simple `#intent-field`, `#confidence`, etc. `docs/glossary.md`'s intro sentence still describes the marking accurately, no change needed there.

## Phase 2 — Visual identity

Diagram priority per the project owner: model diagrams first (they're what will actually stress-test the spec), branding last.

- [ ] `assets/interaction-model.svg` — diagram of the Detect → Predict → Assist → Confirm → Activate flow
- [ ] `assets/intent-field.svg` — diagram of the two-layer field model (Intent Field / Engagement Field)
- [ ] `assets/confidence-curve.svg` — diagram of the confidence falloff curve
- [ ] `assets/safe-zone.svg` — diagram of the non-overlapping safe-zone/exclusivity rule
- [ ] `assets/interaction-lifecycle.svg` — diagram of the Idle → Intent Detection → Confidence Estimation → Progressive Assistance → Activation → Completed lifecycle (Specification §3)
- [ ] `assets/logo.svg`
- [ ] Optional short animation/GIF demonstrating glow intensity + micro-attraction + scale-up

## Phase 3 — Prototypes & examples

- [ ] `prototypes/v0/` — first exploratory build: confidence formula, field falloff, assistance behaviour
- [ ] `prototypes/playground/` — sandbox for comparing alternative curves/fields/models side by side
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

## Deferred idea — `docs/principles/` (post-v0.1, not scheduled)

Not to be started now — captured so it isn't lost.

A future `docs/principles/` folder, one file per concept, each with 2–3 pages of explanation, diagrams, counter-examples, edge cases and recommendations: `agency.md`, `confidence.md`, `intent.md`, `predictability.md`, `safe-zones.md`, `progressive-assistance.md`.

Rationale: `specification.md` stays deliberately short and normative (the rules); `principles/` would carry the *why* behind each rule, letting the paradigm mature without bloating the core documents.

---

## Open questions to resolve while writing the spec

- [ ] Exact confidence formula (inputs: distance, velocity, direction stability, dwell time)
- [ ] Falloff curve for the Intent Field (exponential vs. linear)
- [ ] How Intent Fields partition the viewport when targets are close (Voronoi-like exclusivity)
- [ ] Default numeric ranges: max translation (2–8px), max scale (1.03–1.08), safe gap between targets
