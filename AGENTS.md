# AGENTS.md

## Project Overview

This is a LaTeX academic paper: **"Dual View Knowledge Graph Explorer"** by Wolfgang Fahl. It uses the `llncs` document class (Springer LNCS proceedings format).

## Build

- **Build PDF**: `./scripts/tex2pdf`
- **Clean artifacts**: `./scripts/tex2pdf --clean`
- **Check dependencies**: `./scripts/tex2pdf --check`
- **CI**: GitHub Actions (`.github/workflows/build.yml`) auto-builds the PDF on push to `main` using the `texlive/texlive:latest` Docker image.

## Project Structure

- `main.tex` — Main LaTeX source
- `common.tex` — Shared preamble/definitions
- `references.bib` — BibTeX bibliography
- `llncs.cls` — LNCS document class
- `splncs04.bst` — LNCS bibliography style
- `images/` — Figures and images
- `scripts/tex2pdf` — Build script (pdflatex × 3 + bibtex)
- `main.pdf` — Pre-built PDF (auto-committed by CI)

## Conventions

- Use `\tquote{}` for inline quotes (defined in `common.tex`).
- Use `\wdq{label}{Q-id}` for Wikidata entity references.
- Follow LNCS formatting conventions.
- All edits go in `main.tex` or `common.tex`; bibliography entries in `references.bib`.