# biblatex-cse

*A BibLaTeX citation and bibliography style implementing the Council of Science Editors (CSE) Name–Year system.*

[![License: LPPL 1.3c](https://img.shields.io/badge/license-LPPL%201.3c-blue.svg)](https://www.latex-project.org/lppl/)
[![BibLaTeX](https://img.shields.io/badge/biblatex->=3.20-blue)](#)
[![Biber](https://img.shields.io/badge/biber->=2.17-blue)](#)
[![LaTeX](https://img.shields.io/badge/LaTeX-package-orange.svg)](https://www.ctan.org/pkg/biblatex-cse)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)](#)

---

## Overview

**`biblatex-cse`** provides a complete [BibLaTeX](https://ctan.org/pkg/biblatex) style that follows the  
[**Council of Science Editors (CSE)** Name–Year](https://www.councilscienceeditors.org/) citation system.

It produces in-text citations like:

```
(Fauci and Lane 2020)
(Haasnoot et al 2021, 1287–1290)
```

and reference lists formatted as:

```
Fauci AS, Lane HC. 2020. Four decades of HIV/AIDS—much accomplished, much to do.
N Engl J Med. 383(1):1–4. https://doi.org/10.1056/NEJMp1916753
```

---

## Contents

| File | Description |
|------|--------------|
| `biblatex-cse.bbx` | Bibliography formatting (reference list) |
| `biblatex-cse.cbx` | Citation formatting (in-text citations) |
| `biblatex-cse-doc.tex` | User manual (compilable LaTeX documentation) |
| `bibliography.bib` | Sample bibliography |

---

## Installation

### Automatic Installation

The `biblatex-cse` style files are distributed with `biblatex`.  This means that, most probably, `biblatex-cse` is already installed in your system. 

Follow the *Usage* instructins below.  
If you get the following error
`Package biblatex Error: Style 'biblatex-cse' not found.`
then do a *Manual Installation*.

### Manual Installation
Copy the files `biblatex-cse.bbx` and `biblatex-cse.cbx` to your working directory.  

### Requirements
- `biblatex` ≥ **3.20**
- `biber` ≥ **2.17**
- `csquotes` (optional, recommended)

---

## Usage

Add to your preamble:

```latex
\usepackage[backend=biber,style=biblatex-cse]{biblatex}
\addbibresource{bibliography.bib}
```

Compile with `pdflatex → biber → pdflatex → pdflatex` or with `latexmk -pdf`.

Example document:

```latex
\documentclass{article}
\usepackage[backend=biber,style=biblatex-cse]{biblatex}
\addbibresource{bibliography.bib}
\begin{document}

As shown in \textcite{Fauci2020}, ...
Recent studies confirm these results \parencite[45–47]{Lee2020a,Lee2020b}.

\printbibliography[title={References}]
\end{document}
```

---

## Citation examples

| Type | Example |
|------|----------|
| **Journal** | `Author(s). Year. Title. Journal title. Volume(issue):pages. DOI` |
| **Book** | `Author(s). Year. Title. Edition. Publisher.` |
| **Thesis** | `Author. Year. Title [dissertation]. Institution.` |
| **Online** | `Author. Year. Title. Publisher; [updated YYYY Mon DD; accessed YYYY Mon DD]. URL` |

---


## Options and Customization

The style inherits all BibLaTeX options. Common tweaks:

```latex
\ExecuteBibliographyOptions{
  giveninits=true,
  maxcitenames=2,
  maxbibnames=5,
  urldate=iso,
  dashed=false
}
```

To reduce the bibliography font size:
```latex
\AtBeginBibliography{\small}
```

To make the bibliography heading follow the style of a subsection header:
```latex
\defbibheading{bibliography}{\subsection*{#1}}
```

---

## Project structure

```
biblatex-cse/
├── biblatex-cse.bbx
├── biblatex-cse.cbx
├── biblatex-cse-doc.tex
├── bibliography.bib
└── README.md
```

---

##‍💻 Development

### Test installation

```bash
latexmk -pdf biblatex-cse-doc.tex
```

---

## License

Licensed under the [LaTeX Project Public License (LPPL) v1.3c](https://www.latex-project.org/lppl/).

---

## Acknowledgments

- [BibLaTeX](https://ctan.org/pkg/biblatex) by Philipp Lehman and Audrey Boruvka  
- *CSE Manual for Authors, Editors, and Publishers* (9th ed.)  
- The [Pygments](https://pygments.org) and [minted](https://ctan.org/pkg/minted) teams  

---

### ⭐ Contributions

Pull requests, bug reports, and suggestions are welcome!  
If you use **`biblatex-cse`**, please star ⭐ the repo or share improvements.

---

Copyright © 2024-25 João M. Lourenço.  
Crafted with 💙 for reproducible scientific writing.
