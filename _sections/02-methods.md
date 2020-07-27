---
layout: post
title: Methods
description: We asked 7 subects to undergo 10 MRI sessions, one week apart, and perform a BH task. We acquired ME data and applied different ME-ICA based denoising to remove motion effects. We then compared the reliability of each pipeline using intraclass correlation coefficient and measureing the relation between FD and DVARS.
image: methods.png
---

Seven healthy volunteers underwent 10 MRI sessions in a 3T Siemens PrismaFit scanner, spaced 1-week apart at the same time of day. A BH task (Fig. 1) adapted from [7] was administered at each session while collecting ME-fMRI data (340 scans, TR=1.5 s, TEs=10.6/28.69/46.78/64.87/82.96 ms, flip angle=70°, MB=4, GRAPPA=2, 52 slices, Partial-Fourier=6/8, FoV=211x211 mm2, voxel size=2.4x2.4x3 mm3). CO2 levels were measured using a nasal cannula, a gas analyzer (ADInstruments), and a BIOPAC MP150 system.
Data preprocessing and data analysis followed the same steps reported in [8]. Briefly, after a minimal data preprocessing (Fig. 2), CVR and lag maps were first obtained in the second TE (SE) and OC data (GLM with lagged HRF-convolved PETCO2 timeseries as covariate of interest; 12 motion parameters and Legendre polynomials as nuisance regressors, SE-MPR or OC-MPR, Fig. 3). 
The optimally combined volume was decomposed using ME-ICA [9], then noise and signal ICs were manually labelled, and three additional extended GLMs were created: adding the noise ICs timeseries directly as additional nuisance regressors (ME-AGG); orthogonalized w.r.t. the PETCO2 trace (ME-MOD); or orthogonalised w.r.t. the PETCO2 trace and signal ICs timeseries (ME-CON). FD [10] and DVARS [11] were computed before realignment (SE-PRE) and after removal of the fitted nuisance regressors from SE and OC data. The CVR and lag maps were registered to the MNI space, then ICC(2,1) [12] was computed to assess their reliability across sessions.


<img src="assets/images/methods.png" style="max-width:60%;display:block;" align="center"/>
*Figure 1: Left: Preprocessing and data analysis used in this study. Right: BreathHold task.*