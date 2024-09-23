# crp2a.r-universe.dev

Most of the R packages of the laboratory are distributed on [CRAN](https://cran.r-project.org/), but some packages can only be installed from our universe: [crp2a.r-universe.dev](https://crp2a.r-universe.dev).

If available, CRAN releases must be regarded as the preferred source.

## Download tesselle packages

If you want to install a package, simply use `install.packages()` with the additional repository:

``` r
## Enable this universe
options(repos = c(CRAN = "https://cloud.r-project.org",
                  crp2a = "https://crp2a.r-universe.dev"))

## Install some packages
install.packages("gammaShiny")
```

## Use the repository

You can use this repository in your R package (always prefer the CRAN release if available). To do so, prepare the `DESCRIPTION` file of your R package:

* List the package under `Suggests:`
* Add the line `Additional_repositories: https://tesselle.r-universe.dev`
* Test your package with `R CMD check --as-cran`

