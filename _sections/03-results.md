---
layout: post
title: Results
description: Considering the relationship between FD and DVARS and the ICC analysis, a conservative ME-ICA denoising approach is the best way to reduce impact of motion without compromising reliability in CVR mapping. Otherwise, a conventional OC approach is recommended, but with less reduction of motion effects.
image: results.png
---

Considering the relationship between FD and DVARS (Fig. 4-5) and the ICC analysis (Fig. 6), a conservative ME-ICA denoising approach is the best way to reduce impact of motion without compromising reliability in CVR mapping. Otherwise, a conventional OC approach is recommended, but with less reduction of motion effects. Further studies should extend these results to other fMRI with substantial collinear artefacts.


<img src="assets/images/results_1.png" style="max-width:100%;display:block;" align="center" />
*Figure 2: CVR map for each denoising and session of a representative subject*

<img src="assets/images/results_2.png" style="max-width:100%;display:block;" align="center" />
*Figure 3: Lag map for each denoising and session of a representative subject*

<img src="assets/images/results_3.png" style="max-width:100%;display:block;" align="center" />
*Figure 4: FD vs DVARS correlation for a representative subject, and (B) for all subjects for all of the analysis approaches. A lower
slope in the correlation means lower residual motion effects and better motion denoising.*

<img src="assets/images/results_4.png" style="max-width:100%;display:block;" align="center" />
*Figure 5: Right: BH responses in %DVARS and %BOLD. Left: Tendency to average in all the trials.*

<img src="assets/images/results_5.png" style="max-width:100%;display:block;" align="center" />
*Figure 6: Thresholded (>0.4) voxelwise ICC(2,1) of CVR and lag in MNI space. Note how optcom and meica-con have the best reliability
for both CVR and lag maps, while meica-agg has the lowest in both. ICC below 0.4 indicates poor reliability.*