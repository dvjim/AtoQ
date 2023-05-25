# Sequential Milestones Underlying Hippocampal Neural Stem Cell Development into an Adult State
## Table of Contents
1. [Summary](#summary)
2. [Highlights](#highlights)
6. [Methods](#methods)
## Summary
***
Quiescent adult neural stem cells (NSCs) in the mammalian brain arise from proliferating NSCs
during development. It is unknown whether the transition to an adult NSC state is simply a
switch to quiescence, a hallmark of adult NSCs, or a more complex yet unknown process. Here
we investigated intrinsic NSC dynamics across early postnatal stages in the mouse dentate
gyrus at cellular, molecular and metabolic levels. We found that NSCs shift cell cycle dynamics
to increase occupancy in the G2/M phase before quiescence acquisition. Single-cell RNA-seq
identified the molecular cascade underlying two phases with the transition to quiescence,
followed by further NSC maturation. Metabolic analysis further revealed a burst of autophagy
before quiescence acquisition and elevated cellular ROS levels with NSC maturation. Our study
demonstrates that NSC development into an adult state is not a singular switch from
proliferation to quiescence but is a multi-step developmental process with defined milestones.

[DIO] 

* Code used for the next-generation single-cell RNA sequencing analysis accompanying the manuscript.
* Raw sequencing data can be found at GEO under the SuperSeries accession GSEXXX.
## Highlights
***
  * NSC development into an adult state is a multi-step process
  * NSC occupancy in the G2/M cell cycle phase increases before quiescence acquisition
  * Molecular cascade underlying NSC quiescence acquisition and subsequent maturation
  * Metabolic changes in autophagy &amp; ROS occur during early and late NSC development
  * 
## Methods
***
Please see manuscript for full detail of methods. Below is an outline of general processes taken in data collection and analysis
* RNA processing 
  * SMART-Seq2 and Tn5 buffer system
* Data processing 
  * RSEM and STAR based mapping and TPM calculation
  * Seurat SCT normalization
  * Clustering using Monocle 
* Data Analysis 
   * Creation of pseudotime trajectory and identify sub-trajectories
   * Static Gene Regulatory Networks of clusters
   * Identification of variable gene aross pseuotime with kinetic patterns 
   * Dyanimc Gene Regulatory Networks of sub-trajectory
   * Gene Ontological Analysis using clusterProfiler 

