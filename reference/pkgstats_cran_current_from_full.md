# Reduce `data.frame` of full CRAN archive data to current packages only.

Reduce `data.frame` of full CRAN archive data to current packages only.

## Usage

``` r
pkgstats_cran_current_from_full(prev_results, results_file = NULL)
```

## Arguments

- prev_results:

  Result of previous call to this function, if available. Submitting
  previous results will ensure that only newer packages not present in
  previous result will be analysed, with new results simply appended to
  previous results. This parameter can also specify a file to be read
  with [`readRDS()`](https://rdrr.io/r/base/readRDS.html).

- results_file:

  Can be used to specify the name or full path of a `.Rds` file to which
  results should be saved once they have been generated. The '.Rds'
  extension will be automatically appended, and any other extensions
  will be ignored.

## Value

A `data.frame` object with one row for each package containing summary
statistics generated from the
[pkgstats_summary](https://docs.ropensci.org/pkgstats/reference/pkgstats_summary.md)
function.

## See also

Other archive:
[`dl_pkgstats_data()`](https://docs.ropensci.org/pkgstats/reference/dl_pkgstats_data.md),
[`pkgstats_fns_from_archive()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_fns_from_archive.md),
[`pkgstats_fns_update()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_fns_update.md),
[`pkgstats_from_archive()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_from_archive.md),
[`pkgstats_update()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_update.md)
