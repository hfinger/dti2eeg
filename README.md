# Modeling Functional Brain Connectivity: from DTI to EEG

* The order and labels of all ROI's are stored in the file [labels_sources.mat](labels_sources.mat)
* The order and labels of all electrodes in the file [labels_electrodes.mat](labels_electrodes.mat)

## Structural Connectivity Data

* The structural connectivity data obtained from DTI fiber tracking is located in the file [dti/SC.mat](dti/SC.mat).
* The average fiber lengths are stored in the file [dti/dist.mat](dti/dist.mat)

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