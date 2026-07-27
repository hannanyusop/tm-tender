# AGENTS.md — Repository Working Rules

Scope: this file applies to the entire repository unless a more specific `AGENTS.md` exists in a subdirectory.

This repository organizes tender source documents and generated working outputs for the TM & Cradle BIG 2.0 / Falcon RFP.

## Source-of-Truth Order

When creating, reviewing, or updating tender outputs, use this order:

1. This root `AGENTS.md` for repository-wide structure, naming, and output rules.
2. Any scoped `AGENTS.md` in the relevant directory, such as `Source/AGENTS.md`.
3. `Source/01 Summary.md` for orientation.
4. Original source files in `Source/` for exact wording, requirements, clauses, forms, and submission-critical details.
5. Existing files in `Output/` for established output structure and naming patterns.

Do not rely only on summaries for final submission wording. Verify contractual, financial, legal, commercial, technical, and submission-critical details against the original source files.

## Directory Structure

Use these top-level directories consistently:

| Directory | Purpose |
| --- | --- |
| `Source/` | Original tender documents, source summaries, and source-specific index instructions. |
| `Output/` | Generated working documents, checklists, proposal drafts, compliance matrices, and submission-ready support files. |

Do not rename original files in `Source/` unless explicitly requested. Preserve source filenames so references remain traceable.

## Output Folder Naming

Create generated work under `Output/` using numbered folders:

```text
Output/NN Descriptive Folder Name/
```

Rules:

- Use two-digit numeric prefixes: `01`, `02`, `03`.
- Use title case after the number.
- Keep names short but specific.
- Prefer nouns that describe the output set, not the task.
- Do not use vague names such as `Misc`, `New`, `Drafts`, or `Files`.

Examples:

```text
Output/01 RFP Submission Checklist/
Output/02 Commercial Proposal/
Output/03 Technical Proposal/
Output/04 Compliance Matrix/
```

## Output File Naming

Name generated files inside output folders using numbered files:

```text
NN Descriptive Name.md
```

Rules:

- Use two-digit numeric prefixes.
- Use title case.
- Prefer Markdown for working documents unless the required deliverable format is Word, Excel, PowerPoint, PDF, CSV, or another source-mandated format.
- Keep the filename aligned with the document purpose.
- Avoid duplicate names with different meanings.

Examples:

```text
Output/01 RFP Submission Checklist/01 Checklist.md
Output/02 Commercial Proposal/01 Volume II Index.md
Output/03 Technical Proposal/01 Technical Response Outline.md
```

## Directory Index Rules

Each output folder should be self-explanatory.

For a folder with one file, the file itself may act as the index if it includes:

- Tender reference or project context.
- Source file references.
- Clear sections or tables showing what the file covers.

For a folder with more than one file, create an index file:

```text
Output/NN Descriptive Folder Name/00 Index.md
```

The index should include:

| Section | Required Content |
| --- | --- |
| Purpose | What this folder is for. |
| Source References | Original source files used. |
| File Index | Table listing each file, purpose, and status. |
| Open Issues | Missing inputs, assumptions, or items requiring user confirmation. |
| Last Updated | Date of the latest meaningful update. |

Use this table format for file indexes:

```markdown
| File | Purpose | Status |
| --- | --- | --- |
| `01 Checklist.md` | RFP submission checklist. | Draft / In Review / Final |
```

## Markdown Content Standards

Generated Markdown files should include enough context to be useful without opening the whole repository.

Recommended structure:

1. Title.
2. Tender reference or document context.
3. Source references.
4. Usage notes or assumptions.
5. Main content.
6. Open issues or verification notes, if any.

Use checkboxes for actionable review items:

```markdown
- [ ] Action item
```

Use tables for document inventories, compliance lists, evidence maps, and submission tracking.

## Source References

Every generated output that depends on tender documents should cite source filenames using repo-relative paths.

Examples:

```markdown
Source: `Source/01 PART III - Appendix A_Checklist of Tender Submission_amend.docx`
Source: `Source/PART I - Instructions to Proposers RFP Falcon (Ver1.0) (1).pdf`
```

When a requirement comes from multiple sources, list all relevant sources instead of collapsing them into a generic reference.

## Submission and Compliance Work

For tender compliance, checklist, proposal, and submission-pack tasks:

- Start with `Source/AGENTS.md`.
- Use `Source/01 Summary.md` for orientation.
- Verify exact requirements in the original source files.
- Cross-check Appendix A checklist items against Part I submission instructions.
- Keep Phase 1 and Phase 2 submissions separate where the tender requires it.
- Keep priced and unpriced BOQ files clearly separated.
- Flag numbering inconsistencies, missing source files, or unclear requirements instead of silently normalizing them.

## Existing Output Index

| Path | Purpose | Status |
| --- | --- | --- |
| `Output/01 RFP Submission Checklist/01 Checklist.md` | Checklist covering Appendix A items, Part I submission mechanics, Phase 2 price submission, and quality checks. | Draft |

Update this index whenever a new top-level output folder is created.
