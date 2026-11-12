# Download latest version of 'pkgstats' data

Download latest version of 'pkgstats' data

## Usage

``` r
dl_pkgstats_data(current = TRUE, path = tempdir(), quiet = FALSE)
```

## Arguments

- current:

  If 'FALSE', download data for all CRAN packages ever released,
  otherwise (default) download data only for current CRAN packages.

- path:

  Local path to download file.

- quiet:

  If `FALSE`, display progress information on screen.

## Value

(Invisibly) A `data.frame` of `pkgstats` results, one row for each
package.

## See also

Other archive:
[`pkgstats_cran_current_from_full()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_cran_current_from_full.md),
[`pkgstats_fns_from_archive()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_fns_from_archive.md),
[`pkgstats_fns_update()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_fns_update.md),
[`pkgstats_from_archive()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_from_archive.md),
[`pkgstats_update()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_update.md)
