# test a 'ctags' installation

This uses the example from
<https://github.com/universal-ctags/ctags/blob/master/man/ctags-lang-r.7.rst.in>
and also checks the GNU global installation.

## Usage

``` r
ctags_test(quiet = TRUE, noerror = FALSE)
```

## Arguments

- quiet:

  If `TRUE`, display on screen whether or not 'ctags' is correctly
  installed.

- noerror:

  If `FALSE` (default), this function will error if either 'ctags' or
  'gtags' are not installed. If `TRUE`, the function will complete
  without erroring, and issue appropriate messages regarding required
  but non-installed system libraries.

## Value

'TRUE' or 'FALSE' respectively indicating whether or not 'ctags' is
correctly installed.

## See also

Other tags:
[`ctags_install()`](https://docs.ropensci.org/pkgstats/reference/ctags_install.md),
[`tags_data()`](https://docs.ropensci.org/pkgstats/reference/tags_data.md)

## Examples

``` r
# The function errors if not ctags or gtags found.
# \donttest{
ctags_okay <- !is.null (tryCatch (
    ctags_test (),
    error = function (e) NULL
))
# }
```
