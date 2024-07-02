# Election Results Analysis

## Description

This repository contains a Jupyter Notebook for analyzing the first-round results of the 2024 legislative elections in France. The analysis includes data processing, visualization, and exclusion of constituencies without a second round of voting.

## Data Sources

The data used in this analysis is sourced from the following locations:

- **Geographical boundaries of constituencies**: [Contours géographiques des circonscriptions législatives](https://www.data.gouv.fr/fr/datasets/contours-geographiques-des-circonscriptions-legislatives/)
- **Legislative election results**: [Résultats du 1er tour des élections législatives 2024 par circonscription](https://www.data.gouv.fr/fr/datasets/resultats-du-1er-tour-des-elections-legislatives-2024-par-circonscription/)

## Methodology

1. **Loading Data**: The notebook begins by importing necessary packages such as `pandas`, `geopandas`, and `matplotlib`. The election results data is loaded from a CSV file using `pandas`.

2. **Data Cleaning and Preparation**:
   - The dataset is filtered to exclude constituencies where the election was decided in the first round.
   - Unique candidate codes are extracted for further analysis.

3. **Analysis**:
   - The results are processed to understand the distribution of votes among different political parties.
   - Additional statistical analyses and visualizations are performed to identify trends and patterns.

4. **Visualization**: 
   - The notebook employs `matplotlib` to visualize the geographical distribution of election results.
   - Maps and charts are generated to provide insights into the election data.

## Results

The analysis provides several insights into the 2024 legislative election results, including:
- Distribution of votes by political party.
- Identification of constituencies moving to the second round.
- Geographical representation of voting patterns.

## Usage

To run the notebook, ensure you have the required packages installed. You can install them using `pip`:

```bash
pip install pandas geopandas matplotlib
