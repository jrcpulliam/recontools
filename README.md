
[![Build Status](https://travis-ci.org/reconhub/recontools.svg?branch=master)](https://travis-ci.org/reconhub/recontools) [![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/reconhub/recontools?branch=master&svg=true)](https://ci.appveyor.com/project/reconhub/recontools) [![Coverage Status](https://img.shields.io/codecov/c/github/reconhub/recontools/master.svg)](https://codecov.io/github/reconhub/recontools?branch=master) [![CRAN\_Status\_Badge](http://www.r-pkg.org/badges/version/recontools)](https://cran.r-project.org/package=recontools)

Tools to develop RECON packages
===============================

Installation
------------

### CRAN

Not yet on CRAN

### Development version

To install the most recent development version use:

``` r
devtools::install_github("reconhub/recontools")
```

What does it do?
----------------

### Package scaffolding

When starting a new RECON package, you can use `init_package` to quickly create default package structure:

``` r
# from within your session
recontools::init_package("mynewpackage")

# you can also set a specific path for the new package
recontools::init_package("mynewpackage", path = "my_new_package_dir")

# you can also disable the CRAN checks
recontools::init_package("mynewpackage", check_cran_name = FALSE)
```

In case you want to create a new package from the command line, run:

    Rscript -e "recontools::init_package('mynewpackage')"

Please note that this creates all optional components (like the MIT license).

`init_package` currently does the following:

-   Checks if the package name is valid and already taken on CRAN
-   Initializes a git repository, if not already present
-   Creates default `.Rbuildignore` and `.gitignore` files
-   Creates an `R` directory
-   Creates a default `DESCRIPTION` file
-   Adds an MIT License (asks for it)
-   Adds `testthat` tests
-   Adds a code of conduct (from the `devtools` package)
-   Creates a default `README.Rmd`
-   Creates a sample vignette (using the `devtools` package)
-   Adds travis CI + codecov (asks for it)
-   Adds appveyor (asks for it)
-   Adds a default `.lintr` file
-   Adds a `NEWS.md` file
-   Runs `devtools::document()` at the end

### Package checks
