# Changelog

All notable changes to the Intent-Aware UI concept and documentation are tracked here.

The format follows [Keep a Changelog](https://keepachangelog.com/). Versions track the maturity of the concept and documentation, not a released package.

## [Unreleased]

### Added

- Project scaffolding: `docs/`, `examples/`, `assets/`, `prototypes/`
- Glossary of normative terminology
- Code of Conduct, Contributing guide, Security policy
- Specification v0.1 (Draft)
- Design Principles
- Research (state-of-the-art references, no claims), now with a formal Bibliography
- Prior Art (technique-by-technique comparison), partially cited
- Accessibility, reframed around Motor Variability
- Roadmap
- FAQ
- Open Questions, organized by theme (Interaction, Motion, Intent Fields, Accessibility, Evaluation, Platform Support)
- Architecture: single-page conceptual diagram (Principles / Specification / Research → Interaction Lifecycle → Intent Field → Confidence → Progressive Assistance → Activation)
- `docs/README.md`: documentation hub with profile-based reading paths and a full numbered index
- Per-document prev/next navigation across all of `docs/`
- Concept Map: one-page hierarchy (Vocabulary → Core Concepts → Principles) with the 5-step concept chain and the 4 principles governing it
- Phase 1 (Documentation) complete: README, Manifesto, Glossary, Architecture, Specification, Concept Map, Design Principles, Research, Prior Art, Accessibility, FAQ, Roadmap, Open Questions

### Changed

- FAQ: reworded the "magnetic buttons" answer to drop the internal `conv.md` reference, retitled "Is this AI?", clarified the opt-out answer, added "Isn't this over-engineering?" and "Why a specification before a prototype?"
- Specification: added a fail-toward-inaction rule to User Agency (Section 9); removed the now-redundant trailing Version section
- Added a `Status / Version / Last Updated` header to every doc in `docs/` (except Roadmap, which has its own status section)
- Research: "Open Questions" section now points to the dedicated `open-questions.md` instead of duplicating a shorter list
- Root README: Documentation table rows are now links; added an Architecture row and a pointer to the new `docs/README.md` index
- Reordered the canonical reading order into four named groups: Foundation, Guidance (Design Principles, Accessibility, FAQ), Background (Research, Prior Art), Project — updated all affected prev/next nav lines and `docs/README.md`'s index accordingly
- Research: removed the "Bubble Cursor" and "Sticky Targets" sections (merged into one generic "Dynamic Target Acquisition" section); named techniques now live only in Prior Art
- Prior Art: removed the "Fitts' Law" section, now covered only in Research; "Explicit Activation" renamed to "Activation" for consistency with the new Core Concepts list
- Specification: added a frozen **Core Concepts** list (Intent, Intent Field, Engagement Field, Confidence, Progressive Assistance, Safe Zone, Activation, User Agency)
- Glossary: tagged the 8 matching entries **★ Core Concept**
- Specification: Core Concepts and §2 Principles now explicitly cross-reference the Glossary and each other instead of standing alone

### Fixed

- Full documentation consistency pass and citation fact-check (all 4 existing citations verified accurate via web search)
- Root README: Documentation table reordered to match the Foundation/Guidance/Background/Project grouping
- Architecture: corrected two section references (§3 is "Interaction Lifecycle", §7 is "Assistance", not "Interaction Model"/"Progressive Assistance")
- Specification: removed an inaccurate claim that Open Questions lists candidate 9th core concepts
- Research: added a missing citation for the Midas Touch Problem (Jacob, 1990) — previously stated as fact with no source
- Roadmap: Phase 1 checklist now lists Architecture, FAQ and Open Questions as done
- Contributing: removed a stale, duplicated mini-roadmap in favor of linking to `docs/roadmap.md`

### Changed (post-freeze correction)

- Research: reworded the Midas Touch Problem section — states the gaze-based origin (Jacob, 1990) explicitly, then generalizes it beyond eye tracking
- Specification: §8 (Activation) now explicitly names avoiding a Midas Touch effect as a MUST, not just an implied consequence
- Glossary: added a "Midas Touch Problem" entry (supporting term)
- Prior Art: reworded the Eye Tracking Research entry so gaze interaction reads as where the term was first identified, not as its defining domain

### Fixed (pre-push QA pass)

- All internal links and anchors across every doc programmatically verified (0 broken)
- Terminology casing swept ("Intent Field", "Engagement Field", "User Agency", "Safe Zone", "Core Concept(s)", "Intent-Aware UI") — no inconsistent variants found
- ToDo.md: fixed a dead link to `conv.md` (removed from the repo ahead of the public push) that also violated its own "no internal-only references" rule
- Standardized every doc's version header from `0.1` to `0.1.0`, matching the `[0.1.0]` tag already used in this file

### Fixed (root README refresh, post-push)

- "Core Principles" now matches the Specification's actual 6 principles (was a stale 7-item paraphrase missing Reversibility); "Interaction Model" renamed to "Interaction Lifecycle" with the correct step names; "Accessibility" section reframed around Motor Variability instead of a condition list; "Status" section updated to reflect the v0.1.0 freeze
- Added inline links to Glossary/Specification/Manifesto/Architecture/Research/FAQ/CONTRIBUTING throughout
- Glossary: moved the "★ Core Concept" badge from the heading line to the line below, on all 8 entries — the old `## Term — ★ Core Concept` heading produced a broken, triple-hyphenated GitHub anchor instead of the expected `#term`

---

**Documentation frozen at v0.1.0.** No further spec/doc changes planned until a working prototype produces real feedback.

## [0.1.0] - 2026-07-16

### Added

- Initial README and project positioning
- Manifesto
