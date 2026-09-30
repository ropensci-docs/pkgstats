# Extract tarball of a package into temp directory and return path to extracted package

Extract tarball of a package into temp directory and return path to
extracted package

## Usage

``` r
extract_tarball(tarball, exdir = fs::path_temp())
```

## Arguments

- tarball:

  Full path to local tarball of an R package.

- exdir:

  Directory into which tarballs are to be extracted.

## Value

Path to extracted version of package (in
[`tempdir()`](https://rdrr.io/r/base/tempfile.html)).

## See also

Other misc:
[`pkgstats_fn_names()`](https://docs.ropensci.org/pkgstats/reference/pkgstats_fn_names.md)

## Examples

``` r
f <- system.file ("extdata", "pkgstats_9.9.tar.gz", package = "pkgstats")
path <- extract_tarball (f)
```
