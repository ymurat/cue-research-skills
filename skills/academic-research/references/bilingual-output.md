# Turkish-English Output Guide

## Choose a mode

- **Bilingual (default when the user requests Turkish-English output):** give a complete English section followed by its Turkish counterpart, or use paired columns only when a table remains readable on mobile. Avoid alternating every sentence.
- **English-only / Türkçe:** use one language when explicitly requested. Otherwise mirror the user's language for routine chat while keeping research deliverables bilingual when requested.
- **Teaching material:** state the audience and language level; keep student-facing language separate from instructor notes. When requested, provide equivalent EN and TR versions rather than a partial summary in the second language.

## Preserve meaning and terminology

- Keep paper titles, proper names, citation keys, dataset/benchmark/model names, code, identifiers, formulas, and metric names in their original form. Do not translate a title inside a reference.
- Use established Turkish academic terms when clear; retain the English term in parentheses on first use if it is more precise or widely used (e.g., “yapı geçerliği (construct validity)”, “sızıntı (data leakage)”). Avoid inventing Turkish translations for API names or standard metrics.
- Keep claims, uncertainty, caveats, numerical values, units, and citation placement aligned across both languages. Do not make the Turkish version stronger or more certain than the English version.
- Do not translate quoted source text as if it were the original wording. Mark paraphrases and direct quotations appropriately.
- If a term has multiple plausible Turkish renderings, state the chosen term once in a short glossary rather than silently switching.

## Bilingual report pattern

Use only the sections needed:

# [Title in English] / [Türkçe başlık]

## English
- **Question / scope:** …
- **Evidence:** …
- **Finding or decision:** …
- **Limitations / uncertainty:** …
- **Next step:** …

## Türkçe
- **Soru / kapsam:** …
- **Kanıt:** …
- **Bulgular veya karar:** …
- **Sınırlılıklar / belirsizlik:** …
- **Sonraki adım:** …

## Terim notu (optional)
| English term | Türkçe karşılık / kullanım |
|---|---|

Keep the two language versions substantively equivalent. For a short answer, a two-column table may replace the separate sections only if it is easy to read on a phone.

## Quality check

Before delivery, check names, dates, units, references, cross-language consistency, and whether each version preserves the same limitations and action items. Use Turkish characters correctly (ç, ğ, ı, İ, ö, ş, ü); retain UTF-8 text.
