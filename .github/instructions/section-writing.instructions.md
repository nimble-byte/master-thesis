---
name: section-writing
description: "Use when writing or refining subsection/subsubsection content. Triggers: section writing, subsection draft, write section, missing citations."
applyTo: contents/**/*.tex
---

# Purpose

This instruction guides agents to help produce, review and iterate subsection or subsubsection drafts for the thesis. It assumes collaborative work and links drafts to a tracking GitHub issue.

## Prerequisites (starting checklist)

The following conditions should be met before starting a section writing task. Point out missing prerequisites or ambiguities in the notes before proceeding.

1. Writing notes present for the target subsection (either in a shared instruction file or linked in the GitHub issue).
2. The referenced subsection (frontmatter `section`) can be found in the specified LaTeX file (frontmatter `file`, e.g., `contents/03-methods.tex`) and has a label (e.g., `sec:methods-data`) that matches the notes.
3. A GitHub issue exists to track the work and is referenced using the issue id (e.g., `#1123`).
4. `literature.bib` is present in the repository root and up-to-date enough for citation checks.

### Writing Note Template

When writing notes for a subsection, use the following template to ensure all necessary information is included and how to structure the notes for the agent:

```md
---
file: contents/03-methods.tex
section: sec:methods-data
issue_id: "#1123"
---

# Writing Notes

# Open Questions

- Question 1
  - response to question 1
- Question 2
  - response to question 2

# Missing Citations

- [ ] AuthorYearKey1
- [ ] AuthorYearKey2
```

## Workflow

1. User requests section writing for a specific target (include file path and subsection label, and reference the GitHub issue id).
2. Agent reads the provided writing notes and the target `.writing-notes/*` context as well as the `contents/*` files and produces:
   - A list of open questions and ambiguities in the notes under a "# Open Questions" header in the writing note file referenced
   - A list of missing citations by checking `literature.bib` for the documents referenced in the notes in APA format
3. User answers the open questions and provides any missing citation keys (or adds them to `literature.bib`). Open questions have to be resolved before proceeding to drafting.
4. User prompts the agent to produce the first draft for the subsection (specify tone, length, and which points to prioritise).
5. Agent generates a draft and annotates places with `TODO` or `MISSING_CITATION{<key>}` markers where human review or bibliography additions are required.
6. Iterative improvement: the user edits the draft and re-prompts the agent for refinement. Repeat until ready.
7. When the draft is acceptable, the user creates a commit with a single-line header and a body referencing the issue (e.g., header `docs(section): add draft for sec:methods-data` and body `references #1123`).

## Commit message template

- Header (one line): `docs(section): add draft for <section-label>`
- Body (optional): `references #<issue>`

## Notes on citations

- The agent will attempt to detect missing citations by matching author references in the notes against entries in `literature.bib`.
- If a citation is missing, the agent will list the missing as markdown checklist items (e.g., `- [ ] Millerh2019`) in the "# Missing Citations" section of the notes.

## Example user prompt
"Write a 300-word subsection for `contents/03-methods.tex`, label `sec:methods-data`, linked to issue `#1123`. Use the writing notes attached to issue `#1123`. Prioritise describing sampling and data preprocessing."
