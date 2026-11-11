# Optional example: Garrett 52B pilot

This example explains the workflow's origin. It is not an included dataset,
an authoritative edition, or a prerequisite for processing another manuscript.

A local project used a 101-page PDF supplied under the descriptive filename
`Ancientalchemicalmagicalalphabets.pdf`. Its initial pilot linked a letter-name
table on PDF page 7 to a 28-sign main table on PDF page 8 by matching source keys.
The main table had seven rows and four physical columns, read right to left.

That pilot preserved 28 full cells, 28 sign crops, and 28 name cells. The source
key was Arabic; names were recorded separately in Latin transcription. Two name
readings remained uncertain; historical phonemes were unknown. Assistant visual
checks were recorded without claiming expert or human approval.

The left-margin sequence on page 8 and the other alphabet tables were outside
the initial extraction. Inventorying 101 pages therefore did not complete the
book. The manuscript's script/origin attributions remained claims to evaluate.

An initial project validator compared source pixels, hashes, IDs, keys, and
selected database constraints, but did not compare every reading or status
across JSON, CSV, and SQLite. A pass could therefore miss a changed phoneme or
review label in another representation. This is why the general contract calls
for comparing all fields used by exercises or exports.

Apply the method to a new source using that source's own page count, script,
geometry, reading direction, and evidence. The original PDF, images, database,
builder, and validator are not distributed with this skill, and their local
paths are not installation requirements.
