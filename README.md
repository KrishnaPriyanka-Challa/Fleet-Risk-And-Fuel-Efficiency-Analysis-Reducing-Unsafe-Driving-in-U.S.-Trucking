# Project Background
Az National Trucking (ANT), headquartered in California, is a national trucking corporation that provides long-haul trucking services for a variety of general, non-specialized cargo types. The company’s operations span across the western United States, with the exception of hazardous materials (HAZMAT).

With a large fleet and wide operational footprint, ANT faces ongoing challenges in ensuring driver compliance and managing operational efficiency. Non-compliance with safe driving practices — such as speeding, unsafe following, and lane departures — can increase insurance risks, operational costs, and overall safety concerns.

This project leverages ANT’s fleet and driver data to identify critical insights that can reduce risk, improve fuel efficiency, and enhance fleet management decision-making.

Insights and recommendations are provided on the following key areas:

- **Geographic Risk Analysis:** Identifying regions and routes where most abnormal or high-risk driving events occur.
- **Mileage vs. Risk Correlation:** Evaluating whether higher mileage reduces or increases driver risk.
- **Fleet Fuel Efficiency & Utilization:** Analyzing which truck models are both fuel-efficient and better utilized.
- **Risk-Contributing Driving Behaviors:** Determining which abnormal driving events most impact driver risk scores.
- **Truck Models & Risk Association:** Assessing which truck models are more often linked with higher driver risk.

The SQL queries used to inspect and clean the data for this analysis can be found here [link].

Targed SQL queries regarding various business questions can be found here [link].

An interactive PowerBI dashboard used to report and explore sales trends can be found here [link].



# Data Structure & Initial Checks

The company's main database structure, as seen below, consists of six tables: geolocation,  risk_factor, trucks_mg, truck_mileage, avg_mileage, driver_mileage. 

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8833e14d-d6cf-4b6a-b239-19bc0833487c" />




# Executive Summary

### Overview of Findings

The analysis shows that most high-risk drivers accumulate elevated scores due to lane departures, unsafe following distance, and over-speeding. It also highlights that a small subset of drivers is responsible for a disproportionate share of safety incidents. At the equipment level, Ford and Caterpillar models show lower associated risk scores and stronger safety performance, making them safer options for wider utilization across the fleet.

<img width="1183" height="737" alt="image" src="https://github.com/user-attachments/assets/c8ee976c-821c-4314-895e-ac42b5456e36" />



# Insights Deep Dive

### Geographic Risk Analysis:

* Most abnormal driving events cluster in Downtown Santa Rosa, Downtown Willits, and Highway 18 near Victorville, showing these corridors are hotspots for unsafe driving.

* These incidents are not evenly spread, a few high-density areas account for a large share of risky behavior, suggesting route-specific monitoring could quickly reduce exposure.

<p align="center">
  <img width="600" height="800" alt="image" src="https://github.com/user-attachments/assets/28edd031-cb51-4e05-922c-8ec60e2e6a2f" />
</p>


### Mileage vs. Risk Correlation:

* Mileage alone does not explain risk, drivers with both high and low mileage show widely different risk scores.

* A handful of drivers (A73, A35, A50) have scores ≥ 9.0, showing that risk is driven more by behavior than distance, making targeted interventions more effective than mileage caps.

<p align="center">
  <img width="500" height="600" alt="image" src="https://github.com/user-attachments/assets/0cbaa0d1-5208-4c54-8498-56ec3a2edbca" />
</p>


### Fleet Fuel Efficiency & Utilization:

* **Ford** stands out as the best-performing model, it is both fuel-efficient and widely used.

* Caterpillar, Peterbilt, and Volvo are heavily used but less efficient, raising long-term cost concerns.

* Navistar, Hino, Kenworth, and Crane are efficient but underutilized, suggesting the fleet isn’t fully capturing their potential.

<img width="500" height="600" alt="image" src="https://github.com/user-attachments/assets/48064deb-f8ef-4162-b097-ca96124bfe13" />     <img width="400" height="200" alt="image" src="https://github.com/user-attachments/assets/6b19508e-6671-4d28-ab94-7769879f5e2b" />


### Risk-Contributing Driving Behaviors:

* The biggest contributors to driver risk are over-speeding, lane departure, and unsafe following distance.

* High-risk drivers repeat these behaviors at much higher rates, with A73, A35, and A50 showing persistent issues that require focused retraining.

<p align="center">
  <img width="800" height="1000" alt="image" src="https://github.com/user-attachments/assets/02c1c8ce-f3ea-4b24-be1a-d3b8e794e751" />
</p>

### Truck Models & Risk Association:

* Oshkosh and Crane show the highest average risk but are used by fewer drivers, so more data is needed before drawing firm conclusions.

* Ford and Caterpillar consistently show lower risk across many drivers, making them safer allocations.

* Volvo, Kenworth, and Navistar combine low risk with solid utilization, making them strong candidates for future fleet expansion.

<p align="center">
  <img width="500" height="600" alt="image" src="https://github.com/user-attachments/assets/9bd87e82-bddb-4899-95ee-65b6f983c0ed" />
</p>

# Recommendations:

Based on the insights and findings above, we would recommend the Fleet Safety and Operations team to consider the following:

* Several drivers have risk scores ≥ 9.0, indicating significant safety concerns. Implement targeted coaching and corrective training programs for high-risk drivers (risk ≥ 7.0), with particular focus on speeding control and following distance discipline.

* The most common events are over-speeding, lane departure, and unsafe following distance. Create specialized training modules and in-cab alerts for these behaviors, reinforcing safe driving habits through real-time feedback and periodic refresher courses.

* Ford and Caterpillar have lower associated risk scores and better driver safety metrics. Prioritize these models for future fleet expansion and allocate higher-risk drivers to safer vehicle types where possible.

* Risk and efficiency trends vary by driver and truck model. Leverage dashboards and normalized driver risk scores to establish internal scoring policies for rewards, insurance negotiations, and timely interventions.

# Assumptions and Caveats:

Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:

* Assumption 1 (ex: missing country records were for customers based in the US, and were re-coded to be US citizens)
  
* Assumption 1 (ex: data for December 2021 was missing - this was imputed using a combination of historical trends and December 2020 data)
  
* Assumption 1 (ex: because 3% of the refund date column contained non-sensical dates, these were excluded from the analysis)
