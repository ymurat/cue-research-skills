# Manuscript Alphabet Archive

An agent skill for building and reviewing source-linked archives of manuscript
alphabets, cipher signs, and glyph tables. It helps keep each sign connected to
the original page while separating source keys, letter names, transliterations,
and historical sound claims.

## What it helps with

- Start a page inventory and extract one table before expanding a corpus.
- Preserve page, cell, and sign images with coordinates, relative paths, and hashes.
- Track uncertain readings, variants, review methods, and pending regions.
- Compare records across JSON, CSV, or SQLite when those formats are used.
- Choose evidence-supported mappings for learning exercises and manual transcription.

The workflow supports source keys in Arabic, Latin, or other scripts. It uses
the user's chosen data directory, not a fixed Mac path or the skill's installation
directory. See the [record contract](references/archive-contract.md) for the
suggested fields and validation coverage.

## Installation

With the Skills CLI:

```bash
npx skills add ymurat/cue-research-skills --skill manuscript-alphabet-archive
```

Alternatively, copy this entire folder, including `references/`, into a skills
directory supported by your agent. Follow that host's discovery/reload procedure.
The `agents/openai.yaml` file supplies optional display metadata for compatible
hosts; the skill entrypoint is [SKILL.md](SKILL.md).

## Example request

> Use manuscript-alphabet-archive with my manuscript in the project directory.
> Start with the alphabet table on PDF page 12. Keep the original page, cell,
> and sign crops; record the Latin source keys separately from proposed names
> and sounds. Report unknown readings and the checks you actually performed.

Provide your own source files and choose a corpus output directory. Reading the
instructions requires no API key. Actual extraction needs PDF/image tools and
file access in the agent's environment; the skill does not install those tools.
Use the current project's schema and utilities when they already exist.

## Scope and limits

This is a workflow and reference package. It does not include manuscript scans,
extracted signs, an OCR model, a database, an importer, or a validator. It does
not promise recognition accuracy or historical decipherment. A glyph's source
key or proposed name alone does not establish its historical pronunciation.
Paleographic conclusions require source review; automated integrity checks
cannot authenticate a script or a reading.

The optional [Garrett 52B example](references/garrett52b-example.md) describes
the initial pilot and its limits. Its 101-page/28-sign counts do not apply to
other manuscripts, and the original pilot files are not required or included.

## Türkçe açıklama

Bu beceri, el yazmalarındaki alfabe ve işaret tablolarını kaynak sayfalarıyla
bağlantılı bir arşive dönüştürmek için hazırlanmıştır. Harfin görüntüsünü,
kaynakta verilen karşılığını, adının Latin harfli okumasını ve tarihî ses
değerini ayrı tutar. Belirsiz okumaları ve henüz işlenmemiş bölümleri görünür
kılar; öğrenme alıştırmalarında yalnız kaynakla kontrol edilmiş eşleştirmeleri
kullandırır. Arapça, Latin harfli veya başka yazı sistemlerindeki anahtarlarla
çalışılabilir.

Kullanmak için kendi kaynak dosyanızı ve çıktı klasörünüzü belirtin. Beceri bir
OCR motoru ya da hazır veri tabanı değildir; PDF, görseller ve pilot betikleri
pakete dahil değildir. Örnek istek: “Bu yazmanın 12. sayfasındaki harf tablosunu
çıkar; kaynak hücreleri ve koordinatları koru, kesin olmayan okumaları işaretle.”

## License and provenance

[MIT License](LICENSE), copyright © 2026 Murat Yılmaz. The license covers the
newly authored skill instructions and documentation. Separately supplied source
materials and tools retain their own rights and licenses. See
[ATTRIBUTION.md](ATTRIBUTION.md) for provenance.
