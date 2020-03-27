
<!-- README.md is generated from README.Rmd. Please edit that file -->

# epichecks

<!-- badges: start -->

[![Travis build
status](https://travis-ci.org/R4IDSR/epichecks.svg?branch=master)](https://travis-ci.org/R4IDSR/epichecks)
[![AppVeyor build
status](https://ci.appveyor.com/api/projects/status/github/R4IDSR/epichecks?branch=master&svg=true)](https://ci.appveyor.com/project/R4IDSR/epichecks)
[![Codecov test
coverage](https://codecov.io/gh/R4IDSR/epichecks/branch/master/graph/badge.svg)](https://codecov.io/gh/R4IDSR/epichecks?branch=master)
[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
[![CRAN
status](https://www.r-pkg.org/badges/version/epichecks)](https://CRAN.R-project.org/package=epichecks)
<!-- badges: end -->

The goal of {epichecks} is to provide functions for simplifying data
quality checks and threshold analyses for IDSR data. The package further
contains helper functions that automate the production of feedback
documents for countries.

## Installation

Currently the package is not on CRAN. Once it is - you can install the
released version of epichecks from [CRAN](https://CRAN.R-project.org)
with:

``` r
# install.packages("epichecks")
```

In order to install the package you will first need to install an extra
bit of software called
[Rtools](https://cran.r-project.org/bin/windows/Rtools/).  
You can download the installer from:
<https://cran.r-project.org/bin/windows/Rtools/>  
Please install the version highlighted in green.

Once this is installed and you have restarted your computer, the
development version of the package can be installed from
[GitHub](https://github.com/) with:

``` r
install.packages("remotes")
remotes::install_github("R4IDSR/epichecks")
```

## Folder set up

In order for the funtions to work you need to have folders set up
correctly.

Create one main folder, in example called **WHO AFRO**.  
Within this folder create an R project (e.g. **WHO\_AFRO.Rproj**) -
*remember to open R through this project every time - to have the
correct root directory*.  
Within the **WHO AFRO** folder have a **Data** folder.  
The **Data** folder contains the *PHE dataset* and a **Processed**
folder which in turn has a folder for each calendar week.  
Place *IDSR data* for each country as *CSV* files in to the appropriate
calendar week folder.  
Within the **WHO AFRO** folder create an **Outputs** folder, and within
that a **Verification** folder. The package will create a folder for
each calendar week and place, for each country, an excel with flags and
a pdf letter with flags.

As an example:

<img src="man/figures/folder_layout.png"/>

## Getting started

Open your R project and type the below code.

This will produce outputs for week 35 of 2018 as an example. See
?week\_report for details of parameters that can be adjusted.

``` r
library(epichecks)
week_report(current_week = "2018-W35")
```

Please note that the ‘epichecks’ project is released with a [Contributor
Code of Conduct](.github/CODE_OF_CONDUCT.md). By contributing to this
project, you agree to abide by its terms.
