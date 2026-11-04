---
name: talk-prep
description: "Use when the user needs to present a paper or research at a conference talk, seminar, journal club, defense rehearsal, or invited talk, or make a poster; prepare a timed talk script, slides, Q&A, rehearsal, and speaker notes."
---
# Talk and poster preparation

Adapted from [mimaowang/paper-to-podium](https://github.com/mimaowang/paper-to-podium/tree/8cb3bf579c2214f215a9336df519e74821a874ac), pinned to commit `8cb3bf579c2214f215a9336df519e74821a874ac` (MIT; notice in `LICENSE-paper-to-podium`). The bundled SimplePlus theme is v1.1 from [pm25/SimplePlus-BeamerTheme](https://github.com/pm25/SimplePlus-BeamerTheme/tree/d4134a7659515d1842e599b33aa84a82e39197d2); its separate `LICENSE` and `NOTICE.md` are retained in `assets/simpleplus/`.

Core rule from upstream: the script is the talk; slides are an excerpt of the script, never the other way round.

## Talk workflow
1. **Intake**: occasion (conference, seminar, defense, invited, class), audience expertise, duration including Q&A, language, venue template, required extras. Infer from context; ask only if duration or audience is unknown.
2. **Read and research**: read the whole paper; keep a source list separating paper-internal claims (table/figure/section) from external facts. Every number said aloud must be traceable.
3. **Script**: plain spoken language at the speaker's pace. The bundled `estimate_talk_length.py` has English and Chinese rates only; for Turkish, count the spoken words and use a pace chosen for the speaker rather than treating an English rate as Turkish-specific. Leave margin for questions.
4. **Slides**: one idea per slide, the paper's 2-4 argument-carrying figures on their own slides, readable from the back row. Use the user's institutional template if any; else the bundled Beamer skeleton, the `slides` skill for .pptx/Google Slides, or `icarus-figures` for redrawn figures. For Turkish in Beamer, use XeLaTeX with fontspec and a font with Turkish glyphs; drop the CJK block.
5. **Visual QA**: render every page (`render_pdf_pages.sh`) and look at it; fix crowding and overflow.
6. **Verify**: fact-check numbers against the source list; proofread the script (use `turkish-native` for Turkish); blind review by a fresh reader who sees only the slides.
7. **Stage**: script aligned to slide numbers with page-turn cues; print-ready script (`script_to_print_pdf.py`, whose bundled `--lang` options are `en` and `zh` only). For Turkish print PDFs, use a separately validated workflow.

## Q&A preparation (always include)
- 10-15 likely questions grouped as: clarifying, methodological (validity threats, sample, baselines), novelty and related work, generalisability, ethics and data, "what next".
- For each: a 20-40 second answer, the evidence it rests on, and a backup slide if needed.
- The 3 hardest questions get a frank answer that concedes the limitation where real.
- Optionally ask the debate agents (Metodolog, Şeytanın Avukatı, Etki ve Etik) to play hostile audience members.

## Poster workflow (not covered upstream)
1. Get the venue's size and orientation (e.g. A0 portrait) and any template.
2. Write a one-sentence takeaway as the title or headline; the poster must make sense in 10 seconds from 2 m away.
3. Layout: 3 or 4 columns, reading order left-to-right top-to-bottom; about 300-800 words total; one main figure as the visual anchor; QR code to the paper or artifact.
4. Body text at least about 24 pt and titles about 72 pt or larger at A0 (scale for other sizes); check by rendering at 25% and reading.
5. Build in LaTeX (tikzposter/beamerposter), PowerPoint, or Figma as the user prefers.
6. Prepare a 1-minute and a 3-minute spoken walk-through plus the Q&A list above.

## Done means
Script within time with margin; every slide visually checked; numbers traced; Q&A sheet ready; print-ready notes. No em dashes, no buzzwords, no fabricated numbers.
