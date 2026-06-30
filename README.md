# Berry Curvature & Quantum Geometry in Topological Lattice Models

This repository contains numerical simulations exploring Berry curvature, the quantum geometric tensor, and Zeeman-type intrinsic response coefficients (IGMC) in topological lattice models, including Weyl semimetals, Rashba spin-orbit coupled systems, and gapped Dirac models.

## Overview

The notebooks in this repository build two-band tight-binding and continuum Hamiltonians for various lattice models, then compute interband geometric quantities like the symmetric quantum metric (Q) and antisymmetric Berry curvature (Z) components of the quantum geometric tensor. These quantities are validated against analytical expressions where available, mapped across the Brillouin zone, and integrated over momentum space with Fermi-Dirac weighting to obtain intrinsic gyrotropic magnetic-like conductivity (IGMC) coefficients as a function of chemical potential.

## Contents

- **`zeeman_berry_curvature_kxky_map.ipynb`** — Zeeman Berry curvature tensor (Z_αβ) calculation for a tilted Weyl lattice model, with interactive component selection and 2D kx-ky mapping at fixed kz.

- **`weyl_quantum_metric_Qxy_validation.ipynb`** — Numeric vs. analytical validation of the quantum metric component Q_xy^(-+) for an isotropic Weyl Hamiltonian, with a 2D momentum-space map.

- **`weyl_zeeman_curvature_Zxy_validation.ipynb`** — Companion notebook isolating the antisymmetric Berry curvature component Z_xy^(-+) for the isotropic Weyl model, validated against its closed-form expression.

- **`igmc_sigma_zz_mu_sweep_no_tilt.ipynb`** — Full 3D Brillouin zone integration of the Zeeman Berry curvature to compute the IGMC response σ^C_zz as a function of chemical potential for a tilt-free lattice model.

- **`rashba_igmc_sigma_xy_mu_sweep.ipynb`** — IGMC σ^C_xy calculation for a 2D Rashba spin-orbit coupled electron gas in full SI units, capturing the chemical potential dependence of the response in physical units (A·m⁻¹·T⁻¹).

- **`dirac_lattice_sigma_zz_conductivity_mu_sweep.ipynb`** — 3D tilted Dirac-like lattice model with explicit finite-difference Hamiltonian derivatives, computing symmetric conductivity-like response σ^C_zz via momentum-space integration.

- **`gapped_dirac_2d_Zxx_sigma_xx_mu_sweep.ipynb`** — 2D gapped Dirac model with a second-order pole formulation of Z_xx, decomposing the conductivity response σ_xx^D into symmetric and antisymmetric parts as a function of chemical potential.

## Physical Background

The underlying framework treats Bloch Hamiltonians as effective two-level systems parametrized by a vector N(k) (and, where applicable, a tilt term N0(k)), with interband Berry connections obtained via the Hellmann–Feynman theorem. Combining these connections with spin matrix elements yields the quantum geometric tensor, whose real (symmetric, metric-like) and imaginary (antisymmetric, curvature-like) parts govern distinct physical responses including the intrinsic gyrotropic magnetoelectric-type conductivities studied here. These calculations connect to ongoing work on prethermalization and nonequilibrium dynamics in related lattice systems.

## Requirements

- Python 3.x
- NumPy
- Matplotlib

## Usage

Each notebook is self-contained and can be run independently. Most expose tunable model parameters (hopping amplitudes, mass terms, tilt strength, spin-orbit coupling) near the top of the file for quick exploration of different physical regimes.
