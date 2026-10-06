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
```

The number and instructor fields are optional: fill them in and they
appear; leave the braces empty and they're omitted. A typical workflow
is to set these once per class and hand students the folder.

## What's in this folder

| File | What it is |
|---|---|
| `L42i_paper_template.tex` | **The template.** Your paper, plus the COURSE INFO block at the top. |
| `L42i_paper_template.bib` | The bibliography — add your sources here. |
| `figures/` | Put images here (a placeholder diagram is included). |
| `acmart.cls` | The document style. Don't edit. |
| `ACM-Reference-Format.bst` | The citation style. Don't edit. |
| `NOTICE.txt` | Attribution and license notes (see below). |

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

## A note on structure

The sections in `L42i_paper_template.tex` (Introduction, Background, System Design,
Implementation, Performance, Discussion, Conclusion) are a **suggestion**
for a project paper. Rename, reorder, or replace them to fit the
assignment.

## License and attribution

This template is derived from the ACM `acmart` template by Boris Veytsman.
The `acmart` class is under the LaTeX Project Public License (LPPL) v1.3c,
and `ACM-Reference-Format.bst` is public domain. `L42i_paper_template.tex` is a modified
version of the `acmart` sample `sigconf.tex`, renamed and adapted for
course use as the LPPL requires. Full details are in `NOTICE.txt`.

(Note: `acmart` is *not* Creative Commons — it's LPPL.)
