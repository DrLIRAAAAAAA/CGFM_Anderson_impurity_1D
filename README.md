# Anderson impurity model (AIM) solver based on the cumulant Green's functions method (CGFM)

Solver for the Anderson impurity model (AIM) based on the cumulant Green's functions method (CGFM) (https://doi.org/10.1016/j.cpc.2025.109651).
The method is based on the iterative construction and exact diagonalization of a finite chain containing a single correlated impurity site connected to a chain of uncorrelated sites. The eigenvectors and eigenvalues of the finite chain are used to obtain the 
atomic Green's functions for the chain using the Lehmann representation. Using the cumulant expansion, the atomic cumulants are obtained from the atomic Green's functions. The atomic cumulants are then used as approximations to the full cumulants to calculate the Green's functions for 
the infinite chain limit.

### Pre-requisites and how to install them

- gfortran (https://fortran-lang.org/)

  `sudo apt-get install gfortran`
- LAPACK   (https://netlib.org/lapack/)

  `sudo apt-get install liblapack-dev`
- BLAS     (https://netlib.org/blas/)

  `sudo apt-get install libblas-dev `

### How to compile and run the code

- Compiling

  `gfortran -std=legacy -mcmodel=medium -o CGFM_Anderson_impurity_1D.exe CGFM_Anderson_impurity_1D.f90 -llapack -lblas`

  After compiling, the module files and the executable will be created.
  
- Running

  `nohup ./CGFM_Anderson_impurity_1D.exe > CGFM_Anderson_impurity_1D.out &`

  Using this command, the code runs in the background, freeing up the terminal. To check the execution status, use `top`.

  While running, the temporary files "fort.*" are created. They can be removed after the code is done running. After running, the output files containing the density of states and the occupations numbers are created.

### More details

Check the "README.md" inside the "CGFM_Anderson_impurity_1D" directory for a detailed description of the code parameters, variables, subroutines, functions, and output files.
