# Node Arcanum

Public translations of grimoires and esoteric source texts.

Each work lives in its own folder containing the book and all source documents, supporting files, and rendered versions.

## Works

- **Shams al-Ma'arif** (`shams-al-maarif/`) — al-Buni's encyclopedic grimoire (13th c. Arabic). English-only and Arabic+English rendered PDFs, per-page source, OCR, chapter index, glossary.
- **Picatrix** (`picatrix/`) — coming soon.
- **Ghayat al-Hakim** (`ghayat-al-hakim/`) — coming soon.

## Structure

```
node-arcanum/
├── README.md
├── LICENSE
├── _template/                    # drop-in folder for new works
└── <work-name>/
    ├── README.md                 # what this work is, source, attribution
    ├── *.pdf                     # rendered books (Arabic, English, bilingual)
    ├── pages/                    # per-page source markdowns
    ├── ocr/                      # per-page OCR'd text
    └── docs/                     # indexes, glossaries, supporting material
```

## Status

This repo is the public face of work happening in the private `grimoires-arcanum` research corpus. New works are added as translations are completed.

## Large files and Git LFS

The rendered PDFs (e.g. `shams-al-maarif/english-only.pdf` and `arabic-full.pdf`) are over 100 MB each. **GitHub rejects files over 100 MB on regular push.** This repo is set up to use **Git Large File Storage (LFS)** for `.pdf`, `.png`, and `.zip` files (see `.gitattributes`).

Before your first push, install Git LFS:

```bash
# macOS (Homebrew)
brew install git-lfs

# macOS (no Homebrew) — download from https://git-lfs.github.com
# Linux
sudo apt install git-lfs

# Then in this repo:
git lfs install
git lfs track "*.pdf"   # already configured in .gitattributes
git add .gitattributes
```

Without LFS, push will fail at the 100 MB-per-file limit. Alternative: host the large PDFs as **GitHub Release assets** and link to them from the work README.

## Pushing to GitHub

```bash
cd "/Users/sc/Project Files/node-arcanum"

# 1. Create the empty repo on GitHub first (do this in the browser)
#    Suggested name: node-arcanum
#    Visibility: public

# 2. Connect local repo to GitHub
git remote add origin git@github.com:YOUR_USERNAME/node-arcanum.git

# 3. Initial commit + push
git add .
git commit -m "Initial public release: Shams al-Ma'arif (English + Arabic)"
git push -u origin main
```

## License

**Strict — All Rights Reserved, personal use only.** See [`LICENSE`](./LICENSE).

- You may read, print, and quote (with attribution) the translations for personal study
- You may NOT reproduce, publish, sell, or use commercially
- All rendered PDF pages are watermarked (`@nodedotshane · personal use only`, top-left) — the watermark is integral to the license
- Original Arabic source texts are public domain; the translations are not

## Attribution

Every work folder contains a `README.md` citing the source manuscript, the public-domain original, and any AI assistance used in the translation. The original Arabic/Latin/Greek source texts are not in this repo — only English renderings and supporting material.
