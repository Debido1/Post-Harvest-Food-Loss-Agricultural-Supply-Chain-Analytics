# Reducing Post-Harvest Food Loss in Nigeria

## Project Overview

This project presents a Power BI analytics solution designed to
investigate post-harvest food losses across the agricultural supply
chain in Nigeria.

The project focuses on four connected areas: farm production, storage,
transportation, and market demand. The objective is to understand where
losses occur, identify factors associated with spoilage and damage, and
provide insights that could support better decisions around storage,
transportation, distribution, and market supply.

The dashboard was designed as a decision-support tool rather than simply
a collection of charts. It allows users to interact with the data by
crop type and state and explore how production, losses, transportation
performance, and market conditions vary across the dataset.

## Business Problem

Post-harvest losses can occur at several stages of the agricultural
supply chain. Produce can be lost or damaged during storage and
transportation, while poor distribution can also result in unsold or
spoiled produce at markets.

This project was created to investigate questions such as:

-   How much agricultural produce is being produced?
-   Which crops account for higher production and losses?
-   What are the main reported causes of storage loss?
-   How do storage conditions relate to spoilage?
-   How much produce is damaged during transportation?
-   How do vehicle type, distance, and road condition relate to
    transport losses?
-   Where are supply and demand mismatches occurring?
-   Which crops and market types generate higher revenue?
-   Where can interventions potentially reduce waste and financial
    losses?

## Business Objectives

The project was designed to:

-   Monitor overall crop production and production costs.
-   Analyse production trends over time.
-   Identify crops associated with higher levels of loss.
-   Analyse storage losses and their reported causes.
-   Examine the relationship between storage conditions and spoilage.
-   Evaluate transportation damage, fuel costs, travel time, and road
    conditions.
-   Analyse market demand, supply gaps, unsold quantities, spoilage, and
    selling prices.
-   Compare performance across crops, states, storage types, vehicle
    types, and market types.
-   Provide actionable insights that could support post-harvest loss
    reduction strategies.

## Tools and Technologies

-   Microsoft Power BI
-   Power Query
-   DAX
-   Power BI data modelling
-   Data visualisation
-   Google Drive for crop image assets
-   Synthetic dataset

## Dataset

The project uses synthetically generated data designed to simulate
agricultural supply-chain operations in Nigeria.

The data is organised into four main tables:

### Farm Production

Contains:

-   Farm ID
-   State
-   Crop type
-   Harvest date
-   Quantity harvested
-   Expected shelf life
-   Storage type
-   Initial quality
-   Production cost
-   Crop image URL

### Storage Loss

Contains:

-   Storage ID
-   Farm ID
-   Entry and exit dates
-   Quantity stored
-   Quantity spoiled
-   Temperature
-   Humidity
-   Storage cost
-   Loss reason

### Transportation

Contains:

-   Transport ID
-   Farm ID
-   Market ID
-   Vehicle type
-   Distance
-   Departure and arrival dates
-   Transport time
-   Fuel cost
-   Quantity transported
-   Quantity damaged
-   Road condition

### Market Demand

Contains:

-   Market ID
-   State
-   Market type
-   Crop type
-   Demand
-   Quantity received
-   Selling price
-   Unsold quantity
-   Produce spoiled at market

## Data Model

The Power BI model connects the agricultural datasets so that users can
analyse the supply chain across different stages.

The model includes relationships between:

-   Farm production and storage records through Farm ID.
-   Farm production and transportation through Farm ID.
-   Transportation and market demand through Market ID.
-   Crop information through crop type.
-   A dedicated date table for time-based analysis.

The model supports interactive filtering by crop type and state.

## Dashboard Pages

### 1. Overview

![Overview Dashboard](images/overview-dashboard.png)

The Overview page provides a high-level view of agricultural production
and the broader post-harvest landscape.

It analyses:

-   Total crop produced
-   Total production cost
-   Total market demand
-   Overall loss rate
-   Production by crop
-   Production by storage type
-   Monthly production trends
-   Geographic distribution of production and losses

A dynamic crop image component is also included to display the relevant
crop when a crop is selected.

### 2. Loss Analysis

![Loss Analysis Dashboard](images/loss-analysis-dashboard.png)

The Loss Analysis page focuses on identifying where and why produce is
being lost.

It analyses:

-   Total cost lost
-   Storage loss rate
-   Market loss rate
-   Transportation damage rate
-   Loss by crop
-   Main causes of storage loss
-   Loss rate by state
-   Temperature and spoilage relationship
-   Storage loss by storage type

Reported storage-loss causes include bruising, rot, pests, overheating,
and mold.

### 3. Transportation Analysis

![Transportation Dashboard](images/transportation-dashboard.png)

The Transportation page evaluates losses and costs associated with
moving agricultural produce from farms to markets.

It analyses:

