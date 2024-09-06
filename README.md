# Africa-Infrastructure-Explorer
**Visualizing infrastructure gaps in piped water and electricity access across Africa using Afrobarometer survey data and predictive modeling.**

## Overview

This project aims to visualize critical aspects of infrastructure and essential services across Africa using data from the Afrobarometer Round 7 and Round 8 surveys. The focus is on mapping areas with piped water access, sewage systems, electricity grids, and cell service. Additionally, a Random Forest model is employed to predict piped water access based on various survey variables.

## Features

- **Geospatial Visualizations**: Interactive maps displaying piped water access, electricity grid availability, sewage systems, and cell service across Africa.
- **Infrastructure Gaps**: Identifies regions lacking essential services using visual markers.
- **Random Forest Predictions**: A machine learning model that predicts piped water access based on survey responses.

## Data Source

The data used in this project is sourced from the Afrobarometer survey network, specifically Rounds 7 (2017) and 8 (2019). Afrobarometer collects public opinion data on democracy, governance, the economy, and social issues across Africa.

- **Afrobarometer Round 7**: 45,826 entries
- **Afrobarometer Round 8**: 48,088 entries

## Methodology

### Pre-Visualization Data Cleaning

1. Retained only relevant columns (piped water access, electricity grid presence, sewage system, and cell service).
2. Removed indecision responses (-1 and 9 values), filtering approximately 900 rows.
3. Extracted geospatial data (latitude, longitude) for heatmap generation.

### Random Forest Model

- Focused on predicting piped water access, as there were no reliable predictors for electricity grid availability.
- The model's accuracy improved from **0.7627** in Round 7 to **0.7954** in Round 8.
- The most significant predictors were:
  - **Sewage System Availability**
  - **Water Source Location**

### Visualizations

The visualizations display regions with and without essential services, such as:

- **Blue Points**: Areas with piped water access.
- **Yellow Points**: Areas with electricity grid presence.
- **White Points**: Areas lacking both services.
- **1's and 0's Overlays**: Indicate cell service or sewage system availability.

### Random Forest Prediction

The Random Forest model can be used to predict piped water access based on various survey variables, including sewage system availability, water source location, and more.
