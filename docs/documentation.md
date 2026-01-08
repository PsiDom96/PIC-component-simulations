Photonic Integrated Circuits in GDS Factory and Tidy3D
Dominic Ditmyer

## Contents

1.  Motivation

2.  Methods

    a.  Python environment

    b.  Layout design

    c.  Simulation

3.  Mach-Zehnder Interferometer

4.  Ring Modulator


**Abstract**:

Here, I present the design and simulation of photonic integrated circuit
components using free and open-source tools. Included are steps and
design choices that lead to the resulting analysis.

# 1. Motivation

# 2. Methods

## Python Environment

For this project, I will be using Python programming and other widely
available open-source software packages for computer-aided engineering.
The preliminary step is the creation of a virtual environment in order
to isolate project-specific Python dependencies for the workflow.

My preference is venv, which is a python module that supports creating
lightweight "virtual environments" with their own Python installation
\[1\]. To create an environment, I first create a directory for the
project and then create the venv inside the directory.

With the venv activated, I now install the necessary Python packages for
GDSFactory and Tidy3D using pip. This should install all the required
dependencies automatically.

Command Prompt:

> (venv) C:\\directory\\venv\> pip install gdsfactory tidy3d

I also like to use Jupyter Notebooks for testing scripts and
exploration.

## PIC Layout Design

For the layout of the photonic components, I am using GDSFactory, a program that allows users to input Python code to output CAD files (GDS, OASIS, etc.) \[2\].



# References:

\[1\] [venv --- Creation of virtual environments --- Python 3.13.3
documentation](https://docs.python.org/3/library/venv.html)

\[2\] [GDSFactory 9.5.1 ---
GDSFactory](https://gdsfactory.github.io/gdsfactory/)
