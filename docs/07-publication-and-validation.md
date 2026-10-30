# Publication, Versioning and Validation

**Status: proposed release policy**

## Lifecycle labels

- **Draft:** incomplete or unreviewed; must display draft status.
- **Community-reviewed:** editorial/peer review recorded with limitations.
- **Expert-reviewed:** named qualified subject review with scope and last review date; no accreditation implication.
- **Superseded/withdrawn:** traceable previous release, correction or withdrawal reason.

No label claims the learner has passed a test or holds an official OWC credential.

## Versions and stable identities

- Record `schema_version` separately from `course.version`.
- Prefer semver-like content releases (e.g. 0.1.0, 0.2.0) while defining exactly what a breaking educational-content change means.
- Stable competency IDs and immutable publication tags enable LMS providers to preserve version references.
- Resource URLs and assets should be reproducible; published release manifests should contain paths, versions, licenses and integrity digests where practical.
- Translations and organizational overlays record original source revision to prevent stale policies or mismatched learning outcomes.
- Changes to a published learning outcome must receive a clear version change and migration guidance; do not silently redefine competency IDs.

## CI checks for MVP

1. Parse all YAML/Markdown front matter and reject malformed syntax.
2. Validate required fields and enumerated types against draft JSON Schema.
3. Ensure unique IDs, existing local references, correct competency mappings, supported locales and version format.
4. Flag missing rights/provenance, missing learning objectives and inaccessible media metadata.
5. Check source links and track stale/dated regulatory claims without assuming every external URL is always available.
6. Validate practice question answer shapes and explanations; human reviewers still check factual correctness.
7. Publish preview/diff and only release approved revisions.

## Reproducibility and acceptance

A versioned course should be downloadable and independently rendered with no live OWC service dependency. Exporters must report supported feature subsets, unmapped constructs and tested destination systems. Do not claim standards conformance until tested.

## Security

Treat contributed Markdown/HTML, media files and external links as untrusted. Sanitize for display, prevent remote script execution by default, protect contributor account/session data and disallow secrets/employee personal information in commits. The OWC content repo never stores real learner grades or operational private exams.
