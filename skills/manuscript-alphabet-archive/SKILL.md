---
name: manuscript-alphabet-archive
description: Use when building, extending, or reviewing an archive of manuscript alphabets, cipher signs, glyph tables, source key mappings, letter-name readings, or learning exercises grounded in those records.
license: MIT
---

# Manuscript Alphabet Archive

Keep each sign traceable to its source image. A shape, a source key, a letter
name, a transliteration, and a historical sound are separate evidence.
This is a workflow/reference skill, not an OCR engine or a supplied corpus.

## Start or resume

Use the user's chosen data directory; the skill installation directory is not
the corpus root. Read [archive-contract.md](references/archive-contract.md)
when creating records or comparing formats. Preserve an existing project's
schema and document field mappings instead of silently renaming its fields.

For a new corpus, record the source identity, file hash, and PDF page count;
create a page inventory and distinguish blank, cover, content, and unexamined
pages. Start with one inspected table. For an existing corpus, inspect its
manifest, preparation scripts, and validation coverage before reporting progress
or regenerating outputs. Preserve deliberate edits before rebuilding.

Use available PDF/image tools to extract native scans or render pages. Record
which image and resolution define the coordinates. Missing tools or source
files limit execution; describe that limit instead of inventing results.

## Extract signs

Inspect the table's actual layout and reading direction. Give each source
occurrence a stable ID independent of its proposed reading. Record table,
physical row/column, reading order, and source page separately. Marginal signs
and variants retain their own context; similar shapes need not be identical.

Keep the source page, full cell, and sign crop, with source-image coordinates,
relative paths, and hashes. Generate a contact sheet and source overlay; inspect
every stroke for clipping. Preserve originals alongside enhancement derivatives.
For rotations or resampling, document the coordinate transformation. Unresolved
signs and empty cells stay explicit rather than reconstructed from expected order.

## Interpret and teach

| Evidence | Treatment |
| --- | --- |
| Source key, in any script | Record the literal key and its review status |
| Letter name or transliteration | Separate value, provenance, and uncertainty |
| Historical phoneme | Unknown stays `null`; key/name alone is not proof |
| Historical attribution | Distinguish manuscript claim from corroboration |

Use source-checked mappings for scored exercises and label the review method.
Provisional names are annotated reference material; uncertain names are excluded
from scoring. Assistant checking is not human or expert approval. Manual
transcription preserves selected signs and supported mappings; missing vowels,
unknown readings, historical speech, and translations are not generated as fact.

## Verify and report

Check structural integrity and source pixels, then compare relevant readings
and review statuses across exported representations. A validator's pass means
only the checks it actually performs; it does not establish paleographic truth.
Derive expected counts from the current corpus, not a different pilot.

Report inventoried pages, extracted signs, reviewed mappings, unresolved readings,
and pending regions separately. Keep local processing local unless the user
chooses a remote service. Read the optional [Garrett 52B example](references/garrett52b-example.md)
only for an illustration of pilot limits; its files and counts are not prerequisites.
