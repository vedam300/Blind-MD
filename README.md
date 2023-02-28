# Blind-MD
MD simulation of two proteins that were placed beside each other, blindly, by editing the pdb files, to understand the interacting domains

The contents of the PDB files - a human protein and a predicted viral protein - were pasted into a single merged file. 
Any steric clashes were avoided by moving the peptides away from each other using pymol
System Preparation: The HOH and other heteroatom entries were removed from the coordinate file
The system was then solvated using TIP3P water molecules and counter ions were added to balance charge.
Periodic boundary conditions were used in the simulations with a triclinic box
Energy minimization (steepest descent algorithm) was run for 5,000 steps to remove unfavorable steric contacts, followed by a 1-ns equilibration phase
All simulations were performed in the NPT ensemble at constant number of particles N, pressure, and temperature
The production runs of equilibrium MD were performed for 1 ns.
The production run was performed by submitting jobs using SLURM language in the high performance cluster (HPC) of Indian Institute of Technology, Guwahati – ParamIshan.
Data were analyzed using GROMACS and locally written code. Molecular graphic images were prepared using visual molecular dynamics (VMD).
All simulations were carried out with the extended united atom CHARMM27 allatom force field (CHARM22 plus CMAP for proteins) forcefield.
