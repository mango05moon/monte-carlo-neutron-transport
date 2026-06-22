# Monte Carlo Neutron Transport Simulation

A Python simulation of thermal neutron absorption and scattering through shielding materials (water, lead, graphite), implemented using Monte Carlo techniques as part of PHYS20762 Computational Physics at the University of Manchester (2025–2026).

---

## Methods

- **Inverse-transform sampling** of the exponential distribution for physically correct free-path lengths
- **Isotropic scattering** on the unit sphere via spherical polar coordinates
- **Weighted log-linear regression** to extract characteristic attenuation lengths with propagated uncertainties
- **Binomial uncertainty quantification** for transmission, reflection, and absorption rates
- **Woodcock fictitious-tracking method** for neutron transport across heterogeneous two-material interfaces
- **Convergence analysis** confirming expected 1/√N uncertainty scaling
- **Shielding optimisation study** comparing all two-material combinations over fixed total thickness

A custom `UniformBuffer` class pre-generates random numbers in batches, achieving approximately **2× speedup** in the inner simulation loop. Total notebook runtime: **under 45 seconds**.

---

## Key concepts

Monte Carlo particle transport, inverse-transform sampling, stochastic random walks, uncertainty quantification, weighted regression, RNG validation (spectral test / Marsaglia's theorem), performance optimisation
