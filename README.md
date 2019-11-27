# RKDGV1D3V 
# 1D3V Solver for the kinetic Boltzmann equation

Contributors: Alex Aleskeenko, Jeffrey Limbacher, Truong Nguyen, Craig Euler

E-mail: alexander.alekseenko@csun.edu

This is a copy of a Fortran code that implements solution of the Boltzmann equation in one spatial dimension using nodal-discontinuous 
Galerkin discretization in the velocity variable, discontinuous Galerkin discretizations in the spatial variable, and 
Runge-Kutta/Adam-Bashforth integration in time. The code includes several models for evaluating the Boltzmann collision 
operator: the full Boltzmann collision operator for binary collisions (hard--spheres are currently 
supported), linearized collision operator, BGk, ES-BGK, and model collision operator with enforced relaxation rates for moments. 

The code is MPI parallel. 

Methods for discretization of the Boltzmann collision operator that are used in this code were reported in following papers: 

2019 A. Alekseenko, J.  Limbacher, Evaluating high order discontinuous Galerkin discretization of the Boltzmann
collision integral in $O(N^2)$ operations using the discrete Fourier transform.\ \textit{Kinetic and Related Models} Vol.~12, 
n.~4,703-- 726, DOI: 10.3934/krm.2019027 

2018 A. Alekseenko, T. Nguyen, and A. Wood, A deterministic-stochastic method for computing the
Boltzmann collision Integral in $O(MN)$ operations. \textit{Kinetic and Related Models}, Vol.\, 11, no. 1937-5093

2015 A. Alekseenko and C. Euler, A Bhatnagar-Gross-Krook kinetic model with velocity-dependent collision frequency and 
corrected relaxation of moments.\textit{Continuum Mechanics and Thermodynamics} DOI: 10.1007/s00161-014-0407-0

2014 A. Alekseenko and E. Josyula, Deterministic solution of the spatially homogeneous
Boltzmann equation using discontinuous Galerkin discretizations in the velocity space, 
\textit{Journal of Computational Physics}, Vol.~272, n.~1, (2014) 170--188.

2012 A. Alekseenko and E. Josyula, Deterministic solution of the Boltzmann equation using a discontinuous
Galerkin velocity discretization.\ \textit{Proceedings of the $28^{\mathrm{th}}$ International Symposium 
on Rarefied Gas Dynamics, Spain 2012}, AIP Conference Proceedings, 2012, 8 pp.

2012, A. Alekseenko, S. Gimelshein and N. Gimelshein, An application of discontinuous Galerkin space and velocity discretization to model kinetic equations. \textit{International Journal of Computational Fluid Dynamics}, Vol. 26, No. 3, 145--161.

2011, A.M. Alekseenko, Numerical properties of high order discrete velocity solutions to the BGK kinetic equation. \textit{Applied Numerical Mathematics}, Vol. 61 (2011), pp. 410--427, http://dx.doi.org/10.1016/j.apnum.2010.11.005\.


