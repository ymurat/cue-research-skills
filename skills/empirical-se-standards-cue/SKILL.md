---
name: empirical-se-standards-cue
description: Design, self-check, or review empirical software engineering studies against the ACM SIGSOFT Empirical Standards. Use for experiments, case studies, surveys, repository mining, data science, systematic reviews, and related empirical SE methods.
---

# Empirical SE Standards for Cue

Use this skill when a study or manuscript makes empirical claims in software engineering. It supplies a method-sensitive checklist and evidence trail. It does not replace disciplinary judgment, a full peer review, or an ethics or legal decision.

## Source and freshness

- Before applying criteria, read only the relevant method sections in `references/essential-attributes.md`.
- That checklist is a CC0 snapshot fetched from the ACM SIGSOFT Empirical Standards repository on 2026-10-31. The standards files in the official repository were last changed on 2026-10-14 when checked on 2026-11-07; later repository commits may affect other site files. Check the [official standards repository](https://github.com/acmsigsoft/EmpiricalStandards) before formal citation or high-stakes use, and record the access date.
- Preserve the distinction between essential attributes and desirable guidance. Do not turn a checklist into a rigid score or infer that one missing item automatically invalidates a study.
- Verify method references, editions, and bibliographic details before citing. Do not invent citations, DOIs, page numbers, methods, sample sizes, or study facts.

## Workflow

1. **Identify the task and evidence.** Determine whether the user wants study design, a manuscript self-check, or a reviewer-style assessment. Use only supplied or otherwise authorized materials. Keep manuscript files read-only unless the user explicitly requests editing.
2. **Identify the empirical method from the actual study.** State the purpose, research questions, contribution type, unit of analysis, data, and analysis approach when the material supports them. Distinguish the authors' method label from what they actually did. For multiple methods, use each applicable method standard plus the General Standard. This standards collection has no separate Design Science standard; use Engineering Research where appropriate and explain that mapping.
3. **Select criteria.** Read the General Standard and matching method section(s) in `references/essential-attributes.md`. Read only relevant sections of the official standards or supplements when a decision depends on details beyond the bundled essential checklist.
4. **Trace every judgment to evidence.** For each relevant attribute, record one status: **Met**, **Partly met**, **Missing**, **Not assessable from the supplied material**, or **Not applicable**. Give a page, section, table, figure, or short quotation where possible. Do not treat an omission from a supplied excerpt as a manuscript-wide omission.
5. **Evaluate appropriateness and validity.** Assess whether the method fits the research question, whether the design and analysis support the claims, and whether limitations and ethics are addressed. Use a validity scheme suited to the method. For experiments, consider conclusion, internal, construct, and external validity. For case studies, consider construct and internal validity, external validity, and reliability. Explain concrete threats and actual mitigations, not generic lists.
6. **Prioritize feedback.** Separate essential omissions that affect interpretation or validity from desirable improvements and editorial suggestions. Distinguish fixable reporting gaps from design flaws that undermine an inference. Do not demand a different method when the chosen method is appropriate.
7. **State limits.** Mark missing evidence, inaccessible appendices/data, unclear method classifications, and standards that need live verification. Never claim to have inspected a source or artifact that was not available.

## Study-design output

Provide a concise design brief with:

- purpose and research questions;
- chosen method(s), contribution type, and applicable standards;
- a table mapping each relevant essential attribute to the planned design decision and where it will be reported;
- sampling/data collection, analysis, ethics/data management, and validity plans;
- open questions and assumptions requiring the researcher's decision.

Do not manufacture a population, sample size, data, results, ethics approval, or partner commitments. Use explicit placeholders where the researcher has not decided.

## Manuscript self-check or review output

Start with a short scope statement and a restrained overall assessment. Then provide:

1. the actual method/contribution classification and any mismatch with the manuscript's label;
2. an evidence-linked table or compact list of relevant essential criteria and statuses;
3. the highest-priority validity, analysis, reporting, and ethics concerns, linked to manuscript evidence;
4. concrete revisions ordered by importance;
5. materials or current-source checks still needed.

When asked for a simulated referee report, use `academic-paper-peer-review` for report structure and keep this skill's method-specific evidence mapping. Do not issue an accept/reject recommendation unless asked and supported by available evidence.

## Method notes

- Select the standard based on the actual method: case study, experiment, questionnaire or qualitative survey, repository mining, data science/benchmarking, systematic review, mixed methods, longitudinal study, grounded theory, replication, engineering research, and other categories in the bundled checklist.
- For systematic reviews, use the project's review protocol and relevant systematic-review skill alongside this checklist. Do not claim PRISMA or another reporting guideline is met from this checklist alone.
- For computational studies, distinguish reproducing a reported result from reproducing the full research process. Use the reproducibility skill when the task concerns rerunning artifacts or computational workflows.
- For human participants or personal data, flag ethics and data-protection issues for appropriate specialist review. This checklist is not ethics approval or legal advice.

## Provenance

This Cue adaptation is based on the `empirical-se-standards` skill in Murat Yılmaz's `academic-agent-skills` repository and the CC0-1.0 ACM SIGSOFT Empirical Standards checklist. See `ATTRIBUTION.md` and the bundled CC0 notice. The bundled checklist may lag the official source.
