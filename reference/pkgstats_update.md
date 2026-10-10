# Update pkgstats\` data on GitHub release

This function is intended for internal rOpenSci use only. Usage by any
unauthorized users will error and have no effect unless run with
`upload = FALSE`, in which case updated data will be created in the
sub-directory "pkgstats-results" of R's current temporary directory.

## Usage

``` r
pkgstats_update(upload = TRUE)
```

## Arguments

- upload:

  If `TRUE`, upload updated results to GitHub release.

## Value

Local path to directory containing updated results.

## See also

Other archive:
[`dl_pkgstats_data()`](https://docs.ropensci.org/pkgstats/reference/dl_pkgstats_data.md),
[`pkgstats_cran_current_from_full()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_cran_current_from_full.md),
[`pkgstats_fns_from_archive()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_fns_from_archive.md),
[`pkgstats_fns_update()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_fns_update.md),
[`pkgstats_from_archive()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_from_archive.md)
