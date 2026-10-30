# Canonical Format and Examples

**Proposed v0.1 design, not frozen**

## Source format

- **UTF-8 Markdown** for textual lessons; a documented, conservative Markdown subset to support portability. No arbitrary script execution.
- **YAML** for manifests, competencies, practice items and evaluation guides. Equivalent JSON representation should be straightforward, and exporters may expose JSON.
- **JSON Schema (2020-12 proposed)** for validation of structured records once fields are ratified.
- **Media** stored in an accessible assets directory or referenced by stable public URL with license and provenance. A URL is a reference, not a promise of offline availability.

## Recommended repository layout

```text
curricula/
  README.md
  docs/                 # reviewed, canonical design docs
  specification/        # future versioned machine-readable schemas
  courses/
    responsible-ai/
      course.yaml       # canonical course manifest
      competencies.yaml
      modules/
      lessons/           # Markdown resources
      practice/          # open practice questions and answers
      evaluation/        # nonbinding evaluation guidance
      assets/
      CHANGELOG.md
  shared/                # future reusable competencies/resources
  examples/              # illustrative non-approved samples
```

## IDs and versioning

- Course IDs are globally unique within the OWC catalogue, e.g. `OWC-AI-101`; lesson IDs are stable within the project, e.g. `OWC-AI-101-L01`.
- **Schema version** and **content version** are distinct; a typo correction must not imply a new schema.
- Never silently reassign an existing ID to a different learning outcome. Deprecations and aliases should be recorded.
- A translation maintains a relationship to a source content ID and revision. Region-specific adaptations are distinguishable from translations.
- Use BCP 47 language tags (e.g. `en`, `si-LK`) and explicit review dates; treat absent dates as unknown.

## Illustrative manifest

```yaml
schema_version: '0.1.0'
id: OWC-AI-101
version: '0.1.0'
status: draft
locale: en
title: Responsible AI at Work
competencies_ref: competencies.yaml
modules:
  - id: M01
    title: Foundations
    resource_refs:
      - lessons/introduction.md
practice_ref: practice/questions.yaml
evaluation_guide_ref: evaluation/guide.yaml
license: TBD
```

The proposed `extensions` field may support **namespaced provider data**, e.g. `extensions: { 'example.org/interactive': {...} }`. Exporters may ignore extensions without breaking required core semantics; namespacing and schema semantics are open for decision.

## Rights and safety

Do **not** put private employee records, copyrighted source material copied without permission, proprietary exam items, executable HTML/JS, tokens or confidential data in the repository. Review external links and uploaded media before publication.
