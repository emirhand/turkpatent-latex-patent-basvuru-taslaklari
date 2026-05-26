# Türkpatent LaTeX Template (Basic)

This repository provides a ready-to-use LaTeX template for drafting patent applications that strictly comply with **Türkpatent** (Turkish Patent and Trademark Office) formatting guidelines. It is designed with an academic directory structure to keep your workflow clean and organized.

## Features

This template automatically handles the formatting requirements mandated by Türkpatent, so inventors can focus on writing their application:
- **Page Margins**: Enforces Top 2-4 cm, Left 2.5-4 cm, Right 2-3 cm, and Bottom 2 cm for text pages [1]. Drawing pages (*Resimler*) automatically switch to Top/Left 2.5 cm, Right 1.5 cm, and Bottom 1 cm [1].
- **Line Spacing**: Enforces 1.5 line spacing across the text sections [2].
- **Line Numbering**: Automatically applies line numbers in increments of 5 for the *Tarifname* (Description) and *İstemler* (Claims) sections, while disabling them for drawings [1, 3].
- **Page Numbering**: Maintains continuous page numbering for text sections and automatically switches to a distinct `current/total` format (e.g., 1/3, 2/3) for the *Resimler* section [3, 4].
- **Section Breaks**: Ensures every main section starts on a new page automatically [2].

## Directory Structure

The project is organized to separate the LaTeX configuration from your actual patent prose:

├── main.tex                 # The root file to compile.
├── preamble.tex             # Contains packages, margin setups, and formatting rules.
└── bolumler/                # Subdirectory for your application prose.
    ├── 01-tarifname.tex     # TARİFNAME (Description) 
    ├── 02-istemler.tex      # İSTEMLER (Claims)
    ├── 03-ozet.tex          # ÖZET (Abstract)
    └── 04-resimler.tex      # RESİMLER (Drawings)


## How to Use

1. Clone this repository to your local machine.
2. Open `main.tex` in your preferred LaTeX editor (e.g., TeXstudio, Overleaf, or VS Code).
3. Fill in your patent details inside the respective `.tex` files located in the `chapters/` directory. Pre-filled standard headings (like *Teknik Alan*, *Önceki Teknik*) are provided in `01-tarifname.tex`.
4. Compile `main.tex` using pdfLaTeX or Latexmk.

