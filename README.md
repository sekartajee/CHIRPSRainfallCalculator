# CHIRPS Rainfall Calculation Tool

A custom ArcGIS ModelBuilder tool designed to automate rainfall aggregation
from CHIRPS raster data for GIS analysis and reporting.

## Tools & Technologies
- ArcMap
- Python
- CHIRPS rainfall dataset

## Workflow Overview
1. Input CHIRPS raster data
2. Spatial clipping to the area of interest
3. START and END of data time frame
4. Output Coordinate System
5. Aggregation Type
6. Z value field: pick GRID_CODE
7. Output shapefile and tabular summaries

## Tool Architecture

This tool consists of two ArcGIS ModelBuilder models:

### 1. Main Model — `Rainfall Calculation`
- Handles user inputs and validation
- Calls the aggregation submodel
- Manages final outputs (rasters and tables)

### 2. Submodel — `extracted points`
- Performs temporal rainfall aggregation
- Processes raster time series
- Returns summarised outputs to the main model

The submodel is nested inside the main model to allow
modular reuse and easier maintenance.

## Notes
- Python scripting in this project is partially AI-assisted.
- The workspace paths are hardcoded for now
