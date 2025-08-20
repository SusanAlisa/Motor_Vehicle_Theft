# Motor_Vehicle_Theft

## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Data Cleaning/Preparation](#data-cleaning--preparation)
- [Exploratory Data Analysis Performed](#exploratory-data-analysis-performed)
- [Data Analysis](#data-analysis)
- [Results/Findings](#results--findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)

### Project Overview
This project explores motor vehicle theft trends in New Zealand to uncover patterns, identify high-risk locations, and provide insights that can guide crime prevention strategies and policy decisions.

[Dashboard](dashboard-stolen-vehicle)

<img width="718" height="360" alt="Dashboard stolen vehicle" src="https://github.com/user-attachments/assets/e4a7c54b-9a9d-4f17-a55c-c1ce228ba03c" />

### Data Sources
Motor Vehicle Theft CSV Dataset Folder "Motor + Vehicle + Theft +CSV"– containing detailed records of stolen vehicles across New Zealand.

Supporting files include:

- stolen_vehicles.csv

- make_details.csv

- locations.csv

### Tools Used
- Excel – for data cleaning, pivot analysis, and dashboard visualization
- Power Query – to merge multiple sheets, remove duplicates, and format data
- Pivot Tables & Charts – to explore trends and summarize findings

### Data Cleaning / Preparation

- Merged all datasets into one master sheet using Power Query
- Checked for and handled missing or blank values
- Removed duplicates and standardized formats (e.g., vehicle IDs, dates, colors)
- Created a clean, analysis-ready dataset

### Exploratory Data Analysis Performed

- Top 5 High-Theft Locations: Identified and compared theft frequency by city/region
- Yearly Theft Trends: Tracked how thefts increased/decreased over time
- Vehicle Type & Color: Found the most targeted vehicle models and colors
- Theft Frequency by Time & Day: Highlighted peak days and times thefts occur
- Interactive Dashboard: Used slicers (Year, Location, Vehicle Type, Color) to drill down into theft trends

### Data Analysis

Since the dataset is split across multiple sheets, the following formulas were used to merge information into a single analysis sheet: 

 #### a. VLOOKUP to Get Make Name 

Used in stolen_vehicles sheet to fetch vehicle make details: 

```
=VLOOKUP(C2, make_details!A:B, 2, FALSE)

```

C2 = Make_ID 

Searches in Make_Details sheet (Column A:B) 

Returns Make_Name from Column 2


 ####  b. VLOOKUP to Get Location Name 

```

=VLOOKUP(E2, locations!A:B, 2, FALSE)

```

E2 = Location_ID 

Searches in Locations sheet (Column A:B) 

Returns Location_Name from Column 2 

### Results / Findings

1. Top 5 High-Theft Locations: They include: Auckland (1,626), Canterbury (660), Bay of Plenty (442), Wellington (417), and Waikato (269)
2. Total number of vehicles stolen - 4,527
3. Most stolen vehicle type: Station wagon.
4. Highest theft period: December 2021 & March 2022.

### Recommendations
- For Law Enforcement:
  - Increase patrols in high-theft locations.
  - Implement surveillance during peak theft hours.
- For Vehicle Owners:
  - Use tracking devices.
  - Park in secure areas.
- For Policymakers:
  - Stricter vehicle theft laws.
  - Public awareness campaigns

### Limitations
While this project provides useful insights into motor vehicle theft patterns, the dataset has limitations including missing values, duplicate records, absence of recovery data, and limited geographic/time detail. These constraints mean the analysis is primarily descriptive, and further insights would require more complete, granular, and contextual data.
💻
📊


  
