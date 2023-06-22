# Monkeys Exhibit Human-like Gaze Biases in Economic Decisions

This repository contains data, MATLAB, and python codes needed to reproduce the analyses reported in:

#### Monkeys Exhibit Human-like Gaze Biases in Economic Decisions

Lupkin, S.M. & McGinty, V.B.

bioRxiv, 2022; doi: https://doi.org/10.1101/2022.02.24.481847



### Contents of this repository

- ***Matlab***: Folder containing the data and analysis scripts performed in Matlab. For each analysis script (.mlx file), there is a corresponding data file (.mat file) with the same name. The scripts described below were created with Matlab version R2020a. 
  
  - *BasicPsychometrics*: This file reproduces the analyses reported in the *Basic Psychometrics* sections of the Results, including the graphs that are shown in Figure 1D-F, as well as Figure 2. 
  
  - *GazeBehavior*: This file reproduces the analyses reported in the *Gaze Behavior and Basic Fixation Properties* section of the Results. 
  - *GazeBiases*: This file reproduces all of the analyses described in the *Gaze-Related Choice Biases* section of the Results, including graphs in Figures 5C-F, 6B-E, & 7B/C
  
  - *GammaSpeciesComparison*: This file generates the graph in Figure 8. The model parameters for each of the four human datasets were obtained from the GitHub repository associated with [this paper](https://www.nature.com/articles/s41562-019-0584-8) paper. The repository can be accessed [here](https://github.com/glamlab/gaze-bias-differences).  
  
  - *GLAM_OOS_ModelFit*: This file reproduces the goodness-of-fit analyses reported in the *Gaze-Weighted Linear Accumulator Model (GLAM)* section of the Results, Supplementary File 4, and depicted in Figure 9. The data contained in the relevant .mat file were output from the Jupyter Notebooks contained in the ***Python*** folder of this repository. 

- ***Python***: Folder containing the jupyter notebooks and requisite .csv files needed to run the Gaze-Weighted Linear Accumulator Model (GLAM). The model toolbox is available on the [glambox repository](https://github.com/glamlab/glambox). The associated documentation can be found [here](https://glambox.readthedocs.io/en/latest/). The results of the analyses contained in these files are all reported in the *Gaze-Weighted Linear Accumulator Model (GLAM)* section of the Results. Note that the notebooks in this folder have been tested on both a macOS (BigSur) as well as the Windows Subsytem for Linux (WSL) using a Ubuntu 20.4 operating system.
  - *GLAM_relative_fit.ipynb*: Jupyter notebbok containing the code necessary to run the the gaze-bias (gamma as a free parameter) and no gaze-bias (gamma set to 1) variants of the GLAM and to then compare the relative fit of the two variants to each other. The model parameters for both variants are presented in Supplementary File 2. 
  - *GLAM_absolute_fit.ipynb*: Jupyter notebbok containing the code necessary to run out-of-sample simulations in order to assess the GLAM's ability to predict the observed behavioral data.  
  - *GLAMdata_monkey.csv*: *.csv file used to run the model using the DATA_GROUPING flag set to "monkey". In this case, one model is fit for each monkey. 
  - *GLAMdata_session.csv*: *.csv file used to run the model using the DATA_GROUPING flag set to "session". In this case, one model is fit for each session.


 
