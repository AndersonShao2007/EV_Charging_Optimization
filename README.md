# Optimizing EV Charging Station Placement in the Bay Area

## Overview

Electric vehicle adoption in the San Francisco Bay Area has grown faster than the region’s charging infrastructure. This project develops a data-driven model for estimating charging demand and recommending where new Level 2 and fast-charging stations should be installed.

The analysis combines population density, traffic flow, EV registrations, and existing charging infrastructure. A GA-BP neural network is used to predict demand, while Binary Particle Swarm Optimization identifies high-priority locations for future stations.

## Research Question

Where should new EV charging stations be installed in the Bay Area to improve accessibility, reduce wait times, and prepare for future EV adoption?

## Methods

The project follows four main steps:

1. Collect and clean demographic, traffic, EV-registration, and charging-station data.
2. Combine the datasets by ZIP code or geographic region.
3. Predict future charging demand using a GA-BP neural network.
4. Use Binary Particle Swarm Optimization to recommend station locations under geographic and infrastructure constraints.

### Models

- **GA-BP Neural Network:** A backpropagation neural network whose parameters are optimized using a genetic algorithm.
- **Binary Particle Swarm Optimization:** A location-selection algorithm used to identify which areas should receive additional chargers.

## Data

The model uses:

- EV registrations
- Population density
- Traffic volume
- Existing charging-station locations
- Charger type and capacity
- Geographic information



## Key Results

The model identified several areas with large projected infrastructure shortages. ZIP code 94104 was estimated to require approximately:

- 322 additional fast chargers
- 11,229 additional Level 2 chargers

The proposed expansion strategy prioritizes urban areas before expanding into suburban and rural communities. The model estimates that the recommendations could reduce average wait times by 25% and improve station utilization by 20%.


## Repository Structure

```text
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_exploratory_analysis.ipynb
│   ├── 03_demand_prediction.ipynb
│   └── 04_location_optimization.ipynb
├── data/
├── results/
├── figures/
├── requirements.txt
└── README.md
