# Sequential Milestones Underlying Hippocampal Neural Stem Cell Development into an Adult State
## Table of Contents
1. [Summary](#summary)
2. [Highlights](#highlights)
3. [Technologies](#technologies)
4. [Included Files](#technologies)
5. [Installations](#installations)
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
## Technologies
***
A list of technologies used within the project:
* [Seurat](https://satijalab.org/seurat/): Version X
* [Monocle](http://cole-trapnell-lab.github.io/monocle-release/): Version X
* [CellRouter](https://github.com/edroaldo/cellrouter): Version X
* [velocyto.R](http://velocyto.org/): Version X
* [SCENIC](https://scenic.aertslab.org/): Version X
## Included Files
***
### Analysis Scripts
* AtoQ.R a script to recreate the entire analysis (running all the figure scripts below and generating all plots).
### Figures 
* Scripts to recreate the plots used  in figures 2 and 3 (and some supplementary data) of the manuscript. Scripts can be found in Figures/Figure.R 
### Data
* Results of original analysis as an rds object with and DataCollection class including loom file result from RNAVelocyto as an rds file
### Resources
* AtoQlibrary.R a library supplementing to run AtoQ.R script
### Expression matrices
* Supplementary tables from manuscript and expression matricies to run analysis (includes TPM and SCT normalized matricies) and vizualize result uisng monocle functions
### Installations
***
To recreate fiugres and data from manuscript you will need to install several base packages
```
list.of.packages <- c( "")
new.packages <- list.of.packages[!(list.of.packages %in% installed.packages()[,"Package"])]

if(length(new.packages)) install.packages(new.packages, repos=c("http://cran.rstudio.com/", "https://bioconductor.org/biocLite.R"))
```
In case of a missing package after running the steps above, please install them by typing:
```
source('http://bioconductor.org/biocLite.R')
biocLite('package_name')
```
Please install Monocle, and velocyto.R and sorce our library to successfully run figures and data from manuscript. Our library contains the [CellRouter class](https://github.com/edroaldo/cellrouter/blob/master/CellRouter_Class.R), so please make sure you provide the correct directory for the Java libraries inside the folder "AtoQ", as specified by the variable 'libdir'. If you experience errors running CellRouter please run their CellRouter_Class.R script. Manuscript result pertaining to any bioinformatic code is found in a [DataCollection class] within the Code section of this repository.
```
BiocManager::install("monocle")

library(devtools)
install_github("velocyto-team/velocyto.R")

source('path/to/AtoQ.R')
ibdir <- 'path/to/AtoQ/'
```
Additional packages
```
BiocManager::install("clustree")
BiocManager::install("bluster")
BiocManager::install("clusterProfiler")
```
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

