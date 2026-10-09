# Mad Scientist 1

Four simulation studies for COP greater than one

## What this article adds, and why it matters

Can a timed launch, switched transformer, contact chain or coupled-coil release
deliver more useful receiver work than all the energy supplied over a complete
cycle? These four proposed simulation studies connect their motivating
observations to that COP question through explicit dynamical models.

Each OP receives two illustrated pages, with background and observation flowing
into the simulation. State variables, contact or switching laws, receiver work,
all input ports and modeled reset define the calculation. Parameter comparisons,
exact reference cases and numerical checks make the resulting COP interpretable.
The common method distinguishes numerical error estimates, justified bounds and
uncertainty about component laws.

This is a local, unpublished draft. The PDF contains ten pages and eight figures:
an introduction, four two-page studies, and the common simulation account.
The studies are proposed work; the exact illustrations are analytic reference
cases, with no numerical simulation results reported.

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
