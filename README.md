This code is used to create a dimension reduction plot of the axolotl injury recovery data to identify novel cell type populations. 

## Background

The axolotl is a highly regenerative vertebrate with a somewhat unique ability to regenerate complex tissues upon losing them. Studies have sought to study how this regeneration occurs and characterize the cell types in case it may provide insights for regenerative medicine. We hope to characterize some of the observed heterogeinity in axolotls and link this to known genes involved in diseases of cell proliferation (i.e. cancer) and tissue formation. This will provide insights into how regeneration is conferred and regulated and insights that can be provided from new single-cell methods (i.e. MARS) can more thoroughly explore and characterize the data. Our aims are as follows:

Aim 1. Identify rare populations of cells at different time points during regeneration. 

Aim 2. Dissect the genetic drivers of cell state transition at different time points during regeneration.

## Data

The data used in this analysis is available in the Data folder of this repository (repo). The data used was a single-cell RNA-seq (scRNAseq) set available from the publication DOI: 10.1126/science.aaq0681 and the Genome Ascenion Viewer at GSE106269. The gene matrix of counts of genes by cell ID is available in .csv form. There is currently only one file the aaq0681_TableS5.csv which is a matrix of counts of the gene expression by cell ID (rows) and gene name (column) of the scRNAseq dataset available for the uninjured axolotl upper arm connective tissue (Single-cell RNA-seq data set (10X Genomics) of 2,375 cells of the axolotl uninjured adult upper arm CT).

## Installation

This repo requires the Seurat library for R (4.0.4) in order to analyze scRNA-seq data. In order to install R , one can follow the instructions available on the R website: https://www.r-project.org/

Installation of the Seurat library can be performed in R as follows:
```
install.packages('Seurat')
```

## Usage

The analysis code assumes the same structure as the current repo is used. One can run the following command directly from the be440project directory to analyze the data:

```
Rscript Script/main.R
```

The output is an Rplots.pdf file in the Figures directory containing a clustering analysis (Shared nearest neighbor) plotted in a UMAP plot and feature plots for four key tissue regulation genes. 

## References

1. Leigh ND, Dunlap GS, Johnson K, et al. Transcriptomic landscape of the blastema niche in regenerating adult axolotl limbs at single-cell resolution. Nat Commun. 2018;9(1):5153. 
2. Gerber T, Murawala P, Knapp D, et al. Single-cell analysis uncovers convergence of cell identities during axolotl limb regeneration. Science. 2018;362(6413).
3. Qin T, Fan CM, Wang TZ, et al. Single-cell RNA-seq reveals novel mitochondria-related musculoskeletal cell populations during adult axolotl limb regeneration process. Cell Death Differ. 2021;28(3):1110-1125.
4. Oviedo NJ, Beane WS. Regeneration: The origin of cancer or a possible cure?. Semin Cell Dev Biol. 2009;20(5):557-564. doi:10.1016/j.semcdb.2009.04.005
5. Sibai M, Parlayan C, Tuğlu P, Öztürk G, Demircan T. Integrative Analysis of Axolotl Gene Expression Data from Regenerative and Wound Healing Limb Tissues. Sci Rep. 2019;9(1):20280. Published 2019 Dec 30. doi:10.1038/s41598-019-56829-6
6. Brbić, M., Zitnik, et al. MARS: discovering novel cell types across heterogeneous single-cell experiments. Nature methods. 2020, 17(12), 1200–1206.
7. Yuhan Hao, Stephanie Hao, Erica Andersen-Nissen et al. Integrated analysis of multimodal single-cell data. BioRxiv. 2020.10.12.335331. doi: https://doi.org/10.1101/2020.10.12.335331
