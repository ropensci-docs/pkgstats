# Condense the output of `pkgstats` to summary statistics only

Condense the output of `pkgstats` to summary statistics only

## Usage

``` r
pkgstats_summary(s = NULL)
```

## Arguments

- s:

  Output of
  [pkgstats](https://docs.ropensci.org/pkgstats/reference/pkgstats.md),
  containing full statistical data on one package. Default of `NULL`
  returns a single row with `NA` values (used in
  [pkgstats_from_archive](https://docs.ropensci.org/pkgstats/reference/pkgstats_from_archive.md)).

## Value

Summarised version of `s`, as a single row of a standardised
`data.frame` object

## Note

Variable names in the summary object use the following abbreviations:

- "loc" = Lines-of-Code

- "fn" = Function

- "n_fns" = Number of functions

- "npars" = Number of parameters

- "doclines" = Number of documentation lines

- "nedges" = Number of edges in function call network, as a count of
  *unique* edges, which may be less than the size of the `network`
  object returned by
  [pkgstats](https://docs.ropensci.org/pkgstats/reference/pkgstats.md),
  because that may include multiple calls between identical function
  pairs.

- "n_clusters" = Number of connected clusters within the function call
  network.

- "centrality" used as a prefix for several statistics, along with "dir"
  or "undir" for centrality calculated on networks respectively
  constructed with directed or undirected edges; "mn" or "md" for
  respective measures of mean or median centrality, and "no0" for
  measures excluding edges with zero centrality.

## See also

Other stats:
[`desc_stats()`](https://docs.ropensci.org/pkgstats/reference/desc_stats.md),
[`loc_stats()`](https://docs.ropensci.org/pkgstats/reference/loc_stats.md),
[`pkgstats()`](https://docs.ropensci.org/pkgstats/reference/pkgstats.md),
[`rd_stats()`](https://docs.ropensci.org/pkgstats/reference/rd_stats.md)

## Examples

``` r
f <- system.file ("extdata", "pkgstats_9.9.tar.gz", package = "pkgstats")
if (FALSE) { # ctags_test(noerror = TRUE)
p <- pkgstats (f)
s <- pkgstats_summary (p)
}
```
