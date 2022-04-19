# integer_matrix_approximation (IMA)

This repository contains an implementation of an approximation of integer matrix factorization in `python` and `R`.

The code here is based directly off of the implementation in `MATLAB`, named `SUSTain` and available [here](https://github.com/kperros/SUSTain)

The scripts contain the minimum functionality required to apply IMA to a 2-dimensional matrix of natural numbers (inclusive of 0). Additional functionality is available in the `MATLAB` implementation, e.g. expanding IMA to tensors or allowing other forms of discrete data. 

We welcome forks of this repository that expand or optimize this code for `python` and `R`.

## Installation

### python

To prepare a conda environment and install countland (before first use):

    conda create -n IMA -c conda-forge
    conda activate IMA
    pip install git+https://github.com/shchurch/integer_matrix_approximation.git#subdirectory=IMA-python

To activate the conda environment (before each use):

    conda activate IMA

### R

From an R prompt, run the following: 

    library(devtools)
    install_github("shchurch/integer_matrix_approximation", subdir="IMA-R")

## Development

### python

To install from local source:

    conda create -n IMA -c conda-forge python==3.10
    conda activate IMA
    cd IMA-python
    pip install .[dev]

### R

This package is built with the excellent [devtools](https://github.com/hadley/devtools). Extensive explanations on using devtools
to create R packages is available in the book
[R Packages](http://r-pkgs.had.co.nz/).

Development typically involves `cd`ing to the package directory `IMA-R/`, launching R, and running some combination of the following:

	options(error=traceback) # Get line numbers for errors
    library(devtools)
    devtools::load_all()
    devtools::document()
    devtools::check() # A wrapper for R CMD check, see http://r-pkgs.had.co.nz/check.html#check
    devtools::build() # Create package bundle, including executed vignettes

