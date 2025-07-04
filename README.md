
# STIMA-exampleData

This repository contains example data used in the vignettes and
replication scripts of the [STIMA](https://github.com/vagm110901/STIMA)
R package.

## Contents

The `inst/extdata/exampleData/` directory includes compressed datasets
(`.zip`) and `.RDS` file required to reproduce the analyses and figures
described in the package
[vignettes](https://github.com/vagm110901/STIMA/tree/master/vignettes).

These datasets are primarily derived from:

- [Yadav et al. (2023)](https://doi.org/10.1016/j.neuron.2023.01.007).
- GEO:
  [GSE190442](http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE190442).
- GEO:
  [GSE222322](http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE222322).

## Usage

This repository is not intended to be installed as an R package.
Instead, it is used as a remote data source.

To download specific files programmatically from R, you can use:

``` r
file_url <- "https://github.com/vagm110901/STIMA-exampleData/raw/refs/heads/master/inst/extdata/exampleData/File.rds"
utils::download.file(file_url, destfile = "YourFile.rds", mode = "wb")
```

or

``` r
zip_url <- "https://github.com/vagm110901/STIMA-exampleData/raw/refs/heads/master/inst/extdata/exampleData/File.zip"
utils::download.file(zip_url, destfile = "YourFile.zip", mode = "wb")
utils::unzip("YourFile.zip", exdir = "YourFolder")
file.remove("YourFile.zip")
```
