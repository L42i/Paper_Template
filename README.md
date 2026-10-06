# Course Paper Template

A reusable LaTeX template for course project papers, built on the ACM
`acmart` class. Clean two-column layout, automatic citations, and worked
examples of figures, tables, and equations — with all ACM copyright and
submission machinery stripped out.

The template ships configured for **Technology Ensemble, Fall 2026,
Georgia Institute of Technology, School of Music**, but it is
course-neutral: point it at any class by editing one file.

## Reusing this for another course

Edit the **COURSE INFO** block near the top of `L42i_paper_template.tex` and change the
values. The course line on the paper updates automatically.

```latex
\newcommand{\coursename}{Technology Ensemble}
\newcommand{\coursenumber}{}          % optional — leave empty to hide
\newcommand{\courseterm}{Fall}
\newcommand{\courseyear}{2026}
\newcommand{\courseinstitution}{Georgia Institute of Technology}
\newcommand{\coursedepartment}{School of Music}
\newcommand{\courseinstructor}{}       % optional — leave empty to hide
\newcommand{\pageheadertext}{Georgia Tech \textbullet\ School of Music}
```

The number and instructor fields are optional: fill them in and they
appear; leave the braces empty and they're omitted. `\pageheadertext`
sets the running header at the top of every page — change it, or set it
empty to turn the header off. A typical workflow is to set these once per
class and hand students the folder.

## What's in this folder

| File | What it is |
|---|---|
| `L42i_paper_template.tex` | **The template.** Your paper, plus the COURSE INFO block at the top. |
| `L42i_paper_template.bib` | The bibliography — add your sources here. |
| `figures/` | Put images here (a placeholder diagram is included). |
| `acmart.cls` | The document style. Don't edit. |
| `ACM-Reference-Format.bst` | The citation style. Don't edit. |
| `NOTICE.txt` | Attribution breakdown (see below). |
| `LICENSE` | The template's license (LPPL v1.3c). |

## Getting started on Overleaf (recommended)

1. Zip this whole folder (or upload the zip you were given).
2. On [overleaf.com](https://www.overleaf.com): **New Project → Upload Project**.
3. Open `L42i_paper_template.tex` and press **Recompile**.
4. Make sure the compiler is **pdfLaTeX** (Menu → Settings). It usually is by default.

## Compiling on your own computer

You'll need a LaTeX installation (TeX Live, MacTeX, or MiKTeX). Then from
this folder:

```
latexmk -pdf L42i_paper_template.tex
```

## The three things people always ask

**Add a figure** — put the image in `figures/`, then:

```latex
\begin{figure}[h]
  \centering
  \includegraphics[width=\columnwidth]{figures/your-image}
  \caption{What the figure shows.}
  \Description{Plain-language description for accessibility.}
  \label{fig:mything}
\end{figure}
```

Refer to it in text with `Figure~\ref{fig:mything}`.

**Cite a source** — add an entry to `L42i_paper_template.bib`, then write
`\cite{thekey}` in your text. There are worked examples of a conference
paper, a book, a journal article, and software in that file.

**Add an equation** —

```latex
\begin{equation}
  a = g^{2}.
\end{equation}
```

**Add code** — a short snippet inside a sentence uses `\lstinline|code|`;
a block uses the `lstlisting` environment (it can be captioned and
referenced like a figure). The listings setup is in the preamble; its
default language is SuperCollider — change the keyword list there, or set
`language=Python` (etc.) in `\lstset`, to suit your course.

## Placeholder text

The body ships filled with `\lipsum[..]` ("Lorem ipsum") placeholder text,
so the template looks the same for any class. Replace each `\lipsum[..]`
with your own writing — the short comment above each section says what
belongs there. Once no `\lipsum` remains, you can delete the
`\usepackage{lipsum}` line near the top.

## A note on structure

The body ships as a set of "Example Section" demos — Citations, Figures,
Equations, Tables, and Code — each pairing placeholder prose with one
working example of that mechanic. Rename, reorder, merge, or replace the
sections to fit the assignment; reuse the mechanics, swap in your own
content.

## License and attribution

This template is licensed under the **LaTeX Project Public License (LPPL)
v1.3c or later** — see the `LICENSE` file. It is a modified version of the
ACM `acmart` sample `sigconf.tex` by Boris Veytsman, renamed and marked as
modified as the LPPL requires; modifications © 2026 Henrik von Coler / L42i.

The bundled `acmart.cls` (LPPL v1.3c) and `ACM-Reference-Format.bst`
(public domain) are redistributed unmodified under their own terms. Full
attribution is in `NOTICE.txt`.

(Note: `acmart` is *not* Creative Commons — it's LPPL.)
