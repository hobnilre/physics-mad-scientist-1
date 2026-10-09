# Mad Scientist 1

Four calculated leads toward COP greater than one

## What this article adds, and why it matters

The article reports executed simulations of a falling-weight lever, switched
transformer, contact chain and coil release. It follows preparation, useful
receiver delivery and reset, with 86 explored parameter cases, numerical graphs,
work tables and independently checked leading results.

The lever reaches an operating-window output/input ratio of 1.1666 and a
complete-history COP of 0.9951. Transformer commutation reduces gross input by
6.90% at matched receiver delivery. Gap and release choices produce substantial
changes in useful output. The complete accounts connect those gains to the
continuing search for COP greater than one; none of the tested models has an
above-one complete-history COP.

This local, unpublished draft has ten pages: an introduction, four continuous
two-page treatments, and a shared account of the results and numerical checks.
Eight figures include exact observation references and four computed result
figures; five tables report calculated comparisons. Numerical plotting data are
embedded in the LaTeX figure inputs. No hardware measurements are reported.

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
