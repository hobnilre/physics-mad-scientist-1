# Mad Scientist 1

Four apparatus investigations for COP greater than one

## What this article adds, and why it matters

Can a falling-weight lever deliver a receiver gain after its reset work is
measured? Where does the work go when a transformer changes taps or a coupled
coil releases into a load? How does a fast terminal mass in a contact chain
deliver work when every mass and spring is tracked?

This article combines two mechanical and two electrical investigations into one
ranked list: falling-weight lever, switched transformer, contact chain and
coupled-coil release. Each has one page for its apparatus, measurements, controls
and open questions. A common energy account follows preparation, driver supplies,
switching, relaxation and actual reset. The goal is to turn an exciting effect
into a complete result another experimenter can check.

This is a local, unpublished draft. The PDF contains six pages: an introduction,
four one-page investigations, and the common measurement method.

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
