# Shams al-Ma'arif (شمس المعارف)

**Author:** Shihab al-Din al-Buni (d. 1225 CE)
**Original language:** Arabic
**Original period:** 13th century
**Source manuscript:** Riyadh manuscript scan (Khalil Al-Maktabi, 2018 facsimile edition)
**Status:** Public domain (medieval work)
**License (this translation):** All Rights Reserved, personal use only — see [LICENSE](../LICENSE)

## Description

*Shams al-Ma'arif* ("The Sun of Knowledge") is al-Buni's encyclopedic grimoire, covering the Divine Names, the 28 lunar mansions, talismanic seals, planetary magic, and the practice of dhikr. It is one of the most influential Arabic magical texts of the late medieval period and remains widely studied in both occult and academic contexts.

## Contents of this folder

```
shams-al-maarif/
├── README.md                    # this file
├── english-only.pdf             # rendered PDF, English translation only
├── arabic-full.pdf              # rendered PDF, Arabic + English (face-to-face)
├── pages/                       # 783 per-page English source markdowns
│   └── page-NNNN.md
├── ocr/                         # 783 per-page OCR'd Arabic text + page images
│   ├── page-NNNN.txt
│   └── page-NNNN.png
└── docs/
    ├── chapter-index.md         # 325 chapters, alphabetical
    ├── glossary.md              # top 100 Arabic terms by occurrence
    └── source-notes.md          # translation methodology + known issues
```

## Watermark

Both PDFs are watermarked on every page in the top-left corner:

> **@nodedotshane  ·  personal use only**

The watermark is integral to the license. Pages distributed without the watermark are not covered by the personal-use grant. If you obtain a watermark-free copy from a source other than this repository, please notify the author.

## Translation

The English translation was produced in multiple stages:

1. **Urdu intermediary:** The source Arabic was first OCR'd, then rendered into Urdu as the working translation language.
2. **English rendering:** The Urdu was rendered into English.
3. **Per-page source markdowns:** Each page of the manuscript was rendered as an individual `page-NNNN.md` file for fine-grained editing.
4. **Rendered PDFs:** The per-page markdowns were typeset using ReportLab with the Amiri Naskh font (Arabic) and Times New Roman (English).

## Translation methodology

- Mistranslations and omissions from the Urdu intermediary are corrected when caught.
- Arabic letterforms and proper names are preserved in the original script alongside the English.
- Chapter headings and decorative frames are preserved.
- The original page numbering is preserved in the rendered PDFs.

## Known issues

- The Urdu intermediary introduces some interpretive choices that may differ from a direct Arabic→English translation. The Arabic+English PDF (face-to-face) lets the reader cross-check.
- OCR'd Arabic has occasional errors in diacritical marks; the source images in `ocr/` let the reader verify.
- A scholarly-grade translation would require direct work from the Arabic by an Arabic-fluent occultist/scholar.

## AI assistance disclosure

The Urdu intermediary and the English rendering involved AI assistance. The structural and editorial decisions, the choice of which works to translate, the per-page source markdowns, and the final PDF rendering are Shane's work.

## Source citations

When citing this translation, please cite:

- Original: al-Buni, Shihab al-Din. *Shams al-Ma'arif*. 13th c.
- Manuscript: Riyadh manuscript scan (Khalil Al-Maktabi facsimile)
- Translation: Shane Coy / Node Arcanum
- Year: 2026

## Related works in this repo

- *Ghayat al-Hakim* (the Western "Picatrix" derives from this)
- *Picatrix* (Latin translation of *Ghayat al-Hakim*)

## See also

- Private research corpus: `grimoires-arcanum/` (the working environment for this translation)
- Source PDF: `grimoires-arcanum/source-text/shams-al-maarif.pdf`
- OCR pipeline: `grimoires-arcanum/scripts/v1_pipeline.py`
