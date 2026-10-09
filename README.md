# Mad Scientist 1

Four conditional model results above event COP 1.15

## What this article adds, and why it matters

Four conditional event models exceed COP 1.15: a falling-weight lever, a
third-derivative contact law, a signed-residue active port and an unconstrained
fitted impedance. Their representative COPs are 1.188267, 1.570796, 17.920440
and 1.679922. Executed graphs, work tables, independent numerical checks and
prospective force/motion or voltage/current measurements make each prediction
concrete.

The lever reports the extra descent below its gravitational reference. The
other models retain their hypothetical internal energy accounts. The fitted
law is compared directly with its passive reference, whose matched COP is
0.247271; the fitted result is not attributed to that reference. Preparation,
reset and physical realization remain further questions.

The local draft has ten pages: an opening, exactly two pages per investigation,
and a common accounting page. Eight vector figures and five result tables
present 201 new integrations, including separate confirmation cases and
below-threshold controls. Instrument error budgets are prospective assumptions,
not measurements. The article remains unpublished.

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
