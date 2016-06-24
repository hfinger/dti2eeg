# Modeling Functional Brain Connectivity: from DTI to EEG

The order and labels of all ROI's are stored in labels_sources.mat
The order and labels of all electrodes in labels_electrodes.mat

## Structural Connectivity Data

The structural connectivity data obtained from DTI fiber tracking is located in the file [dti/SC.mat](dti/SC.mat).
The average fiber lengths are stored in file [dti/dist.mat](dti/dist.mat)

## Functional Connectivity Data

The functional connectivity data is split into corresponding subfolder depending on the source reconstruction method (eloreta, lcmv, mne) or in electrode space.
Each file corresponds to a specific connectivity metric (COH, ICOH, LPC, PLI, PLV, WPLI).
The dimensions of the corresponding variable are as follows:

1. Dimension: subject number
2. Dimension: Session
3. Dimension: Pre and post resting-state conditions
4. Dimension: ROI index
5. Dimension: ROI index
6. Dimension: Frequency in Hz