# Data Analysis for "Limits to the Policy Relevance of Past Climate Research"

[![DOI](https://zenodo.org/badge/926226329.svg)](https://zenodo.org/badge/latestdoi/926226329)

This repository contains R code necessary to reproduce the main analysis presented in *Degroot et al. ND, "Limits to the Policy Relevance of Past Climate Research"*:
1. A Quarto notebook with the R source code is available here: [analysis.qmd](analysis.qmd)
2. The raw data are available here: [Limits Database Final.xlsx](Limits%20Database%20Final.xlsx)
3. A prerendered HTML of the analysis is available for download here: [analysis.html](analysis.html)

## Installation and Requirements

### Software Requirements
- R (version 4.0+): https://cran.r-project.org/
- RStudio: https://posit.co/products/open-source/rstudio/

## R Package Dependencies
We used R version 4.4.2 (R Core Team 2024) and the following R packages: gtsummary v. 2.1.0 (Sjoberg et al. 2021), labelled v. 2.14.0 (Larmarange 2025), tidyverse v. 2.0.0 (Wickham et al. 2019). The figures additionally use patchwork and treemapify. RStudio will prompt to you install these required packages automatically if they are not available when you render the document.

### Running the Analysis
1. Download and extract the repository
2. Open the hcs-meta.Rproj file in RStudio (opens the project)
3. Open analysis.qmd 
4. Click "Render" button
5. Runtime: ~30 seconds

No special hardware required.
