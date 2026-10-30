# Interoperability and Distribution

**Agreed direction:** the content format is independent of the delivery system and of OWC's own products.

## Layered architecture

```text
Public OWC curricula (Markdown / YAML / assets / releases)
                  |
          Parse and validate
                  |
         Content model (IDs, outcomes, resources, practice, guides)
                  |
        Optional provider-specific adapters
         |         |         |         |
       HTML     SCORM      JSON      QTI practice items
                  |
     Any compatible LMS / site / authoring environment
                  |
    Optional adopter-run evaluation and completion records
```

**LTI 1.3 is not a file format.** It is one optional mechanism for an independently hosted learning/assessment tool to launch from an LMS, with additional services available where supported. No dependency on LMS Grid is implied.

## Interoperability profiles (not commitments of implementation)

| Profile | Purpose | Important constraint |
|---|---|---|
| Accessible HTML / Markdown | Browsing, embedding, offline documents | Sanitize renderable content; preserve headings, alt text, language metadata. |
| Structured JSON | Custom apps, catalogues, indexers | Version semantics and schema contracts required. |
| SCORM 1.2 / SCORM 2004 | Portable LMS training package | Completion/resume rules and embedded media require version-specific testing; client-delivered questions are not secret. |
| LTI 1.3 / Advantage | Hosted learning tools integrated with LMSs | Launch/authentication and grade exchange belong to an independent LTI provider; OWC source isn't an LTI tool. |
| QTI | Export/import of public practice assessments | Mapping to supported item types can be lossy; do not claim test-security from QTI. |
| CASE | Exchanging mapped competency frameworks | Only implement a mapping after defining semantics and testing an actual consumer. |
| Schema.org LearningResource | Catalogue discoverability | Metadata mapping, not a curriculum format replacement. |

## Neutrality acceptance tests

- A third-party parser can import a course without OWC accounts, APIs or tokens.
- A standalone lesson can be rendered by two independently implemented consumers with equivalent meaning and accessible structure.
- Course/competency/practice IDs and attribution survive exports or the export documents any information loss.
- One course runs in a third-party LMS via downloadable content, without our EdTech platforms.
- All interoperability claims record the implementation, standard version, tested platform version, test case and result.

## Ownership boundary

**OWC:** source content and public evaluation guidance.
**Content creators/hosted tools:** format conversion, learning experiences, optional LTI endpoints.
**Employers/LMS/assessment providers:** learner accounts, assessments, grades, compliance records and any certificates.

Our own Quizdemics, Anecdote, and LMS Grid may be reference implementations. They must never become privileged or mandatory routes to OWC content.