-   Total quantity transported
-   Total fuel cost
-   Transportation damage rate
-   Average transport time
-   Fuel cost by vehicle type
-   Damage by vehicle type
-   Transport damage versus distance
-   Loss by road condition
-   Transportation cost efficiency

### 4. Market Analysis

![Market Analysis Dashboard](images/market-analysis-dashboard.png)

The Market Analysis page examines the relationship between market
demand, supply, revenue, pricing, and unsold produce.

It analyses:

-   Total revenue
-   Unsold quantity
-   Supply-demand gap
-   Average selling price per kilogram
-   Demand versus quantity received
-   Average price by crop
-   Revenue by market type
-   Unsold quantity by state
-   Overall market performance

A performance indicator is also included to provide a high-level view of
supply fulfilment within the dataset.

## Selected Findings

The dashboard surfaces several patterns within the synthetic dataset:

-   Cassava records the highest total production among the crops
    represented in the production dataset.
-   Total production is approximately 2 million kg in the full dataset.
-   Total production cost is approximately ₦498.8 million in the full
    dataset.
-   Storage loss represents an important component of the losses
    analysed.
-   Bruising, rot, pests, overheating, and mold appear as the reported
    storage-loss causes.
-   Transportation damage is approximately 15.4% in the full
    transportation dataset.
-   Open trucks account for a substantial share of transportation damage
    within the dataset.
-   The market dataset shows a substantial gap between recorded demand
    and quantity received.
-   Unsold produce is recorded across the states represented in the
    market data.

These findings describe patterns in the synthetic dataset and should not
be interpreted as official statistics about Nigeria's agricultural
sector.

## Business Insights and Recommendations

Potential areas for intervention identified from the dashboard include:

### Storage

-   Improve temperature and environmental monitoring.
-   Reduce unnecessary storage duration for sensitive crops.
-   Strengthen handling procedures to reduce physical damage.
-   Investigate storage conditions associated with higher spoilage.

### Transportation

-   Match vehicle types to crop sensitivity and journey requirements.
-   Review routes involving long travel distances.
-   Improve packaging and handling procedures.
-   Investigate the relationship between road conditions and
    transportation damage.

### Market Distribution

-   Improve coordination between demand and quantities supplied.
-   Monitor unsold and spoiled quantities at market level.
-   Improve distribution planning across states and market types.
-   Consider demand forecasting to support better supply allocation.

These recommendations are analytical suggestions based on the synthetic
dataset and are not presented as validated interventions for real-world
operations.

## Key Measures

The dashboard uses DAX measures to calculate and monitor metrics such
as:

-   Total Production
-   Total Production Cost
-   Total Demand
-   Total Loss
-   Loss Rate
-   Storage Loss
-   Market Loss Rate
-   Transportation Damage Rate
-   Total Quantity Transported
-   Total Fuel Cost
-   Average Transport Time
-   Transportation Cost Efficiency
-   Total Revenue
-   Unsold Quantity
-   Supply Gap
-   Average Selling Price
-   Month-over-month changes

A dedicated date table is used for time-based calculations and monthly
comparisons.

## Interactivity

The dashboard includes interactive slicers and cross-filtering to
explore the dataset by:

-   Crop type
-   State
-   Vehicle type
-   Market type
-   Storage type
-   Time period

Selecting a crop or state updates the relevant visuals and KPIs,
allowing users to move from an overall view to more specific operational
questions.

## Repository Structure

``` text
reducing-post-harvest-food-loss-nigeria/

├── README.md
├── power-bi/
│   └── post_harvest_food_loss_dashboard.pbix
├── images/
│   ├── overview-dashboard.png
│   ├── loss-analysis-dashboard.png
│   ├── transportation-dashboard.png
│   └── market-analysis-dashboard.png
├── data/
│   ├── farm_production.csv
│   ├── storage_loss.csv
│   ├── transportation.csv
│   └── market_demand.csv
└── documentation/
    └── project-documentation.pdf
```

## How to Explore the Project

1.  Download or clone the repository.
2.  Open the Power BI `.pbix` file using Power BI Desktop.
3.  Review the data model and relationships.
4.  Explore the four dashboard pages.
5.  Use the slicers to filter by crop, state, vehicle type, or market
    type.
6.  Select individual visuals to cross-filter other components of the
    dashboard.
7.  Review the KPIs, trends, and analytical visuals to understand the
    different stages of the agricultural supply chain.

## Data Disclaimer

This project uses **synthetically generated data** for educational,
analytical, and portfolio purposes.

The figures, farm records, market records, transportation records, and
loss measurements are simulated and should not be interpreted as actual
operational records or official statistics about Nigeria.

The project demonstrates how a similar analytics solution could be
applied to real agricultural supply-chain data.

## Author

**Deborah Enehi Apochi**

Data Analyst & Operations Lead

-   GitHub: [Debido1](https://github.com/Debido1)
