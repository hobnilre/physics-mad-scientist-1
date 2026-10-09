# Mad Scientist 1

Four apparatus investigations for COP greater than one

## What this article adds, and why it matters

Can a timed launch, switched transformer, contact chain or coupled-coil release
deliver more useful receiver work than all the energy supplied over a complete
cycle? These four investigations connect their motivating observations to that
COP question, with measured preparation, operation and actual reset.

Each OP receives two illustrated pages: background, observation and physical
idea, followed by a COP experiment with its own equation, input ports, receiver
measurement and control comparisons. Each experiment targets a repeatable COP
lower bound above one with independently checked machine states. A common energy
account defines gross input, useful output, return flow and uncertainty.

This is a local, unpublished draft. The PDF contains ten pages and eight figures:
an introduction, four two-page investigations, and the common measurement method.

<!-- article-tools:translations:start -->
<!-- article-tools:translations:end -->

## Article and build

[Read the article (PDF)](physics-mad-scientist-1.pdf) · [Manuscript source](physics-mad-scientist-1.md)

Install GNU Make, GNU Coreutils, Pandoc, XeLaTeX and the TeX Gyre fonts, including the LaTeX
packages used by `preamble.tex` and `preamble-local.tex` and the TikZ/PGFPlots standalone figures.
Run `make pdf` from this repository. It regenerates changed figures and builds
the article without any sibling repository or private working files.

The title date is the first version's creation date, pinned in `ARTICLE_DATE`
in the Makefile and retained in the manuscript's `date`. Keep both unchanged
when revising the article. The first page also gives the PDF creation time in UTC
and a planned GitHub destination, explicitly marked as unpublished.
An up-to-date PDF keeps its timestamp;
`make -B pdf` forces a rebuild. Intermediates go to ignored `build/` by default;
`BUILD_DIR=/absolute/path` selects another location. `make clean` removes that
build directory and keeps the article PDF and figure assets.

Shared typography is installed locally in `article-style.yaml`, `preamble.tex`
and `figures/figure-style.tex`. Article-specific definitions are in
`preamble-local.tex`. These files are complete build inputs; no tools checkout
is required.
