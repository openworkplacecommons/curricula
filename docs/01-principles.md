# Principles and Scope

**Draft design specification v0.1**

## Mission (agreed)

Open Workplace Commons (OWC) provides a community-maintained, freely reusable foundation for workplace education: curricula, competencies, teaching materials, practice questions/answers, and evaluation guidelines. It does not certify learners. Organizations and providers decide what training to deliver, how to evaluate it and whether to issue their own completion records.

## Core quality attributes

| Attribute | Design requirement |
|---|---|
| Vendor neutrality | A consumer must not depend on OWC portal APIs, Quizdemics, Anecdote, LMS Grid, or a specific LMS. |
| Human readability | Lessons are readable Markdown; key metadata is small and documented; a website editor can hide technical syntax. |
| Machine readability | Structured fields have defined types and validation, stable IDs and version references. |
| Generality | A course can cover technical, behavioral, legal-contextual or practical skills; media and assessment formats are optional. |
| Modularity | Independent lessons/resources and competencies can be referenced and reused across modules/courses. |
| Extensibility | Unknown namespaced extensions can be safely ignored by consumers, with required core semantics preserved. |
| Accessibility | Plain-language and assistive-technology-friendly source; support captions/transcripts/alt text and keyboard access in exporters. |
| Localizability | BCP 47 languages, translations linked to source revision, explicit jurisdiction/organizational overlays. |
| Trust and traceability | References, origin, authors, reviewer scope, licenses, corrections and version history are retained. |
| Stable publication | A tagged/reproducible release can be downloaded or imported offline. |
| Security and privacy | No learner identity or grades in the curriculum repository; community HTML/scripts are untrusted. |
| Automated quality | CI eventually checks syntax, references, mappings, asset licenses, links and export compatibility. |

## Explicit non-goals

- Running certification exams or maintaining secret official assessment questions.
- Accrediting employers, courses, assessment providers or credentials.
- Storing learners' attempts, personal records or certificates.
- Building a mandatory content player, LMS, commercial publishing service or exam engine.
- Guaranteeing regulatory compliance or asserting that a particular employer training policy is satisfied.
- Claiming SCORM/QTI/CASE/LTI conformance without successful documented tests.

## Separation of concerns

1. **Specification** explains shared semantics and portability contracts.
2. **Canonical content** is versioned, openly available source with clear licensing.
3. **Publication tools** validate/render/export content but are replaceable.
4. **Delivery and evaluation** belong to independent providers and organizations.
5. **Community governance** reviews the accuracy and quality of OWC publications, not learner competence.

The first milestone is a small, accurate, documented specification—not universal support for every current or future edtech tool.
