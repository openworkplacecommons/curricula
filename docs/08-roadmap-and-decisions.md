# Design Decisions, Next Milestones and Open Questions

**Updated: 29 October 2026. All work below is proposed, not completed.**

## Agreed directions

- **Identity:** Open Workplace Commons (OWC); domain `openworkplacecommons.org` was purchased.
- **Repositories:** `openworkplacecommons/curricula` is canonical public content; `openworkplacecommons/portal` is the community-facing application.
- **Scope:** public curricula, materials, public practice questions/answers, nonbinding evaluation guidance. No centrally issued OWC credentials/exams.
- **Independence:** third-party content authors, LMSs and training organizations can import/adapt OWC content through neutral formats, regardless of our products.
- **Contribution model:** GitHub for technical contributors and an eventual friendly portal submission interface for nontechnical contributors; publication requires review.

## Proposed MVP phases

| Phase | Deliverable | Exit condition |
|---|---|---|
| 0 — Spec review | Principles, content model, format, boundaries, initial examples | Maintainers accept a v0.1 proposal after comments; all open decisions recorded. |
| 1 — Seed content | Three **draft** course manifests and one readable starter lesson/practice set | All required metadata validates; rights and status clear. |
| 2 — Validation | JSON schemas, reference/ID validators and CI | A deliberate invalid example fails; valid examples pass. |
| 3 — Portal read-only | Curriculum catalogue and course/lesson view sourced from release | Content can be rendered without copying/editing the canonical source. |
| 4 — Contributions | Simple lesson correction/question submission form + moderation | A nontechnical submission reaches a review queue and can be turned into an approved PR. |
| 5 — Independent integration | HTML export, sample SCORM or JSON consumer, tested with third-party LMS | At least one actual outside consumer can use the same source. |

## First proposed courses

1. Responsible AI at Work — examples, confidential information, verification, human oversight.
2. Cybersecurity Awareness — phishing, authentication, safe sharing and incident reporting.
3. Data Privacy Essentials — handling personal data, minimization, sharing and incident response.

No content above should be called expert-reviewed until an independent qualified review occurs.

## Definition of design-ready

- Canonical content schema and sample course can be understood by a nontechnical educator and parsed by a second independent implementation.
- Stable IDs, schema/content versions, localization, license/provenance and competency relationships are explicit.
- Contributions can be reviewed without silently changing published resources.
- A practice question and public evaluation guide can be exported without requiring any OWC exam infrastructure.
- One distribution route works with a third-party platform without using any of our EdTech products.
- The portal remains a replaceable renderer/editor, not the source of truth.

## Unresolved decisions

- Which fields are mandatory for **draft** vs **reviewed** content? Are short human names separate from immutable IDs?
- The exact syntax/version of JSON Schema and extension namespaces.
- Whether reusable competencies and practice questions can live outside a course in v0.1.
- Which simple question types belong in the core (single choice, multiple select, true/false, scenario rubric)?
- Final content/software licenses and contributor IP attestations.
- Reviewer roles, thresholds and escalation policy; review frequency for legal/privacy/security topics.
- Language/translation source-revision mapping and organization overlays.
- The first integration test: plain HTML export vs SCORM prototype vs independent JSON consumer.
- Wiki role: mirror/navigation only or independently editable general guidance. Avoid two competing authoritative specifications.

## Next concrete action

Review and accept this design through a PR in `curricula`; ratify the content model and licensing; then implement draft schemas/examples and CI before beginning complex portal features.
