# regional_liquefaction
[![DOI](https://zenodo.org/badge/700012083.svg)](https://zenodo.org/badge/latestdoi/700012083)

This project contains python functions to run cpt-based liquefaction calculations on a regional scale. Recreates figures and calculations from the following paper:

Mongold, E. and Baker, J.W. (2024) "Probabilistic Regional Liquefaction Hazard and Risk Analysis: A Case Study of Residential Buildings in Alameda, CA" Natural Hazards Review, 25(4), 04024039, https://doi.org/10.1061/NHREFO.NHENG-2078.

This package is broken down to multiple steps. 'liquefaction' can be imported as a package with a local download of the folder, and running setup.py. The following python files are within **liquefaction**, defining various functions:
1. preprocess.py
2. moss_calcs.py
3. boulangeridriss_calcs.py
4. simulations.py
5. postprocess.py

It is able to run liquefaction calculations on a regional-scale grid, using either Boulanger & Idriss (2014) or Moss et al. (2006) model.

The dependencies are all included in base.py, where module imports are performed.  

This function has been applied with the following inputs:

1. CPT data from the USGS (including water depth) [https://www.usgs.gov/tools/cone-penetration-testing-cpt-data]
2. Simulated soil data using SGeMS [https://sourceforge.net/projects/sgems/]
3. Ground motions using R2D [https://simcenter.designsafe-ci.org/research-tools/r2dtool/]
4. Ground motions using pypsha [https://pypi.org/project/pypsha/]

The directory **example** contains jupyter notebooks that run, post-process, and create figures based on an example run of the data.

paper_figures.ipynb can be run on its own using **full outputs** to re-create figures

To set up a new simulation, the files should be set up and run in the following order:
1. make_inputs.py
2. liq_setup.py
3. liq_run.py
4. run_loss.py


