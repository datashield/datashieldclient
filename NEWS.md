# devtools 1.5.0.99

## The release process

* You can add arbitrary extra questions to `release()` by defining a function 
  `release_questions()` in your package. Your `release_questions()` should 
  return a character vector of questions to ask (#451). 

* `release()` uses new CRAN submission process, as implemented by 
  `submit_cran()` (#430).

## Tool templates and `create()`

* `create()` no longer generates `man/` directory - roxygen2 now does
  this automatically. It also no longer generates an package-level doc
  template, instead call `use_package_doc()`.

* New `use_data()` makes it easy to include data in a package, either 
  in `data/` (for exported datasets) or in `R/sysdata.rda` (for internal
  data). (#542)
  
* New `use_data_raw()` to create `data-raw/` directory for reproducible
  generation of `data/` files (#541).

* New `use_rcpp()` sets up a package to use Rcpp.

* New `use_knitr()` sets up a package to use knitr for vignettes.

* New `use_package()` allows you to set dependencies (#559). 

* New `use_package_doc()` sets up an Roxygen template for package-level
  docs.

* New function `install_svn()` to install an R package from a subversion
  repository.

* Wrote own version of `write.dcf()` that doesn't butcher whitespace and 
  fieldnames.

* renamed `add_rstudio_project()` to `use_rstudio()`, `add_travis()` to 
  `use_travis()`, `add_build_ignore()` to `use_build_ignore()`, and 
  `add_test_infrastructure()` to `use_testthat()` (old functions are 
  aliased to new)
  
* `use_travis()` now figures out what your github username and repo are so
  it can construct the markdown build image for you. (#546)

* `create()` now makes a dummy namespace so that you can build & reload
  without running `document()` first.

## Package installation

* All `install_*` now use the same code and store much useful metadata.
  Currently only `session_info()` takes advantage of this information,
  but it will allow the development of future tools like generic update
  functions.
  
* `install_bitbucket()` has been bought into alignment with `install_github()`:
  this means you can now specify repos with the compact `username/repo@ref`
  syntax. The `username` is now deprecated. 
