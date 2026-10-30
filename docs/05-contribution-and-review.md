# Community Contributions and Review

## Two submission paths

**Technical contributor:** fork/edit files and submit a GitHub pull request.

**Nontechnical contributor (future portal):** use contextual forms on a course/lesson: Suggest an Improvement, Submit a Lesson, Add a Practice Question, Translate. The portal stores a draft and references the course ID, resource ID and source version. After initial validation, a trusted service account or GitHub App may create a PR. **No website submission is published directly.**

A simple monitored form/manual review is sufficient for the MVP. Accounts, rich editing, uploads and automatic PR creation are later enhancements; avoid making GitHub knowledge a prerequisite for educational contributors.

## Contribution metadata

- Content type, source course/resource ID and target version.
- Contributor's chosen public credit/consent preferences.
- Description and educational value of the change.
- Competency mapping and, for questions, correct answers/explanations.
- Authoritative references and dates for time-sensitive claims.
- Provenance, license/rights declaration, third-party asset permissions.
- Language/region and accessibility notes.

## Review roles

| Role | Responsibility |
|---|---|
| Contributor | Proposes a change; does not approve own submission. |
| Editorial maintainer | Checks clarity, metadata, attribution, accessibility, basic structure. |
| Subject-matter reviewer | Verifies domain accuracy and appropriate source evidence. |
| Curriculum reviewer | Verifies learning outcomes, pedagogy, competency mapping and evaluation examples. |
| Release maintainer | Ensures recorded approvals, CI checks and release/version bookkeeping. |

A person may fill multiple roles in a small project, but **a substantive contribution should receive independent review**. A public curriculum quality approval is *not* a certification of learners, training providers or legal compliance.

## Proposed review policy

- Formatting/typo: editorial approval.
- New lesson, important correction or practice item: editorial + domain/curriculum review as appropriate.
- Regulated or jurisdiction-specific claims: relevant qualified reviewer, scope and review date recorded.
- Major curriculum revision: documented release approval and change notes.
- Contested content: reviewers request evidence/revisions; a maintainer may reject with rationale.

## Workflow

```text
Proposal → draft → automated validation → editorial review → SME review if needed
→ approved PR → merge → versioned published release → portal consumes release
```

Keep source/reviewer identities proportionate to role; casual contributors need not submit government IDs. Privileged reviewers need demonstrable relevant expertise. Public attribution must respect privacy/consent.
