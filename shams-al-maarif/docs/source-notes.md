# Source notes — Shams al-Ma'arif translation

## Authorship

Translation by **Shane Coy** (@nodedotshane). The English rendering
chain is: Arabic scan → Urdu intermediary (Shane) → English rendering
(Shane, assisted by an LLM). The Arabic OCR + PDF composition was
done by Mavis from the source scan.

## Translation pipeline

1. **Source PDF** — `shams-al-maarif/scan.pdf` in this repo, 783 pages
2. **OCR** — Arabic text was OCR'd from the source PDF (`shams-al-maarif/ocr/`)
3. **Urdu intermediary** — Shane rendered the Arabic into Urdu
4. **English rendering** — Shane rendered the Urdu into English (LLM-assisted)
5. **Per-page markdowns** — Each manuscript page was written as a separate `page-NNNN.md` file in `shams-al-maarif/pages/`
6. **PDF composition** — Per-page markdowns + OCR were typeset with ReportLab using Amiri (Arabic) and Times New Roman (English) fonts

The Arabic+English PDF (face-to-face layout) uses the OCR'd Arabic directly. The English-only PDF omits the Arabic text.

## Known limitations

- The Urdu intermediary introduces interpretive choices. A direct Arabic→English translation would catch nuances the Urdu missed.
- Diacritical marks in the OCR'd Arabic have occasional errors.
- The original page numbering is preserved; cross-references in the original follow the manuscript pagination.
- The 325 chapter headings were extracted automatically; some chapter groupings may differ from a careful human reading.
- Top-100 glossary is a frequency count; not a curated glossary. Some entries are common particles rather than substantive terms.

## Files in this folder

- `chapter-index.json` — 325 unique chapter titles, sorted alphabetically, with first-page reference
- `glossary.json` — 7,181 Arabic terms with 5+ occurrences and 4+ Arabic letters, sorted by frequency; the top 100 are most useful

## Re-rendering the PDFs

The PDF rendering script is in the private research corpus at `grimoires-arcanum/scripts/compose_shams_pdf.py`. To re-render with corrections:

```bash
cd /Users/sc/Project\ Files/grimoires-arcanum
python3 scripts/compose_shams_pdf.py \
    --pages translation-pages/shams-al-maarif \
    --ocr ocr-pages/shams-al-maarif \
    --out shams-al-maarif-english-only.pdf
```

## Methodology for corrections

1. Edit the relevant `pages/page-NNNN.md` in this folder
2. Re-run the PDF rendering script
3. Commit the new PDF (the file will replace the old one in this repo)
