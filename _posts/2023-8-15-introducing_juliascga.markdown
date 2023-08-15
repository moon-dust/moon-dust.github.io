---
layout: post
title:  "Introducing JuliaSCGA"
date:   2023-8-14 9:30:00 +0800
categories: simulations
---
Recent progresses in neutron scattering instrumentation, especially the advancement of high-resolution two-dimensional detectors, greatly enhance the power of diffuse neutron scattering. For many frustrated magnets, the quasielastic diffuse neutron scattering pattern contains rich information on the correlated states. Vaguely speaking, diffuse neutron scattering fills the gap between the conventional neutron diffraction and inelastic neutron scattering techniques. 

Here we introduce [JuliaSCGA](https://github.com/moon-dust/JuliaSCGA.jl), a [Julia](https://julialang.org) implementation of the efficient [self-consistent Gaussian approximation (SCGA) method](https://link.aps.org/doi/10.1103/PhysRevB.53.11593) to simulate the diffuse neutron scattering pattern for classical spin models. When combined with optimization packages like [Optim.jl](https://github.com/JuliaNLSolvers/Optim.jl/), JuliaSCGA can be used to determine the spin Hamiltonian that was previously achieved only through inelastic neutron scattering. Recent applications of the SCGA method include the pyrochlore-lattice compounds [MgCr<sub>2</sub>O<sub>4</sub>](https://link.aps.org/doi/10.1103/PhysRevLett.122.097201) and [ZnCr<sub>2</sub>Se<sub>4</sub>](https://link.aps.org/doi/10.1103/PhysRevLett.129.237202), and the honeycomb-lattice compound [FeCl<sub>3</sub>](https://link.aps.org/doi/10.1103/PhysRevLett.128.227201).

For single crystal calculations, the use of Julia is straightforward as explained in the [how-to page](https://github.com/moon-dust/JuliaSCGA.jl). For powder calculations, a random array of wavevectors with different lengths can be firstly generated, then the calculated intensity at wavevectors of the same length is averaged for the final plot. Using the [example diamond lattice code](https://github.com/moon-dust/JuliaSCGA.jl/blob/main/examples/diamond_powder.jl), a powder diffuse pattern as the following can be generated:

![](/assets/images/diamond_powder.png)

JuliaSCGA can also be utilized as the basis for more advanced calculations. One example is the [nematic bond theory](https://link.aps.org/doi/10.1103/PhysRevB.99.174404) that incorporate higher order perturbations compared to the SCGA approximation. Following the [original derivation](https://link.aps.org/doi/10.1103/PhysRevLett.119.157202) and a [more recent application](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.106.L220410), we present an [example nematic bond theory code](https://github.com/moon-dust/JuliaSCGA.jl/blob/main/examples/square_nematic.jl) for the the square lattice model. The temperature evolution of spin correlations, including the development of a nematic phase near the phase transition, is presented in the following example plot:

![](/assets/images/nematic_bond_theory.png)
