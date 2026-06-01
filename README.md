# Driving the Transition: An Analysis of Electric Vehicle Adoption Across the United States


- [Driving the Transition: An Analysis of Electric Vehicle Adoption Across the United States](#driving-the-transition-an-analysis-of-electric-vehicle-adoption-across-the-united-states)
  - [Project Introduction](#project-introduction)
  - [Project Goals](#project-goals)
  - [Questions to Answer](#questions-to-answer)
  - [Data Source](#data-source)
  - [Tech Stack](#tech-stack)
  - [Data Cleaning \& Preparation](#data-cleaning--preparation)
  - [Analysis \& Key Findings](#analysis--key-findings)
    - [1. Fuel Mix by State](#1-fuel-mix-by-state)
    - [2. EV Adoption Leaders \& Laggards](#2-ev-adoption-leaders--laggards)
    - [3. Alternative Fuels — Significant vs. Niche](#3-alternative-fuels--significant-vs-niche)
    - [4. Infrastructure Investment Gaps](#4-infrastructure-investment-gaps)



## Project Introduction

This project analyzes electric and traditional vehicle registrations across all 50 U.S. states. The objective is to provide data-driven insights and recommendations to policymakers and automakers. 

**Stakeholder:** Transportation Research Group

## Project Goals
  
- Determine lagging and leading states in EV adoption
  
- Compare EV adoption against traditional fuel vehicle market
  
- Provide actionable recommendations for infrastructure investment for policymakers and automakers. 

## Questions to Answer

- What percentage of vehicles in each state are EVs, PHEVs, HEVs, and gasoline?
  
- Which states have the highest EV adoption rates, and which states lag behind?

- Which alternative fuels (biodiesel, ethanol, hydrogen) are significant vs. niche?

- Where should policymakers prioritize EV infrastructure investment based on adoption trends and gaps in support?

## Data Source

[Click here to download the raw data](Data/vehicle_data_raw.csv)

[Click here to download the cleaned data](Data/vehicle_data_final.xlsx)


## Tech Stack

- Excel & Power Query - Data preparation & cleaning
- Power BI - Data visualization and dashboards

## Data Cleaning & Preparation

The provided raw data was cleaned and prepared for visualization through Power Query and afterwards connected to Power BI for visualization. Full list of issues/observations and actions taken for cleaning can be found in the table below.

| # | Issue/Observation | Action Taken |
|---|---|---|
| 1.|Data is in wide format with one row per each state and fuel type. This format interferes with filtering and aggregation during visualization in Power BI | Un-pivoted the fuel type column and to convert the data to long format |
|2.| A separate column required to categorize "EV" and "Non-EV" fuel sources| Created a separate reference table containing "EV" or "Non-EV" for each fuel type and merged it with the data to create EV_Non_EV column|
|3. |A separate column was necessary to categorize fuel sources as "Mainstream" or "Alternative" | Updated the reference table to include the required categories and made the required changes in the Query|
|4. | State column did not have any duplicates or data quality issues| No action required. Data is available for all 50 U.S. states. **Discussion with the stakeholder may be required to gauge if the scope should expand to U.S. territories**  |
|5. | Hydrogen registration count was available for California only.|  Since we do not know if this lack of data for other states is due to issues in the data collection, the data was not removed. **The stakeholder must validate the accuracy of this approach**|
|6. | Methanol has no data for any state. | Since the column is not useful in the analysis, we removed it to reduce processing time. **The stakeholder must validate the accuracy of this approach**|
|7.|"Unknown Fuel" registrations were available |"Unknown Fuel" registrations were retained and categorized as equivalent to Gasoline for the scope of this analysis. **The stakeholder must validate the accuracy of this approach**.|


## Analysis & Key Findings

### 1. Fuel Mix by State
### 2. EV Adoption Leaders & Laggards  
### 3. Alternative Fuels — Significant vs. Niche
### 4. Infrastructure Investment Gaps