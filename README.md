# MOSAIC-Optical-Test
This project aims to compare the optical calculation results between MOSAIC and an online python library PyMieScatt. 
The particle size range of the cases in this test ranges from 10 to 100 nm. The initial RH should be set to very low values, 
thus we do not need to involve the condensation equilibrium issues in MOSAIC. Here we use RH at 10%. 

#Case 1: Monodisperse homogeneous particles using offline MOSAIC

This case is to compare the difference between the offline MOSAIC postprocessing codes and PyMieScatt. The initial composition for the particles only contain ammonium sulfate, with ratio SO4:NH4=1:0.375. Steps to run the cases:

-- Step 1: Run 1_create_lib.py to create 91 cases with diameter range from 10 to 100 nm.

-- Step 2: Run 2_optical_submit.sh to create initial particles from PartMC with MOSAIC off.

-- Step 3: Run 2_optical_submit.sh again to process this particles. Before submit the job, change the joblist1 in the script to joblist2.

#Case 2: Monodisperse homogeneous particles using online MOSAIC

This case is to compare the difference between the online MOSAIC codes and PyMieScatt. The initial composition for the particles only contain ammonium sulfate, with ratio SO4:NH4=1:0.375. Steps to run the cases:

-- Step 1: Run 1_create_lib.py to create 91 cases with diameter range from 10 to 100 nm.

-- Step 2: Run 2_optical_submit.sh to create initial particles from PartMC with MOSAIC on.

#Case 3 and Case 4 are the heterogenous cases with core of BC and shell of ammonium sulfate, the initial mass ratio of BC, SO4 and NH4 is 0.02:1:0.375. This is the only difference with Case 1 and Case 2. 
