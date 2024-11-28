# qqman: An R package for creating Q-Q and manhattan plots from GWAS results.

## Note
This is a forked version of the original package qqman to allow me (Carmelo Fruciano) a little bit of a different output (e.g., setting the colour of highlighted markers).
Defaults correspond to the original implementation.


[![CRAN_Status_Badge](https://www.r-pkg.org/badges/version/qqman)](https://cran.r-project.org/package=qqman)

[![DOI](https://joss.theoj.org/papers/10.21105/joss.00731/status.svg)](https://doi.org/10.21105/joss.00731)

![qqman.gif](tools/qqman.gif)


## Citation

If you'd like to cite qqman (appreciated but not required), please cite the publication below:

Turner, (2018). qqman: an R package for visualizing GWAS results using Q-Q and manhattan plots. _Journal of Open Source Software_, 3(25), 731, https://doi.org/10.21105/joss.00731

More details are found in the preprint:

Turner, S.D. qqman: an R package for visualizing GWAS results using Q-Q and manhattan plots. [*biorXiv* DOI: 10.1101/005165](https://biorxiv.org/content/early/2014/05/14/005165).

## Installation

Install the stable release from CRAN:

```r
install.packages("qqman")
```

Or install directly from github using devtools

```r
library(devtools)
install_github("stephenturner/qqman")
```

Or install the most recent development release with devtools (note, there be dragons here):

```r
library(devtools)
install_github("stephenturner/qqman", ref="dev")
```

Load the package each time you use it:

```r
library(qqman)
```

## Usage

See the [online package vignette](https://cran.r-project.org/package=qqman/vignettes/qqman.html) for more examples:

```r
browseVignettes("qqman")
```

Take a look at the built-in data:

```r
head(gwasResults)
```

Basic manhattan plot using built-in data:

```r
manhattan(gwasResults)
```

Basic Q-Q plot using built-in data:

```r
qq(gwasResults$P)
```

Get help:

```r
?manhattan
?qq
```

## Notes

* This release is substantially simplified for the sake of maintainability and creating an R package. The old code that allows confidence intervals on the Q-Q plot and allows more flexible annotation and highlighting is still available at the [version 0.0.0 tag](https://github.com/stephenturner/qqman/tree/v0.0.0).
* Special thanks to Dan Capurso and Tim Knutsen for useful contributions and bugfixes.
* Thanks to all the blog commenters for pointing out bugs and other issues.
