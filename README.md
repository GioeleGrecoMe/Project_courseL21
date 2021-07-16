# Project_courseL21
This folder contains the following files:
- main_3D_cone.mph - COMSOL 3D cone model simulations with LNS and H physics
- Main_mouthpiece.mph - COMSOL 3D mouthpiece model simulations with LNS and H physics
- mouthpieceReferenceComsol.pdf - Mechanical design of parametrized mouthpiece shape with the comsol notation
- Cone Data folder - folder that contains simulation data in txt form of Cone simulations results as .txt files
- MouthpieceDATA folder - folder that contains simulation data in txt form of mouthpiece simulations results as .txt files

## COMSOL - Main_mouthpiece.mph
![alt text](https://github.com/GioeleGrecoMe/Project_courseL21/blob/main/Screenshot%20(518).png?raw=true)


Let's describe the tool tree on the left. It contains:
### Global Definitions
In "Alto S90-170" there are all the preset for the A, A1, A2, B, B1, B2, C, C1, C2 mouthpiece models.
In Geometry Parts there are the 3D models that can be exported and printed, "Mouthpiecepieno" is the 3D shape of mouthpiece without cavity, "reed" is the reed model, "interno" is the internal air cavity geometry and "Mouthpiece-to-print" is the finisched model of the mouthpiece ready to print.
### Component 4
Component 4 contains all the data regard the simulation behaviour. It has the "Geometry 4" that are the operation that are computed in order to create the final internal air flux geometry. The "Materials" that is standard air in which was included the Z air impedance.
#### Definitions
It contains lot of probes that can be used to measure input and output impedance, pressure and velocity.
#### Acoustic pressure, frequency domain 3
It contains the Helmholtz model physics.
Typical wave speed for PML is set to c_{ref}=346.12[m/s] that is the sound speed at temperature T=298.15[K], absolute pressure p_A=1[atm] and the Pressure acoustic model has Ideal gas as fluid model. Imposed pressure is a sine type with absolute value of 1000[Pa].
#### Linearized Navier-Stokes, frequency domain
It contains the linearized Navier-Stokes model physics.
It is in adiabatic formulation and other data are the same as in Acoustic pressure.
#### Mesh
Mesh can be adapted to each situation, for the Acoustic pressure simulation is calibrate for fluid dynamics coarser. It is tethraedric no-structured and it has 4 boundary layers.
### Helmholtz Study
It contains sweep between A, B and C2 type and the study step. The simulation starts from 100 Hz to 1200 Hz with 5 Hz steps and compute the helmholtz equation in the geometry domain. 
### NSL study
It contains sweep between A, B and C2 type and the study step. The simulation starts from 100 Hz to 1200 Hz with 5 Hz steps and compute the Linearized Navier-Stokes equation in the geometry domain.
### Results
In this section there are the 3D and 2D plot. 
For the Helmholtz equation the 3D plot are isoline pressure and pressure level (in dB), for the LNS the 3D plots are pressure and velocity.
2D plots are related to the pressure and impedance in certain points like the center of the output section, or on the probes like the inlet impedance or output pressure. 


REPOSITORY LINK https://github.com/GioeleGrecoMe/Project_courseL21
