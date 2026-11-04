---
name: book-consistency
description: "Use when the user wants a long manuscript, book, or thesis (many chapters, tens of thousands of words) checked for consistency: terminology and abbreviation drift, repeated passages across chapters, broken cross-references and numbering, and continuity or contradictions between chapters."
---
# Book consistency audit

Audit a long manuscript chapter by chapter and report problems; do not rewrite the author's text. Structure (reference file first, then check against it, dated report) adapted from chianglianglin/novel-hint `continuity-check` (MIT).

## 1. Prepare
- Convert the source to Markdown: `pandoc book.docx -t gfm -o book.md` (install pandoc if missing; for LaTeX follow `\input`/`\include`).
- Split into one file per chapter (`ch01.md` ...) on top-level headings. Keep a map of chapter -> heading -> approximate page or paragraph number so every finding has a location.
- Never process the whole book in one pass; work chapter by chapter and write intermediate results to files (for long jobs, hand chapters to background workers and merge).

## 2. Build a project-local reference file (default: `book_bible.md`)
For each chapter extract:
- terms and their spelling variants (Turkish and English forms), with where each is first defined;
- abbreviations and where they are first expanded;
- figure, table, equation, listing numbers and captions;
- cross-references ("bkz. Bölüm 5", "Şekil 3.2", "see Section ...");
- key claims, definitions, numbers, dates, and named models or standards (with version/year);
- concepts the chapter assumes the reader already knows.
Merge into one glossary/term table: canonical form | variants found | first definition location | chapters used.
Show the proposed canonical forms to the user before step 3 if the choice is not obvious.

## 3. Checks
1. **Terminology**: same concept written differently (e.g. "gereksinim" vs "gereklilik" vs "requirement"); English term used where an established Turkish term exists, or vice versa; abbreviation used before expansion or expanded twice; TDK spelling and capitalization of terms. Use `turkish-native` and `tr-academic-style` skills where available. Optionally emit a Vale `Vocab` accept/reject list for the canonical terms.
2. **Repetition**: near-duplicate sentences and paragraphs across chapters. Use a local script (Python, TF-IDF cosine or sentence embeddings; flag pairs above ~0.8 similarity) and then read the pairs; report which to keep, not an auto-merge. Also flag the same example, anecdote, or definition retold in several chapters.
3. **Cross-references and numbering**: every referenced chapter/section/figure/table exists, numbers run in order with no gaps or duplicates, captions match the text that cites them, and in-text citations have a reference-list entry (and vice versa; use an available citation-check tool if present, otherwise check the references manually).
4. **Continuity**: a concept is used before it is introduced; two chapters define or quantify the same thing differently; contradicting claims; the same standard or tool cited with different versions or years; promises ("Bölüm 9'da ele alınacak") that are never fulfilled.
5. **Scope claims**: the book's stated aims (preface, introduction, back cover) versus what chapters actually cover; list gaps.

## 4. Report
Write `consistency_report_YYYY-MM-DD.md` (and .docx if the user works in Word):
- short summary with counts per category and the 5-10 most important issues first;
- findings table: # | location (chapter, section, paragraph/page) | category | severity (high/medium/low) | quote (short) | suggested fix;
- the glossary/term table as an appendix, ready to reuse as the book's term list.
Severity: high = misleads the reader or breaks a reference; medium = visible inconsistency; low = stylistic.
Report only verified findings with exact quotes; do not invent locations. Mark anything uncertain as "kontrol edilmeli".

## Rules
- Do not change the manuscript unless the user asks; if asked, apply fixes on a copy and list every change.
- Respect the author's voice; style preferences are suggestions, not errors.
- Reply in the user's language; no em dashes, no buzzwords.

## Source and license

Adapted from [`chianglianglin/novel-hint` `continuity-check`](https://github.com/chianglianglin/novel-hint/tree/d4aa27a5e52d2ebc1565b2416627082667639db6/skills/continuity-check), pinned to commit `d4aa27a5e52d2ebc1565b2416627082667639db6`. The upstream MIT copyright and permission notice is reproduced in this directory's `LICENSE`. This is an adaptation, not an official upstream release.
