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
### Category 1:

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 1]


### Category 2:

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 2]


### Category 3:

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 3]


### Category 4:

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 4]



# Recommendations:

Based on the insights and findings above, we would recommend the Fleet Safety and Operations team to consider the following:

Several drivers have risk scores ≥ 9.0, indicating significant safety concerns. Implement targeted coaching and corrective training programs for high-risk drivers (risk ≥ 7.0), 
with particular focus on speeding control and following distance discipline.

The most common events are over-speeding, lane departure, and unsafe following distance. Create specialized training modules and in-cab alerts for these behaviors, reinforcing safe driving habits through real-time feedback and periodic refresher courses.

Ford and Caterpillar have lower associated risk scores and better driver safety metrics. Prioritize these models for future fleet expansion and allocate higher-risk drivers to safer vehicle types where possible.

Risk and efficiency trends vary by driver and truck model. Leverage dashboards and normalized driver risk scores to establish internal scoring policies for rewards, insurance negotiations, and timely interventions.

# Assumptions and Caveats:

Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:

* Assumption 1 (ex: missing country records were for customers based in the US, and were re-coded to be US citizens)
  
* Assumption 1 (ex: data for December 2021 was missing - this was imputed using a combination of historical trends and December 2020 data)
  
* Assumption 1 (ex: because 3% of the refund date column contained non-sensical dates, these were excluded from the analysis)
