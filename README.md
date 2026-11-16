# Kerr_BH_Accretion
General relativistic ray-tracing and numerical simulation engine in Kerr spacetime to model Doppler-shifted accretion signatures, particle plunge trajectories, and black hole shadows across various spin parameters.

This repository contains the core computational engine and analysis notebooks developed for my Master's Thesis project at IISER Kolkata (NumAstro Lab, supervised by Dr. Sudip Kumar Garain). The project implements general relativistic numerical integration and backward ray-tracing to investigate how accreting matter (specifically radially plunging particle ensembles and continuous flows) appears to a distant observer across varying black hole spin parameters ($a$).

## Key Features & Methodology
Symbolic & Numerical Christoffel Generation: Automatically derives the analytical connection coefficients (Christoffel symbols) for the Kerr metric in Boyer-Lindquist coordinates using SymPy and compiles them into high-performance numerical routines via NumPy.
Robust Geodesic Integration Engine: Utilizes adaptive Runge-Kutta integration (scipy.integrate.solveivp with RK45) to track both massive particle timelike geodesics and null geodesics (photon paths), incorporating strict event horizon boundary checks and polar coordinate singularity handling.
Backward Ray-Tracing Pipeline: Shoots rays backward from a virtual observer screen across an impact parameter grid ($\alpha, \beta$), tracing them through curved spacetime to map the black hole shadow and intercept equatorial accretion structures.
Relativistic Radiative Transfer & Doppler Shifting: Implements exact invariant energy calculations ($E{em} = -p_\mu u^\mu$) coupling particle 4-velocities with photon 4-momenta at the equatorial plane intersection, scaling pixel flux by $I \propto g^4$ to capture kinematic Doppler beaming and gravitational redshift.
