PIC-component-simulations.
Dominic Ditmyer.
Last Updated 1/5/2026.

# Photonic Integrated Ciruit Simulations
This project involves the compiling of physics equation solvers (usually in the form of boundary value PDEs or Integro-Differential equations) that are related to the engineering or photonic integrated circuits (PICs). 

## PIC Component Simulation
One part of the project is to use the GDS Factory software toolkit to practice making design choices in concerteration of common problems in the feild of photonic integrated circuits.
* materials
* circuit geometry
* component design
* multi componenet integration

Simulations on GDSFactory files are most conviniently done with Tidy3D open-source software. Motivating problems include:
* calculating component (waveguide) cross-talk
* calculating propogation loss
* calculating component efficiency (couplers, interferometers)

#### Problem: Calculate what a Mach-Zehnder Interferometer does and how well it does it. 
> * Step 1: create a MZI geometry in gds factory
> * Step 2: Upload to Tidy3d as a gds file.
> * Step 3: 


## LOQC Component Modeling Goals

This part of the project focuses on simulating and analyzing photonic components for **linear optical quantum computing (LOQC)** applications. The primary goal is to create a flexible framework for designing, testing, and characterizing integrated photonic components that can be used to implement single- and two-photon quantum operations, such as Bell state generation.

Key objectives include:

1. **Replicate canonical photonic components**
   - Design and simulate simple integrated photonic components like Mach-Zehnder Interferometers (MZIs) and microring modulators.
   - Generate GDS layouts using [GDSFactory](https://gdsfactory.github.io/) and export them for simulation.

2. **Perform end-to-end optical simulations**
   - Use tools such as [Tidy3D](https://www.tidy3d.com/) to compute electromagnetic fields, spectral responses, and scattering parameters (S-parameters) of components.
   - Evaluate performance metrics relevant to quantum operations, including insertion loss, phase shifts, and crosstalk between waveguides.

3. **Develop a component test framework**
   - Build scripts and routines to systematically characterize multiple devices.
   - Automate measurements of insertion loss, extinction ratios, and crosstalk for different layouts and configurations.
   - Record results in a reproducible, version-controlled manner.

4. **Support LOQC architecture design**
   - Use simulation data to inform higher-level LOQC circuit design decisions.
   - Identify component performance limitations that could affect quantum interference, entanglement generation, and fidelity of two-photon operations.

The ultimate aim is to provide a **robust, documented, and modular workflow** that can serve as a foundation for future experiments in LOQC device design, simulation, and testing.

