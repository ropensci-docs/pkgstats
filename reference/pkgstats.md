# Analyse statistics of one R package

Analyse statistics of one R package

## Usage

``` r
pkgstats(path = ".")
```

## Arguments

- path:

  Either a path to a local source repository, or a local '.tar.gz' file,
  containing code for an R package.

## Value

List of statistics and data on function call networks (or object
relationships in other languages). Includes the following components:

1.  loc: Summary of Lines-of-Code in all package directories

2.  vignettes: Numbers of vignettes and "demo" files

3.  data_stats: Statistics of numbers and sizes of package data files

4.  desc: Summary of contents of 'DESCRIPTION' file

5.  translations: List of translations into other (human) languages
    (where provides)

6.  objects: A `data.frame` of all functions in R, and all other objects
    (functions, classes, structures, global variables, and more) in all
    other languages

7.  network: A `data.frame` of object references within and between all
    languages; in R these are function calls, but may be more abstract
    in other languages.

8.  external_calls: A `data.frame` of all calls make to all functions
    from all other R packages, including base and recommended as well as
    contributed packages.

## See also

Other stats:
[`desc_stats()`](https://docs.ropensci.org/pkgstats/reference/desc_stats.md),
[`loc_stats()`](https://docs.ropensci.org/pkgstats/reference/loc_stats.md),
[`pkgstats_summary()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_summary.md),
[`rd_stats()`](https://docs.ropensci.org/pkgstats/reference/rd_stats.md)

## Examples

``` r
# 'path' can be path to a package tarball:
f <- system.file ("extdata", "pkgstats_9.9.tar.gz", package = "pkgstats")
if (FALSE) { # ctags_test(noerror = TRUE)
s <- pkgstats (f)
# or to a source directory:
path <- extract_tarball (f)
s <- pkgstats (path)
}
```
