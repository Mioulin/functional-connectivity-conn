# functional-connectivity-conn

INPUTS:

Individual raw resting-state fMRI files (20 DMT/20PCB)
Individual structural MRI files, also as nifti files

OUTPUTS:

Denoised resting-state fMRI files - to be found in output/results/preprocessing/niftiDATA_Sub*.nii
ROI-to-ROI connectivity matrix (resultsROI_Subject###_Condition###.mat) and seed-to-voxel functional connectiviy (BETA.*nii) estimates in output/results/firstlevel/ANALYSIS-01. The file _list_sources.mat gives the identity of the 168 sources used to perfrom the analysis (164 ROIs + conditions)
Time series of confounds and ROIs in output/DATA/ROI_Subject###_Condition###.mat
Output.mat and preprocess.m can be used to retrieve information on the performed preprocessing steps and used script

PARAMETERS: Several parameters for preprocessing pipeline:

TR (in seconds, e.g. 2)
slice acquisition order (e.g. 'ascending','descending','interleaved (middle-top)','interleaved (bottom-up)','interleaved (top-down)', 'interleaved (Siemens)','BIDS')
smoothing kernel (fwhm, defualt is 8mm)
Choose template normalization (default is MNI)
Spatial filter range in Hz (default is 0.01 for min and 0.1 for max)
Whether to perform gobal signal regression or not??
