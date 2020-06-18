# MOSAIC-Optical-Test
This project aims to compare the optical calculation results between MOSAIC and an online python library PyMieScatt. 
The particle size range of the cases in this test ranges from 10 to 100 nm. The initial RH should be set to very low values, 
thus we do not need to involve the condensation equilibrium issues in MOSAIC. Here we use RH at 10%. 

#Case 1: Monodisperse homogeneous particles using offline MOSAIC

This case is to test whether the offline postprocessing codes work. The initial composition for the particles only contain ammonium
sulfate. Steps to run the cases:

-- Step 1: Run 1_create_lib.py to create 91 cases with diameter range from 10 to 100 nm.

-- Step 2: Run 2_optical_submit.sh to create initial particles from PartMC for calculation.

-- Step 3: Run 2_optical_submit.sh again to process this particles. Before submit the job, change the joblist1 in the script to joblist2.
