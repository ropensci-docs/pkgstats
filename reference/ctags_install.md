# Install 'ctags' from a clone of the 'git' repository

'ctags' is installed with this package on both Windows and macOS
systems; this is an additional function to install from source on Unix
systems.

## Usage

``` r
ctags_install(bin_dir = NULL, sudo = TRUE)
```

## Arguments

- bin_dir:

  This parameter only has an effect on \*nix-type operating systems
  (such as Linux), on which it's a prefix to pass to the `autoconf`
  configure command defining location to install the binary, with
  default of `/usr/local`.

- sudo:

  Set to `FALSE` if `sudo` is not available, in which case a value for
  `bin_dir` will also have to be explicitly specified, and be a location
  where a binary is able to be installed without `sudo` privileges.

## Value

Nothing; the function will fail if installation fails, otherwise returns
nothing.

## See also

Other tags:
[`ctags_test()`](https://docs.ropensci.org/pkgstats/reference/ctags_test.md),
[`tags_data()`](https://docs.ropensci.org/pkgstats/reference/tags_data.md)

## Examples

``` r
if (FALSE) { # \dontrun{
ctags_install (bin_dir = "/usr/local") # default Linux location.
} # }
```
