# Molecular Cascade Reveals Sequential Milestones Underlying Hippocampal Neural Stem Cell Development into an Adult State 
## Table of Contents
1. [Summary](#summary)
2. [Highlights](#highlights)
6. [Methods](#methods)
## Summary
***
Quiescent adult neural stem cells (NSCs) in the mammalian brain arise from proliferating NSCs during development. Beyond acquisition of quiescence, an adult NSC hallmark, little is known about the process, milestones and mechanisms underlying the transition of developmental NSCs to an adult NSC state. Here we performed targeted single-cell RNA-seq analysis to reveal the molecular cascade underlying NSC development in the early postnatal mouse dentate gyrus. We identified two sequential steps, first a transition to quiescence followed by further maturation, each of which involved distinct changes in metabolic gene expression. Direct metabolic analysis uncovered distinct milestones, including an autophagy burst before NSC quiescence acquisition and cellular ROS level elevation along NSC maturation. Functionally, autophagy is important for the NSC transition to quiescence during early postnatal development. Together, our study reveals a multi-step process with defined milestones underlying establishment of the adult NSC pool in the mammalian brain

[DIO] https://doi.org/10.1016/j.celrep.2024.114339

* Code used for the next-generation single-cell RNA sequencing analysis accompanying the manuscript.
* Raw sequencing data can be found at GEO under the accession GSE232833.
## Highlights
***
  * NSC development into an adult state is a multi-step process with defined milestones
  * Molecular cascade underlying NSC quiescence acquisition and subsequent maturation
  * Sequential metabolic changes in autophagy and ROS during NSC development
  * Autophagy promotes NSC quiescence during early postnatal development
  
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
   * Static Gene Regulatory Networks (GRN) of clusters
   * Identification of variable gene aross pseuotime with kinetic patterns 
   * Dyanimc Gene Regulatory Networks (GRN) of sub-trajectory
   * Gene Ontological Analysis using clusterProfiler 

