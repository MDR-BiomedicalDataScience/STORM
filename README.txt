1. General information
2. How to use
3. New in version 2.0

Copyright J.M. Posma 2011-2019

#####################################################################################################################

1. General information

Title: SubseT Optimization by Reference Matching (STORM)

Summary: A multivariate statistical approach to recover metabolite structure information from multiple (1)H NMR
		spectra in population sample sets. Subset optimization by reference matching (STORM) was developed to
		select subsets of (1)H NMR spectra that contain specific spectroscopic 	signatures of biomarkers
		differentiating between different human populations. STORM aims to improve the visualization of
		structural correlations in spectroscopic data by using these reduced spectral subsets containing
		smaller numbers of samples than the number of variables (n << p). Multiple testing is included by
		default (choice of Bonferroni connection, Benjamini-Hochberg False Discovery Rate and Storey-
		Tibshirani False Discovery Rate) to control the number of false positive associations. STORM improves
		the visualization of more abundant NMR peaks compared to Statistical TOtal Correlation SpectroscopY
		(STOCSY).

Author: J. M. Posma
Institution: Imperial College London
Department: Computational and Systems Medicine, Department of Surgery and Cancer
Email: jmp111@ic.ac.uk
Version: 2.0
Citation: Posma JM, et al. (2012) Analytical Chemistry 84(24):10694-701

Platform dependence: none found
Software dependence: none found (2012a and up works)
Toolbox dependence: none (code now works without the Statistics and Parallel Processing Toolboxes)

#####################################################################################################################

2. How to use

To see how the script should be used in MATLAB simply type JMP_STORM and press enter this displays the help file in
		the command line (to view all options for the variable input arguments):
>> JMP_STORM

To perform STOCSY using the STORM methodology (where ppmref is replaced by the ppm value of the driver):
>> JMP_STORM(ppm,X,ppmref)
 
#####################################################################################################################

3. New in version 2.0

It is slightly different from the original published STORM code in that it:
    1) reduces to STOCSY if: only one index is used or the subset is too small,
    2) now multiple areas of interest can be added to the reference, however the driver will still be the peak with
		the highest intensity unless you specify the driver, and
    3) the plot is different so it can be used on any computer and it has an extra subplot at the top so highly
		correlated peaks can be easily spotted without having to zoom in and scroll.
    4) updated to work in 2018b as it does in previous versions