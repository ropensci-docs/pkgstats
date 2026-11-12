# Statistics from DESCRIPTION files

Statistics from DESCRIPTION files

## Usage

``` r
desc_stats(path)
```

## Arguments

- path:

  Directory to source code of package being analysed

## Value

A `data.frame` with one row and 16 columns extracting various
information from the 'DESCRIPTION' file, include websites, tallies of
different kinds of authors and contributors, and package dependencies.

## See also

Other stats:
[`loc_stats()`](https://docs.ropensci.org/pkgstats/reference/loc_stats.md),
[`pkgstats()`](https://docs.ropensci.org/pkgstats/reference/pkgstats.md),
[`pkgstats_summary()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_summary.md),
[`rd_stats()`](https://docs.ropensci.org/pkgstats/reference/rd_stats.md)

## Examples

``` r
f <- system.file ("extdata", "pkgstats_9.9.tar.gz", package = "pkgstats")
# have to extract tarball to call function on source code:
path <- extract_tarball (f)
desc_stats (path)
#>    package version                date license
#> 1 pkgstats     9.9 2022-05-12 09:41:22   GPL-3
#>                                                                                      urls
#> 1 https://docs.ropensci.org/pkgstats/,\nhttps://github.com/ropensci-review-tools/pkgstats
#>                                                       bugs aut ctb fnd rev ths
#> 1 https://github.com/ropensci-review-tools/pkgstats/issues   1   0   0   0   0
#>   trl depends                                                        imports
#> 1   0      NA brio, checkmate, dplyr, fs, igraph, methods, readr, sys, withr
#>                                                                         suggests
#> 1 hms, knitr, pbapply, pkgbuild, Rcpp, rmarkdown, roxygen2, testthat, visNetwork
#>   enhances linking_to
#> 1       NA      cpp11
```
