# Internal calculation of Lines-of-Code Statistics

Internal calculation of Lines-of-Code Statistics

## Usage

``` r
loc_stats(path)
```

## Arguments

- path:

  Directory to source code of package being analysed

## Value

A list of statistics for each of three directories, 'R', 'src', and
'inst/include', each one having 5 statistics of total numbers of lines,
numbers of empty lines, total numbers of white spaces, total numbers of
characters, and indentation used in files in that directory.

## Note

NA values are returned for directories which do not exist.

## See also

Other stats:
[`desc_stats()`](https://docs.ropensci.org/pkgstats/reference/desc_stats.md),
[`pkgstats()`](https://docs.ropensci.org/pkgstats/reference/pkgstats.md),
[`pkgstats_summary()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_summary.md),
[`rd_stats()`](https://docs.ropensci.org/pkgstats/reference/rd_stats.md)

## Examples

``` r
f <- system.file ("extdata", "pkgstats_9.9.tar.gz", package = "pkgstats")
# have to extract tarball to call function on source code:
path <- extract_tarball (f)
loc_stats (path)
#> # A tibble: 3 × 12
#> # Groups:   language, dir [3]
#>   language dir        nfiles nlines ncode  ndoc nempty nspaces nchars nexpr
#>   <chr>    <fs::path>  <int>  <int> <int> <int>  <int>   <int>  <int> <dbl>
#> 1 C++      src             3    365   277    21     67     933   7002     1
#> 2 R        R              19   3741  2698   536    507   27575  94022     1
#> 3 R        tests           7    348   266    10     72     770   6161     1
#> # ℹ 2 more variables: ntabs <int>, indentation <int>
```
