# Modeling Functional Brain Connectivity: from DTI to EEG

This repository contains Matlab files used in the paper "Modeling of Large-Scale Functional Brain Networks Based on Structural Connectivity from DTI: Comparison with EEG Derived Phase Coupling Networks and Evaluation of Alternative Methods along the Modeling Path" (doi: 10.1371/journal.pcbi.1005025).

* The order and labels of all ROI's are stored in the file [labels_sources.mat](labels_sources.mat).
* The order and labels of all electrodes in the file [labels_electrodes.mat](labels_electrodes.mat).
* The matrix plots in the paper were produced by reordering the source ROI's in a modular structure according to the sorting indices in file [sources_plot_order.mat](sources_plot_order.mat).

## Structural Connectivity Data

* The structural connectivity data obtained from DTI fiber tracking is located in the file [dti/SC.mat](dti/SC.mat).
* The average fiber lengths are stored in the file [dti/dist.mat](dti/dist.mat).

## Functional Connectivity Data

The functional connectivity data is split into corresponding subfolder depending on the source reconstruction method (eloreta, lcmv, mne) or in electrode space.
Each file corresponds to a specific connectivity metric (COH, ICOH, LPC, PLI, PLV, WPLI) as refered to in the paper (doi: 10.1371/journal.pcbi.1005025).
The dimensions of the corresponding variables are as follows:

1. Dimension: Subject number
2. Dimension: Recording session / day
3. Dimension: Pre-task and post-task resting-state conditions
4. Dimension: ROI index (i.e. source connectivity)
5. Dimension: ROI index (i.e. target connectivity)
6. Dimension: Frequency in Hz

## Simulated Functional Connectivity

The simulated functional connectivity data is split into the corresponding subfolders depending on what kind of comparison was performed.
For example, the simulated FC of the reference model can be found in the file [sim_preprocessings/A_Reference.mat](sim_preprocessings/A_Reference.mat).

* The folder *sim_preprocessings* contains all simulated FC matrices using different SC preprocessing steps (all produced using the SAR model).
* The folder *sim_models* contains the simulated FC based on the SAR model and the Kuramoto model.
* The folder *sim_forward_projection* contains simulated FC in electrode space.
