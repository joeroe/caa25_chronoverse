# The chronoverse – towards a common language for chronological modelling in R

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15388369.svg)](https://doi.org/10.5281/zenodo.15388369)

Joe Roe  
University of Copenhagen  
<https://joeroe.io>

This research compendium contains the slides, data and source code for a paper presented at the Computational and Quantitative Methods in Archaeology (CAA) conference in Athens, 6 May 2026. The paper was presented in session S1, "Chronological modelling II: formal methods and research software", convened by Eythan Levy and Thomas Huet.

The slides use [remark.js](https://remarkjs.com/#1) and are generated using [Quarto](https://quarto.org).
The source for the slide, including the R code used to generate the figures, is in `caa25_chronoverse.qmd`.
You will need to install the R packages listed at the top of the document to be able to preview or render it.

## How to view the slides

### Locally

`caa25_chronoverse.html` is a self-contained HTML document containing the slides.
To view them, download or clone it and open it in a web browser.

### Online

The slides can also be viewed online at <https://joeroe.io/caa25_chronoverse/>

Press `s` in the presentation window and see the speaker notes.

## Abstract

There are now quite a large number of R packages for chronological modelling (Marwick et al. 2023).
These include methods developed specifically by or for archaeologists as well as those borrowed from adjacent fields.
Many other types of analysis incorporate chronological data in an *ad hoc* way.
As the range and complexity of these analytic procedures increases, it is can be difficult to integrate the varied data types, interfaces, and output formats into a single workflow – to get different packages to "talk to each other".
This is a common problem, especially in decentralised software ecosystems such as R.
In other domains, the solution has often common in the form of computational 'infrastructure': packages that smooth the way by providing consistent formal representations, a common set of basic methods, and a predictable user interface patterns.

In this paper, I introduce three interconnected R packages:

* *era* provides formal representations of year-based time scales of the type usually used by archaeologists and other palaeoscientists (e.g. Before Present)
* *c14* facilitates 'tidy' analysis of radiocarbon data, including further formal classes for uncalibrated measurements and calibrated, calendar probability distributions, as well as functions for converting data types from existing radiocarbon-analysis packages into tidy formats
* *stratigraphr* is a framework for working with stratigraphies and relative chronologies as directed graphs, with tools for reading, analysing, and visualing these stratigraphic graphs ('Harris matrices')

As well as implementing various analytical methods, the aim of these packages is to provide a common infrastructure for the formal representation of chronological data and a set of consistent tools for reasoning with it.
All three make extensive use of tooling and design patterns from the *tidyverse* (Wickham 2019) to present a predictable user interface that fits into a wider ecosystem of R packages.
In particular, they use *vctrs*-based formalisms to represent different types of chronological vectors, a functional paradigm for composing programs, and assume/encourage the use of a tidy data workflow (Wickham 2014).

A common computational infrastructure for chronological data makes it easier to 'glue together' varied packages for chronological modelling within a single analysis.
And by linking it to an existing, widely-used paradigm (the *tidyverse*) we can take this further, smoothing the way for the integration of chronological data into a wide range of other methodologies.
The packages outlined here are not intended to be the definitive version of such an infrastructure but, I suggest, could serve as the rudiments of a common language for chronological modelling in R – a 'chronoverse'.

## References

* Marwick, Ben, Bjørn Peare Bartholdy, Nicolas Frerebeau, Sam Leggett, Sarah Pederzani, Joe Roe, Sophie C. Schmidt, et al. 2023. "CRAN Task View: Archaeology". <https://github.com/benmarwick/ctv-archaeology/blob/master/Archaeology.md>.
* Wickham, Hadley. 2014. "Tidy Data". *Journal of Statistical Software* 59 (10): 1–23. <https://doi.org/10.18637/jss.v059.i10>.
* Wickham, Hadley, Mara Averick, Jennifer Bryan, Winston Chang, Lucy D’Agostino McGowan, Romain François, Garrett Grolemund, et al. 2019. “Welcome to the Tidyverse.” *Journal of Open Source Software* 4 (43): 1686. <https://doi.org/10.21105/joss.01686>.

## License

[CC BY 4.0 International](https://creativecommons.org/licenses/by/4.0/). Copyright Joe Roe 2025.

