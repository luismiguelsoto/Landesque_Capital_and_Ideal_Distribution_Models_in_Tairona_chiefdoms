Landesque Capital and Ideal Distribution Models: Mapping Agricultural Suitability in the Sierra Nevada de Santa Marta, Colombia (under review)
--------------------------------------------------------------

This repository contains code and data for the spatial and statistical analysis presented in the manuscript submitted to the Journal of Anthropological Archaeology. The study evaluates whether agricultural intensification in the Río Frío basin led to increasingly restricted access to favorable terrain or whether settlement remained closely aligned with environmental opportunity across the Neguanje (AD 100–700), Buritaca (AD 700–1000), and Tairona (AD 1000–1600) periods. The analysis integrates terrain derivatives with machine learning classifiers, spatial cross-validation, and temporal comparison to generate a continuous suitability surface for terraced agriculture and test expectations derived from Ideal Free and Ideal Despotic Distribution models.

Repository Structure:
----------------------------------
1. GIS:
   - Contains all spatial data files required to reproduce the analysis:
     • ALL_STRUCTURES (shp)
     • NEGUANJE_STRUCTURES (shp)
     • BURITACA_STRUCTURES (shp)
     • TAIRONA_STRUCTURES (shp)
     • NEGUANJE_POLYGONS_SITES (shp)
     • BURITACA_POLYGONS_SITES (shp)
     • TAIRONA_POLYGONS_SITES (shp)
     • RIO_FRIO_POLYGON_SURVEY (shp)
     • RIVERS_POLYGON_52KM (shp)
     • DEM_POLYGON_52KM.tif (shp)
     • PREDICTORS_STACK_V11.tif (shp)
     • bg_points_V11.rds — Frozen background points for full reproducibility across sessions

2. R Code Files:
   - The main R script (or R Markdown file) contains the code to:
     a) Download all spatial datasets directly from this GitHub repository via the API.
     b) Derive five terrain covariates from the DEM (Elevation, Slope, TPI, TWI, Distance to DEM-derived channels).
     c) Fit a binomial GLM and a GAM sensitivity analysis to model terrace occurrence probability.
     d) Assess predictor collinearity through Variance Inflation Factors.
     e) Evaluate residual spatial autocorrelation via Global Moran's I and empirical variograms.
     f) Implement spatial block cross-validation with five square blocks of approximately 2 km.
     g) Generate a continuous agricultural suitability surface classified into six quantile-based categories.
     h) Compare settlement distributions across suitability classes for each archaeological period (chi-square test).
     i) Analyze terrace diameter distributions across suitability zones (Kruskal-Wallis, ECDF, upper-tail percentiles).
     j) Calculate catchment-level access to favorable land using spatially blocked bootstrap medians with 10,000 iterations.
     k) Produce all figures (Figures 4–10) and summary tables (Tables 1–2) as reported in the manuscript.

Software and Key Package Versions:
----------------------------------
- R version: [R 4.5.2]
- Key R packages used in this project include (with version numbers):
     • blockCV: version 3.1-5
     • boot: version 1.3-32
     • broom: version 1.0.7
     • car: version 3.1-5
     • classInt: version 0.4-11
     • dplyr: version 1.2.0
     • forcats: version 1.0.0
     • ggplot2: version 4.0.2
     • ggpubr: version 0.6.0
     • ggspatial: version 1.1.10
     • gridExtra: version 2.3
     • gstat: version 2.1-2
     • httr: version 1.4.7
     • jsonlite: version 1.9.1
     • knitr: version 1.49
     • mgcv: version 1.9-1
     • patchwork: version 1.3.0
     • pROC: version 1.18.5
     • RColorBrewer: version 1.1-3
     • rstatix: version 0.7.2
     • scales: version 1.3.0
     • sf: version 1.0-24
     • spdep: version 1.4-2
     • terra: version 1.8-42
     • tidyr: version 1.3.2
     • viridis: version 0.6.5

Getting Started:
----------------------------------
1. Clone or download this repository.
2. Open JAA_R_NOTEBOOK.Rmd in RStudio.
3. Run the notebook from top to bottom. The script automatically downloads all required spatial data from this repository via the GitHub API, so no local path configuration is needed.
4. All figures, tables, and numerical summaries reported in the manuscript are reproduced in sequence.

Manuscript Summary:
----------------------------------
Terraced agriculture in the Río Frío basin offers a long-term record of how Tairona communities organized productive landscapes during demographic growth and political reorganization. This study asks whether intensification led to increasingly restricted access to the most favorable agricultural sectors or whether settlement remained closely aligned with environmental opportunity. The results show persistent concentration of terraces and settlements in favorable corridors rather than progressive displacement into poorer terrain. Residential terraces do not show a simple increase in size with land quality, and surrounding productive land remained broadly comparable across communities through time. These patterns distinguish the Río Frío trajectory from comparative cases in which growing sociopolitical inequality became materially tied to more restricted occupation of prime sectors. At the same time, the evidence does not justify equating spatial persistence with social equality. The results indicate that intensification and hierarchy developed without evidence for progressive spatial monopolization, while leaving open the possibility that inequality operated through labor, returns, or tenure rather than overt territorial exclusion.

For questions or further information, please contact: lms313@pitt.edu
