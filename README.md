
<!-- README.md is generated from README.Rmd. Please edit that file -->

# [**nloptr**](https://astamm.github.io/nloptr/) <img src='man/figures/logo.png' align="right" height="139" />

<!-- badges: start -->

[![R-CMD-check](https://github.com/astamm/nloptr/workflows/R-CMD-check/badge.svg)](https://github.com/astamm/nloptr/actions)
[![test-coverage](https://github.com/astamm/nloptr/workflows/test-coverage/badge.svg)](https://github.com/astamm/nloptr/actions)
[![Codecov test
coverage](https://codecov.io/gh/astamm/nloptr/branch/master/graph/badge.svg)](https://app.codecov.io/gh/astamm/nloptr?branch=master)
[![pkgdown](https://github.com/astamm/nloptr/workflows/pkgdown/badge.svg)](https://github.com/astamm/nloptr/actions)
[![CRAN
status](https://www.r-pkg.org/badges/version/nloptr)](https://CRAN.R-project.org/package=nloptr)
<!-- badges: end -->

[**nloptr**](https://astamm.github.io/nloptr/) is an R interface to
[NLopt](https://nlopt.readthedocs.io/en/latest/), a free/open-source
library for nonlinear optimization started by Steven G. Johnson,
providing a common interface for a number of different free optimization
routines available online as well as original implementations of various
other algorithms. It can be used to solve general nonlinear programming
problems with nonlinear constraints and lower and upper bounds for the
controls, such as

min<sub>*x* ∈ ℝ<sup>*n*</sup></sub>  *f*(*x*),

s.t. *g*(*x*) ≤ 0, *h*(*x*) = 0 and ℓ ≤ *x* ≤ *u*.

The [NLopt](https://nlopt.readthedocs.io/en/latest/) library is
available under the GNU Lesser General Public License (LGPL), and the
copyrights are owned by a variety of authors. See the
[website](https://nlopt.readthedocs.io/en/latest/Citing_NLopt/) for
information on how to cite NLopt and the algorithms you use.

## Installation

### Installing [CMake](https://cmake.org)

The [NLopt](https://nlopt.readthedocs.io/en/latest/) library has
switched to [CMake](https://cmake.org) for its build system.
Consequently, we updated the
[**nloptr**](https://astamm.github.io/nloptr/) package accordingly. This
means that [CMake](https://cmake.org) is now a system requirement. You
can install it by following [CMake installation
instructions](https://cmake.org/install/).

The important thing is that you add the [CMake](https://cmake.org)
binary to your `PATH`:

-   On Windows, the installer has an option to modify the system `PATH`
    environment variable. If that is not selected, please select it.
-   On macOS, you can install [CMake](https://cmake.org) and then run
    it. In the menu bar, there is an item *How to Install For Command
    Line Use* which you can click on to have proper instructions on how
    to update your `PATH`. Note that the location of the
    [CMake](https://cmake.org) binary is always
    `/Applications/CMake.app/Contents/bin/cmake`. Hence,
    [**nloptr**](https://astamm.github.io/nloptr/) knows where to find
    it even if you do not update your `PATH`.
-   On Linux, it will be automatically added unless you specifically
    change the default installation directory before building
    [CMake](https://cmake.org).

Alternatively, you can set an environment variable `CMAKE_BIN` pointing
to a [CMake](https://cmake.org) binary of your liking on your computer
for [**nloptr**](https://astamm.github.io/nloptr/) to use.

### Installing [**nloptr**](https://astamm.github.io/nloptr/)

You can install [**nloptr**](https://astamm.github.io/nloptr/) from CRAN
using:

    install.packages("nloptr")

Alternatively, you can install the development version from GitHub:

    # install.packages("remotes")
    remotes::install_github("astamm/nloptr")

The latest version 2.7.0 of the
[NLopt](https://nlopt.readthedocs.io/en/latest/) library will then be
automatically built using [CMake](https://cmake.org).

## Acknowledgments

I would like to express my sincere gratitude to [Dirk
Eddelbuettel](https://github.com/eddelbuettel), Uwe Ligges and [Jelmer
Ypma](https://github.com/jyypma) for the very instructive discussions
about the pros and cons of various build strategies in R packages.

## Reference

Steven G. Johnson, The NLopt nonlinear-optimization package,
<https://nlopt.readthedocs.io/en/latest/>
