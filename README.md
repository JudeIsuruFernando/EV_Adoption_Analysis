# Driving the Transition: An Analysis of Electric Vehicle Adoption Across the United States


- [Project Introduction](#project-introduction)
- [Project Goals](#project-goals)
- [Questions to Answer](#questions-to-answer)
- [Data Source](#data-source)
- [Tech Stack](#tech-stack)
- [Data Cleaning \& Preparation](#data-cleaning--preparation)
- [Analysis \& Key Findings](#analysis--key-findings)
  - [Fuel Mix](#fuel-mix)
  - [EV Adoption Leaders \& Laggards](#ev-adoption-leaders--laggards)
  - [Alternative Fuels — Significant vs. Niche](#alternative-fuels--significant-vs-niche)
  - [Infrastructure Investment Gaps](#infrastructure-investment-gaps)
- [Recommendations](#recommendations)
- [Limitations](#limitations)



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

[Click here to download the raw data](Data/Raw%20Data/vehicle_data_raw.csv)

[Click here to download the cleaned data](Data/Processed%20Data/vehicle_data_final.xlsx)


## Tech Stack

- Excel & Power Query - Data preparation & cleaning
  
- Power BI - Data visualization and dashboards

## Data Cleaning & Preparation

The provided raw data was cleaned and prepared for visualization through Power Query and afterwards connected to Power BI for visualization.

Full list of issues/observations and actions taken for cleaning can be found in the table below.

| # | Issue/Observation | Action Taken |
|---|---|---|
| 1.|Data is in wide format with one row per each state and fuel type, interfering with filtering and aggregation during visualization in Power BI | Un-pivoted the fuel type column and to convert the data to long format |
|2.| A separate column required to categorize "EV" and "Non-EV" fuel sources| Created a separate reference table containing "EV" or "Non-EV" for each fuel type and merged it with the data to create EV_Non_EV column|
|3. |A separate column was necessary to categorize fuel sources as "Mainstream" or "Alternative" | Updated the reference table to include the required categories and made the required changes in the Query|
|4. | State column did not have any duplicates or data quality issues| No action required. Data is available for all 50 U.S. states. **Discussion with the stakeholder may be required to gauge if the scope should expand to U.S. territories**  |
|5. | Hydrogen registration count was available for California only.|  Since we do not know if this lack of data for other states is due to issues in the data collection, the data was not removed. **The stakeholder must validate the accuracy of this approach**|
|6. | Methanol has no data for any state. | Since the column is not useful in the analysis, we removed it to reduce processing time. **The stakeholder must validate the accuracy of this approach**|
|7.|"Unknown Fuel" registrations were available |"Unknown Fuel" registrations were retained and categorized as equivalent to Gasoline for the scope of this analysis. **The stakeholder must validate the accuracy of this approach**.|


## Analysis & Key Findings

### Fuel Mix

- Across all states, Gasoline is leading at 95% of all registrations

**Gasoline vs EV Screenshot**

- Within the EV market, HEVs claim more than half the market at 60% while the rest is filled by EVs and PHEVs.

**EV Market Screenshot**

- The key takeaway is that while the Gasoline is the current fuel of choice, the market is in the early stages of adopting EVs.

### EV Adoption Leaders & Laggards

- Large states such as California, District of Columbia and Washington are leading in EV adoption.
  
- However, smaller states such as Hawaii are making inroads as well.

**EV Adoption Top and Bottom 5 Screenshot**


- States such as North Dakota, Mississippi and Wyoming are lagging in EV adoption.

- In general, states located in the West Coast are embracing EVs while midwestern and southern states are lagging behind.

-  Possible reasons might include
   -  lack of EV infrastructure
   -  limited state-level policy initiatives.
   -  cultural affinity towards internal combustion engines.

**EV Adoption Heatmap Screenshot**

### Alternative Fuels — Significant vs. Niche

- Alternative fuels (Ethanol, Biodiesel,Compressed Natural Gas (CNG), Hydrogen & Propane) account for only 8% of all registrations with EVs being classified as mainstream fuel for the purpose of this analysis.

- Out of all alternative fuel registrations, Ethanol (88%) & Biodiesel (12%) show significant adoption.
  
- Compressed Natural Gas (CNG), Hydrogen & Propane  collectively represent less than 1% of all alternative fuel registrations.

- A possible cause is that internal combustion engines have greater compatibility with Ethanol and Biodiesel, making the transition to them more convenient and cost-effective

- Based on these observations, it is recommended to prioritize spending on charging infrastructure and incentive programs and allocate minimal spending for alternative fuels until adoption rates justify increased spending.


### Infrastructure Investment Gaps

Using the lower right quadrant of the scatter plot analysis, we have identified states with high EV registrations but low adoption rates, marking them as ideal candidates for EV infrastructure spending and consumer rebate initiatives.

| State | Pure EV Registrations (approx.) | Adoption Rate | Priority Reason
|---|---|---|---|
| Florida | 250,000 | 1.4% |Highest EV registrations outside of California with a massive infrastructure gap to the tune of just 1.4% adoption |
| Texas | 230,000 | 0.9% | Just below Florida when it comes to EV registrations and yet an adoption rate of below 1% makes this an untapped reservoir|
| New York | 100,000 | 1.1%  | A dense urban population with a particularly high potential of possible EV growth in metropolitan areas |

Prioritizing these states will maximize the impact of the infrastructure investment and consumer incentive programs.

## Recommendations

Based on the analysis, the following recommendations are made 
for the Transportation Research Group:

**1. Prioritize EV Charging Infrastructure in Florida, Texas and New York**

Expand EV charging network and establish repair and maintenance points at high traffic areas.

**2. Introduce or Expand Consumer EV Incentive Programs**

Establish state-level rebates and tax incentives for EV adoption, modelling the adoption strategies of leaders in the EV space such as California and Washington. 

**3. De-prioritize Alternative Fuel Infrastructure Spending**

- National alternative fuel adoption rate is less than 1%, making increased spending inviable.

- Investment should be de-prioritized at this stage.

- However, alternative fuel adoption should be measured as an ongoing concern.

- Should the adoption rates continue to grow and surpass 20%, an increase in spending would be viable, barring any unforeseen circumstances.


## Limitations

- Data for U.S. Territories & Minor Outlying Islands were not provided.

- Since the data collection timeframe was not included, wider economic trends were not taken into account. 

- Hydrogen had only data collected for California while Methanol had no data at all. This may be indicative of gaps in the data collection process.

-   "Unknown Fuel" was assumed to be Gasoline for the scope of this analysis. A detailed breakdown of this category may cause slight changes to the results.