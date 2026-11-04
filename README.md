# Cue Research and Workflow Skills

This repository contains four independent agent skills for use with Cue, the AI assistant app. They support research and teaching, long-manuscript consistency review, citation and bibliography checks, and research-talk and poster preparation. Each skill has its own upstream source and license.

## Included skills

- **academic-research** — evidence-grounded research and teaching support in software engineering, AI, VR/XR, and serious games.
- **book-consistency** — read-only, chapter-by-chapter consistency review for long manuscripts.
- **citation-management** — bilingual guidance for citation and bibliography checks in software engineering and AI research.
- **talk-prep** — research-talk and poster preparation, including scripts, slides, Q&A, and rehearsal.

## Scope and limitations

- `citation-management` is a prose-only adaptation. It does not include the upstream automation scripts, references, assets, or `CITATION.cff`; it does not provide that package's automated metadata processing.
- `talk-prep`'s speaking-time estimator supports English and Chinese rates. Its print-PDF script offers `en` and `zh` language options only. Turkish-specific timing or a verified Turkish print/PDF workflow is not included.
- Dependencies and platform assumptions vary by skill. Check each skill's `SKILL.md`, `ATTRIBUTION.md`, and bundled resources before use.

## Sources and licensing

Each skill folder includes its own attribution and applicable license files. The SimplePlus theme bundled under `talk-prep` has a separate license and notice. No single license covers the collection as a whole. See [Sources and Licenses](SOURCES-AND-LICENSES.md) and follow the terms that apply to each component.

These are independent adaptations and are not official releases or endorsements by their upstream authors.