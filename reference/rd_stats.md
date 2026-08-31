# Stats from '.Rd' files

Stats from '.Rd' files

## Usage

``` r
rd_stats(path)
```

## Arguments

- path:

  Directory to source code of package being analysed

## Value

A `data.frame` of function names and numbers of parameters and lines of
documentation for each, along with mean and median numbers of characters
used to document each parameter.

## See also

Other stats:
[`desc_stats()`](https://docs.ropensci.org/pkgstats/reference/desc_stats.md),
[`loc_stats()`](https://docs.ropensci.org/pkgstats/reference/loc_stats.md),
[`pkgstats()`](https://docs.ropensci.org/pkgstats/reference/pkgstats.md),
[`pkgstats_summary()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_summary.md)

## Examples

``` r
f <- system.file ("extdata", "pkgstats_9.9.tar.gz", package = "pkgstats")
# have to extract tarball to call function on source code:
path <- extract_tarball (f)
rd_stats (path)
#>                  fn_name num_params num_doclines param_nchars_mn
#> 1          ctags_install          2           23       157.00000
#> 2             ctags_test          1           22        73.00000
#> 3             desc_stats          1           26        35.00000
#> 4        extract_tarball          1           25        43.00000
#> 5              loc_stats          1           34        35.00000
#> 6               pkgstats          1           45       103.00000
#> 7  pkgstats_from_archive          7           49       174.85714
#> 8       pkgstats_summary          1           50       153.00000
#> 9           plot_network          3           34        78.33333
#> 10              rd_stats          1           26        35.00000
#> 11             tags_data          3           31       105.66667
#>    param_nchars_md
#> 1              157
#> 2               73
#> 3               35
#> 4               43
#> 5               35
#> 6              103
#> 7              163
#> 8              153
#> 9               83
#> 10              35
#> 11              69
```
