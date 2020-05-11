# ISMRM Spectroscopy Study Group: MRS Fitting Challenge
https://www.ismrm.org/workshops/Spectroscopy16/mrs_fitting_challenge/  
  
This data and the fitting challenge was prepared by Malgorzata Marjanska, Dinesh Deelchand, and Roland Kreis.
Malgorzata Marjanska: gosia@cmrr.umn.edu  
Roland Kreis: roland.kreis@insel.ch  
  
## Description of the data

28 datasets are provided in three formats:

- text file (column 1: real part of water suppressed FID; column 2: imaginary part of water suppressed FID; column 3: real part of water FID; column 4: imaginary part of water FID)  
- LCModel (.RAW and .h2o)  
- jMRUI (ASCII txt formats for both water suppressed [WS] and water spectra)  
  
  
Also, the metabolite basis set with macromolecular baseline is provided in these four formats:
- text file (column 1: real part of FID; column 2: imaginary part of FID) for each metabolite and macromolecular baseline (MMBL)
- text file with no reference peak at 0 ppm (column 1: real part of FID; column 2: imaginary part of FID) for each metabolite and MMBL
- LCModel (.RAW) for each metabolite and MMBL and .BASIS
- jMRUI (ASCII txt file format) for each metabolite and MMBL  

An additional dataset, Cr_10mM_test_water_scaling (text, LCModel, jMRUI), is provided for testing water scaling. This dataset contains a Cr spectrum which - with correct water scaling - should come out to be 10 mM.

#### Water scaling information
metabolite concentration = (relaxation corrected water concentration) * (metabolite relaxation correction) * metabolite area / water area

relaxation corrected water concentration = 1 mol / 18.015 g * 0.6 * 0.78 g/ml * exp(-30 ms/110 ms) + 1 mol/18.015 g * 0.4 *0.65 g/ml * exp(-30 ms/80 ms) = 29697 mM

metabolite relaxation correction = 1/(exp(-30 ms/160 ms)) = 1.206

#### Description of the simulated data
Frequency = 123.2 MHz  
Sequence: PRESS  
TE = 30 ms, TE1 = 11 ms, TE2 = 19 ms  
TR >> T1’s  
Spectral width = 4000 Hz  
Number of points = 2048  
Tissue content: GM = 60%, WM = 40%  
Water content: GM = 0.78 g/ml, WM = 0.65 g/ml  
T2 of water: GM = 110 ms, WM = 80 ms  
T2 of metabolites = 160 ms  
  
The datasets were generated using ideal pulses except for MMBL which was obtained experimentally. Glucose was simulated using both anomers, 0.36 alpha-glucose and 0.64 beta-glucose. The datasets may contain some or all of the metabolites listed among the basis spectra. In addition, lipid resonances and artifacts may be present.

## Original MRS Fitting Challenge description

Fitting of the MRS data plays an important role in the quantification of metabolite concentrations. A number of commercial and home-built packages are available and used by the MRS community to fit spectra.

Our aim is to engage the MRS community in fitting of sample datasets that will help in comparing fitting packages and will allow identification of problems and improvements that could be made to make fitting more accurate and reproducible.

Therefore, we generated synthetic data. After the initial review of the data from the first phase of fitting challenge, we are reopening the fitting challenge for a second phase to have a better representation of fitting programs.
