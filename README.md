# Species Habitat Modelling 

## Project Overview

This project focuses on modeling and predicting suitable habitats for the **Great Hornbill (Buceros bicornis)** within the **Malay Peninsula**. The study employs classical Species Distribution Models (SDMs) like MaxEnt and Bioclim, enhanced by Machine Learning techniques such as Random Forests. The ecological data was processed and analyzed in R, with habitat suitability mapped using QGIS.

## Study Area and Species

- **Species:** Great Hornbill (*Buceros bicornis*)
- **Study Area:** Malay Peninsula (Geographic extent: 99°E to 105°E, 1.2°N to 6.7°N)

## Key Features

- **Species Distribution Models (SDMs):** Implemented MaxEnt and Bioclim to predict the distribution of the Great Hornbill based on climatic variables within the Malay Peninsula.
- **Machine Learning:** Applied Random Forests to refine and enhance habitat suitability predictions.
- **Data Processing:** Managed and optimized ecological datasets within R to streamline SDM workflows.
- **Spatial Analysis:** Utilized QGIS to visualize and map habitat suitability using spatial and ecological data.

## Tools and Technologies

- **R:** Data processing and SDM modeling using packages like `geodata`, `raster`, `dismo`, and `sf`.
- **QGIS:** Spatial data visualization and habitat mapping.
- **Stadia Maps API:** Used for fetching basemaps for geographic visualization.
- **MaxEnt and Bioclim:** For species distribution modeling.
- **Random Forests:** For machine learning-based habitat suitability predictions.

## Code and Workflow

The R code for this project is structured to:

1. Load and prepare ecological data specific to the Great Hornbill.
2. Define geographic extents and bounding boxes for the Malay Peninsula.
3. Generate and visualize basemaps and habitat suitability maps.
4. Implement Bioclim models and predict the Great Hornbill's distribution.
5. Evaluate model performance using ROC curves.

### Example Code Snippets

```r
# Load Data
horn <- read.csv("hornbill_my1.csv")
horn1 <- horn[,-1]  # Remove the first column
worldclim <- worldclim_global(var = "bio", res = 10, path = tempdir("C:\\Users\\dy0053tu\\Desktop\\r_data"))

