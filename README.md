# MPI_LASSO_Example

This project is an simple example to demonstrate the usage of MPI for numerical computing.
It implements a distributd alternating direction method of multipliers (ADMM) algorithm for solving lasso problem. 

## Pre-requirement

This repository provide implementations in three languages:
- C. The C implementation requires [GNU Scientific Library (GSL)](http://www.gnu.org/software/gsl/) and Open MPI (or other MPI implementation).
- Python. The python version requires Numpy/SciPy and [MPI4Py](http://mpi4py.scipy.org/).
- Lua. The Lua version is implemented based on [Torch7](http://torch.ch/) with [MPIT](https://github.com/sixin-zh/mpiT).

## How to run it

### Run on local machine

C version
> make

> make run

Python version
> make runpy

Lua version 
> make runlua

### Run on TACC Stampede

C version
> make clean; make

> sbatch my_c_lasso_job

Python version
> sbatch my_py_lasso_job

Lua version 
> sbatch my_lua_lasso_job

**Note:** Here assumes Torch7 is installed in $HOME/torch/install.


## Acknowledgement

The c implementation is from [here](https://web.stanford.edu/~boyd/papers/admm/mpi/).
