# Cloud-Edge Motion by a Ducted Gravity Wave

This repo contains a complete build of CM1 release 19.6 that includes
the initialization code for the cloud-ducted gravity wave. No changes 
have been made to the CM1 model core. The base-state initialization 
for the marginal cloud and cloud layer are found in base.F under 
`isnd = 1000` and `isnd = 1104`. The cloud-ducted gravity wave 
perturbations are initialized in init3d.F under `iinit = 1016`.

To run the model first compile the code using the makefile in `src/`. 
Be sure to modify the makefile to suit your system. CM1 instructions
are included within. This creates the executable `cm1.exe` in the 
`run/` directory. Cloud-ducted gravity wave input files are found 
in `run/config_files`. Once compiled, run the model by copying an
input file to the `run/` directory, rename to `namelist.input`, and
execute using `./cm1.exe`. Model output is stored in `run/RunOutputs`.
This directory must exist before running the CM1 model. A special
section for the cloud ducted wave parameters has been added to the
input files titled `MBMparam`.

The author of CM1 is George Bryan of the National Centre for Atmospheric
Research in Boulder, CO. Full credit goes to him for the model development.

## References:
CM1:

Bryan, G. H., and J. M. Fritsch, 2002: A Benchmark Simulation for Moist Nonhydrostatic Numerical Models. Mon. Wea. Rev., 130, 2917–2928, https://doi.org/10.1175/1520-0493(2002)130<2917:ABSFMN>2.0.CO;2.

Cloud Ducted Gravity Wave:

Muraki, D. J., and Walsh R. P., 2024: Cloud-Edge Motion by a Ducted Gravity Wave. Journal of the Atmospheric Sciences