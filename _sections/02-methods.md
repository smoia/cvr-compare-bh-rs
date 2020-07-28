---
layout: post
title: Methods
description: We asked 6 subects to undergo 10 multi-echo BOLD fMRI sessions, one week apart, and perform a RS or a BH task. We computed CVR and RSFA maps for each session and normalised those maps to the MNI space. We computed the correlation between and the reliability of such maps both at the voxel and at a parcel level. 
image: methods.png
---

Six healthy volunteers underwent 10 MRI sessions in a 3T Siemens PrismaFit scanner, spaced 1-week apart at the same time of day. A RS and a BH task (Fig. 1) adapted from [5] were administered at each session while collecting ME-fMRI data (400 and 340 scans respectively, TR=1.5 s, TEs=10.6/28.69/46.78/64.87/82.96 ms, flip angle=70°, MB=4, GRAPPA=2, 52 slices, Partial-Fourier=6/8, FoV=211x211 mm2, voxel size=2.4x2.4x3 mm3). CO2 levels were measured during the BH task using a nasal cannula, a gas analyzer (ADInstruments), and a BIOPAC MP150 system.
Data preprocessing and data analysis followed the same steps reported in [6]. Briefly, after a minimal data preprocessing, CVR and lag maps were first obtained in the Optimally Combined ME data (GLM with lagged HRF-convolved PETCO2 timeseries as covariate of interest; 12 motion parameters and Legendre polynomials as nuisance regressors). The same preprocessing was applied to the RS data, after which RS fluctuation amplitude (RSFA) was computed using AFNI’s 3dRSFC [7].
Both CVR BH and CVR RSFA maps were normalised to the MNI152 template, then the average value of 118 parcels were obtained using the Schaefer 2018 atlas (100 regions) [8] with the cerebellum and subcortical parcellation of the Destrieux 2010 atlas (18 subcortical and cerebellar regions) [9].
Due to the physiological difference between positive and negative CVR BH , voxels with positive CVR BH were analysed separately from voxels with negative CVR BH. Only those voxels that were always positive for all sessions and all subjects were considered for further analysis of positive CVR. Similarly, only those voxels that were always negative for all sessions and all subjects were considered for further analysis of negative CVR.
ICC(1) [10] was computed with a custom Python based algorithm for each parcel and for each voxel adopting subjects as objects of measurements and sessions as observations. Then, spearman's rho between CVR BH and CVR RSFA was computed for each subject across all parcels and sessions.

<img src="assets/images/methods.png" style="max-width:60%;display:block;" align="center"/>
*Figure 1: BreathHold task.*