# Content Model

**Status: proposed v0.1 model, subject to feedback**

## Core entities

| Entity | Purpose | Required conceptual properties |
|---|---|---|
| **Course** | A versioned grouping addressing an audience and purpose | ID, title, locale, version, status, license/reference policy, competencies, modules |
| **Competency** | Observable learning objective independent of delivery | Stable ID, statement, optional evidence guidance |
| **Module** | Ordered or unordered group of resource references | ID, title, child resource refs, optional competency refs |
| **Learning resource** | Lesson, article, video, scenario, exercise, downloadable document, external resource | ID, type, title, source/URL or local path, language, rights/provenance |
| **Practice item** | Openly published question, correct response and explanatory feedback | Stable ID, type, prompt, option/answer model, competency mapping, explanation |
| **Evaluation guide** | Nonbinding guidance for adopters creating their own assessments | Covered competencies, suggested evidence, item types, rubrics/examples, limitations |

A **course** composes modules and competencies, modules reference resources, and practice items map to competencies. Not every resource is a lesson, and not every course requires an exam or a certificate.

## Relationships

```text
Course v1.0
  ├── targets → Competency A, B, C
  ├── includes → Module 1, 2, ...
  │                 └── references → Lesson / Scenario / Video / Activity
  ├── offers → Public Practice Items → map to Competencies
  └── suggests → Evaluation Guide → maps to Competencies
```

## Course template (proposed minimum)

1. Identity: stable ID, version, schema version, title, language, status.
2. Audience and scope: purpose, intended roles, prerequisites, expected duration if known.
3. Outcomes: measurable competency statements with IDs.
4. Structure: module IDs and resource references (optional sequencing).
5. Educational resources: text and/or licensed external/local media, examples, scenarios and activities.
6. Practice: optional or recommended openly reusable items, answers and explanations.
7. Evaluation: public nonbinding blueprint, sample rubrics and advice on adapting to an organization's policies.
8. Provenance: authors/contributors, links/references, rights, review status, reviewed date, revision history.
9. Localization/adaptation: locale, source revision, applicable jurisdictions, organization extension hints.

## Design questions to settle

- Whether a standalone, reusable competency belongs under a course or a global competency catalogue.
- How strongly to enforce resource ordering and prerequisites across independent delivery systems.
- Exactly which metadata is mandatory for a draft versus an expert-reviewed release.
- Whether Markdown front matter or a separate manifest is the authoritative metadata source for each resource. **Avoid competing duplicate fields.**

## Example

See [the draft Responsible AI manifest](../examples/responsible-ai/course.yaml) and [sample practice questions](../examples/responsible-ai/practice/questions.yaml). They are structure examples, not validated learning material.
