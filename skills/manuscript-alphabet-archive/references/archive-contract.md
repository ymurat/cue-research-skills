# Archive record contract

This is a suggested interchange contract, not a database implementation or a
schema migration. Reuse a project's existing fields with an explicit mapping.
JSON, CSV, and SQLite need not all be produced unless the user's task needs them.

## Source and page inventory

Keep a source ID, title or supplied label, local filename, SHA-256, and page count.
Use relative asset paths within the user's chosen corpus directory. PDF page
numbers are 1-based and distinct from manuscript foliation.

Inventory every page with its kind and extraction state. `pending`, `partial`,
and `complete` describe extraction coverage, not authenticity or reading quality.
Separate expected, extracted, and reviewed cell counts for each table. Unknown
expected counts stay null. An empty cell can be recorded without manufacturing
a glyph. A missing page is not a blank page.

## Minimum sign record

| Field group | Contents |
| --- | --- |
| Identity | Stable occurrence ID, source ID, alphabet ID, table ID |
| Location | PDF page; optional foliation; physical row/column; reading order |
| Source image | Relative path, SHA-256, width, height, extraction/render method |
| Geometry | Cell and glyph boxes; optional cell polygon; coordinate convention |
| Assets | Page, cell, and glyph paths/hashes; optional name-reading crop |
| Source mapping | Literal key; key script or `unknown`; value-specific status and evidence |
| Name reading | Optional manuscript name; its source, alternatives, and status |
| Transliteration | Optional convention and value, separate from the key and name |
| Phoneme | Optional historical sound, evidence, and status; null when unknown |
| Review | Reviewer kind/label, method, evidence location, notes, archive version |

Source occurrence IDs include table identity where a page has several tables,
for example `ms01-p012-t01-r01-c04`. Physical columns count from the left;
reading order follows the source and may run right to left. Record a different
column convention explicitly when preserving an existing schema.

## Coordinates

Default boxes are `[x0,y0,x1,y1]` in source-image pixels, origin top-left, x to
the right and y down; right and bottom are exclusive. State the convention in
the manifest. Bounds must lie inside the referenced image. A crop from a rotated
or resized derivative references that derivative and its transformation; do not
mix those coordinates with the native scan. Hash the exact referenced image.

Keep unmodified crops for comparison. Deskewing, thresholding, and background
removal are derivatives, not substitutes for source evidence.

## Reading status

Suggested value-specific statuses: `unknown`, `unreviewed`, `provisional`,
`uncertain`, `source_checked_by_assistant`, `source_checked_by_human`.
Existing projects may use other labels; document their meaning.

Record who checked what and how. A human source check is not automatically
expert authentication. Conflicting or missing status fields are unresolved;
do not silently select the most confident representation. A bare key/name is
not a historical sound. Source claims about the script's origin are metadata,
not proof of that origin.

Illustrative interpretation fragment for a Latin-keyed sign (no asset or
historical reading is supplied by this example):

```json
{
  "id": "ms01-p012-t01-r01-c04",
  "source_key": {
    "value": "A",
    "script": "Latin",
    "status": "source_checked_by_assistant",
    "evidence": {"pdf_page": 12, "cell_id": "p012-t01-r01-c04"}
  },
  "name_reading": {"value": null, "status": "unknown", "alternatives": []},
  "transliteration": {"value": null, "convention": null},
  "historical_phoneme": {"value": null, "status": "unknown"}
}
```

## Validation coverage

| Check | What it establishes |
| --- | --- |
| Unique IDs and foreign keys | Records link to declared sources, pages, tables, and alphabets |
| Asset hashes, dimensions, bounds | Paths point to the expected images and valid regions |
| Pixel comparison with unmodified source crops | Crops reproduce the declared boxes |
| Inventory and table counts | Counts agree with this corpus's declared scope |
| Explicit field comparison across formats | Compared readings, nulls, alternatives, and statuses agree |
| Contact sheet and overlay inspection | Strokes and labels were visually reviewed in context |

When several formats exist, join by occurrence ID and compare every field used
for exercises or export. ID/key equality alone does not check names, phonemes,
or review status. A changed mapping status or phoneme in just one representation
must be reported as a mismatch. Account explicitly for CSV empty strings versus
JSON/SQLite nulls; empty, unknown, and a literal question mark need not mean the
same thing.

Inspect the actual coverage of any project validator before relying on it.
Run mutating validators on a copy for read-only reviews. Do not claim this skill
ships a validator: it specifies the checks for the available tools to perform.

## Completion report

State source/page coverage, table-by-table extraction and review counts, unknown
totals, unresolved readings, unprocessed margins, and checks actually executed.
Do not calculate a whole-book completion percentage from an unknown sign total.
