## This is the eighth resubmission

* Updates since previous submission:
  * Updated `spatstat` package to new subsetted packages based on feedback from the Spatstat Team (Adrian Baddeley and Ege Rubak). Now `spatstat.geom`, `spatstat.core`, `spatstat.linnet`, and `spatstat (>= 2.0-0)` are in Depends
  * Replaced `parallel` and `doParallel` packages in Imports with `doFuture`, `doRNG`, and `future` packages to allow for parallel processing in `lrren()` and `perlrren()` functions to work across all CRAN environments
  * Removed `utils` package from Imports because the progress bar in `lrren()` and `perlrren()` functions is now produced with a helper function in utils.R that imports the `iterators` package
  * Set default for `n_core` argument in `lrren()` and `perlrren()` to be `n_core = 2` to match documentation
  * Fixed bug in `pval_correct()` when `p_correct = "FDR"` that will return the minimum p-value instead of NULL if no p-value is less than the p-critical value
  * Updated testthat checks for parallelization in `lrren()` and `perlrren()` functions
  
* Documentation for `pval_correct()` references a doi <https://doi.org/10.2307/2283989> that throws a NOTE in win-builder but no other environment

## Test environments
* local OS X install, R 4.0.4
* win-builder, (devel, oldrelease, release)
* Rhub
  * Fedora Linux, R-devel, clang, gfortran
  * Ubuntu Linux 16.04 LTS, R-release, GCC
  * Windows Server 2008 R2 SP1, R-devel, 32⁄64 bit

## R CMD check results
0 errors | 0 warnings | 0 notes

## Submitted by Maintainer
