# SNAP
Single cell neighborhood map (SNAP)
# Spatial Transcriptomics Analysis

This repository contains the `SNAP.R` script,  designed for analyzing spatial transcriptomics data generated using the 10x Genomics Visium platform. The script facilitates the integration and examination of spatial gene expression patterns, aiding in the understanding of tissue architecture and cellular interactions.

## Overview

Spatial transcriptomics enables the mapping of gene expression within tissue sections, preserving spatial context. The `SNAP.R` script processes Visium data to identify spatial gene expression patterns, cell-type distributions, and potential interactions within the tissue microenvironment.

## Features

- **Data Preprocessing**: Loads and preprocesses Visium spatial transcriptomics data.
- **Spatial Clustering**: Identifies spatial domains within tissue sections based on gene expression profiles.
- **Visualization**: Generates spatial plots to visualize gene expression patterns and clustering results.
- **Integration with Single-Cell Data**: Aligns spatial data with single-cell RNA sequencing (scRNA-seq) data for enhanced cell-type identification.

## Requirements

- R (version 4.0 or higher)
- R packages:
  - `Seurat`: For single-cell RNA-seq data analysis.
  - `SpatialExperiment`: To handle spatially resolved transcriptomics data.
  - `ggplot2`: For data visualization.
  - `dplyr`: For data manipulation.
  - `patchwork`: For combining multiple plots.

## Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yanailab/PanCancer.git
   cd PanCancer
   ```

2. **Install required R packages**:

   Open an R session and run:

   ```R
   install.packages(c("Seurat", "ggplot2", "dplyr", "patchwork"))
   if (!requireNamespace("BiocManager", quietly = TRUE))
       install.packages("BiocManager")
   BiocManager::install("SpatialExperiment")
   ```

## Usage

1. **Load the script**:

   In your R session, source the `SNAP.R` script:

   ```R
   source("SNAP.R")
   ```

2. **Run the analysis**:

   Follow the functions and workflows defined in the script to process your Visium data. Ensure your data is in the correct format as expected by the script.

## References
- Barkley, D., Moncada, R., Pour, M., et al. Cancer cell states recur across tumor types and form specific interactions with the tumor microenvironment. [*Nature Genetics*, 54(8), 1192-1201.](https://www.nature.com/articles/s41588-022-01141-9) 
- 10x Genomics Visium Spatial Gene Expression: [https://www.10xgenomics.com/products/spatial-gene-expression](https://www.10xgenomics.com/products/spatial-gene-expression)
- Seurat Package: [https://satijalab.org/seurat/](https://satijalab.org/seurat/)
- SpatialExperiment Package: [https://bioconductor.org/packages/SpatialExperiment/](https://bioconductor.org/packages/SpatialExperiment/)

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

We acknowledge the developers of Seurat and SpatialExperiment for providing essential tools for spatial transcriptomics analysis. 
