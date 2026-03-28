Landesque Capital and Ideal Distribution Models: Mapping Agricultural Suitability in the Sierra Nevada de Santa Marta, Colombia (under review)
--------------------------------------------------------------

This repository contains code and data for the spatial and statistical analysis presented in the manuscript submitted to the Journal of Anthropological Archaeology. The study evaluates whether agricultural intensification in the Río Frío basin led to increasingly restricted access to favorable terrain or whether settlement remained closely aligned with environmental opportunity across the Neguanje (AD 100–700), Buritaca (AD 700–1000), and Tairona (AD 1000–1600) periods. The analysis integrates terrain derivatives with statistical, semi-parametric, and machine learning classifiers, spatial cross-validation, and temporal comparison to generate a continuous suitability surface for terraced agriculture and test expectations derived from Ideal Free and Ideal Despotic Distribution models.

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
     • DEM_POLYGON_52KM.tif
     • PREDICTORS_STACK_V11.tif
     • bg_points_V11.rds — Frozen background points for full reproducibility across sessions

2. R Code Files:
   - The main R script (or R Markdown file) contains the code to:
     a) Load required packages.
     b) Download the datasets and GIS files directly from GitHub.
     c) Process environmental variables and perform House-Lot spatial analysis.
     d) Generate the figures or tables as presented in the manuscript.

Software and Key Package Versions:
----------------------------------
- R version: 4.5.2
- Key R packages used in this project include (with version numbers):
     • blockCV: 3.1-5
     • boot: 1.3-32
     • broom: 1.0.7
     • car: 3.1-5
     • classInt: 0.4-11
     • dplyr: 1.2.0
     • forcats: 1.0.0
     • ggplot2: 4.0.2
     • ggpubr: 0.6.0
     • ggspatial: 1.1.10
     • gridExtra: 2.3
     • gstat: 2.1-2
     • httr: 1.4.7
     • jsonlite: 1.9.1
     • knitr: 1.49
     • mgcv: 1.9-1
     • patchwork: 1.3.0
     • pROC: 1.18.5
     • ranger: 0.17.0
     • RColorBrewer: 1.1-3
     • rstatix: 0.7.2
     • scales: 1.3.0
     • sf: 1.0-24
     • spdep: 1.4-2
     • terra: 1.8-42
     • tidyr: 1.3.2
     • viridis: 0.6.5

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
