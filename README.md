# Description
This directory contains the IRA and CShDA algorithms implemented in Fortran.
Further descriptions of these algorithms are given in [[1]](#1) and [[2]](#2). 

# Iterative Rotations and Assignments (IRA)
The Iterative Rotations and Assignments (IRA) algorithm is a shape matching
algorithm for matching generic atomic structures, including structures with
different number of atoms.

# Constrained Shortest Distance Assignment (CShDA)
The Constrained Shortest Distance Assignment (CShDA) algorithm is a Linear
Assignment Problem (LAP) solver, which is used by the IRA algorithm. 

# Files
Routine files:

 - cshda.f90 contains the CShDA routine for pbc and non-pbc cases.
 - ira_routines.f90 contains all the routines specific to IRA.
 - read_typ.f90 contains a function to read atomic types from xyz format.
 - sorting_module.f90 contains the mergesort algorithm.

# Compile and run
TO COMPILE: (you need lapack library, see the Makefile)

   `make all`
THEN:
   `./compile.sh`

TO RUN:

   `./compare_catalog.x input output > state`

## References
<a id="1">[1]</a> 
Gunde M., Salles N., Hemeryck A., Martin Samos L.
*IRA: A shape matching approach for recognition and comparison of generic atomic patterns*,
Journal of Chemical Information and Modeling (2021), DOI: [https://doi.org/10.1021/acs.jcim.1c00567](https://doi.org/10.1021/acs.jcim.1c00567), HAL: [hal-03406717](https://hal.laas.fr/hal-03406717), arXiv: [2111.00939](https://export.arxiv.org/abs/2111.00939)

<a id="2">[2]</a>
Gunde M.: *Development of IRA: a shape matching algorithm, its implementation
and utility in a general off-lattice kMC kernel*, PhD dissertation,
November 2021.
[PDF link](http://thesesups.ups-tlse.fr/5109/1/2021TOU30132.pdf) 
