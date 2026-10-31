# 🏎️ Formula 1 Analytics Dashboard | Power BI

<div align="center">

[![Formula 1](https://img.shields.io/badge/Formula_1-Analytics-E10600?style=for-the-badge&logo=formula1&logoColor=white)](https://www.formula1.com/)
[![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
![Power Query](https://img.shields.io/badge/Power_Query-Data_Transformation-217346?style=for-the-badge)
![DAX](https://img.shields.io/badge/DAX-Data_Analytics-4472C4?style=for-the-badge)
[![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/binayas/f1-dataset)
![CSV](https://img.shields.io/badge/Data-CSV-217346?style=for-the-badge)

</div>


## Exploring Formula 1 History Through Data --- 1950 to 2026

An interactive, multi-page **Formula 1 analytics report built with Microsoft Power BI**, designed to explore driver performance, constructor results, race outcomes, qualifying, lap times, pit stops, reliability, circuits, sprint race, and championship history.

The project transforms a historical racing dataset into a connected analytical experience using Power Query, dimensional data modeling, advanced DAX, coverage-aware slicers, drill-through navigation, and a consistent report design.

  ### Project principle:
the dashboard does not treat every metric as available for every season. Slicers selections are filtered according to the data coverage relevant to the analysis, helping users focus on periods supported by the underlying records.

## Table of Contents

 - Project Overview
 - Project Demo
 - Visual Preview
 - Project Objectives
 - Data Source and Coverage
 - Data Preparation
 - Data Model
 - Calculated Columns
 - Supporting Tables
 - DAX Measures
 - Dashboard Pages
 - Design and Navigation
 - Visual Preview
 - Challenges and Solutions
 - Validation and Optimization
 - Key Analytical Questions
 - Limitations
 - How to Use
 - Skills Demonstrated
 - Buit With

## 🔎 Project Overview

Formula 1 data spans many eras, with substantial differences in the amount and type of information recorded. Race results and Championship standings extend much further back than detailed lap timing, pit stop and sprint data.

This project brings those datasets together in one Power BI report while respecting those differences in coverage. Users can move from historical overviews to focused investigations of drivers, constructors, races, and specific performance metrics.

## 🎬 Project Demo

[![Watch Dashboard Demo](images/landingPage.png)](https://youtu.be/CvIGxFecIu0)

*Click the image to watch the full dashboard demonstration.*

## 🖼️ Visual Preview

### Landing Page
![Landing Page](images/landingPage.png)

### Overview
![Overview Dashboard](images/Overview.png)

### Driver Analysis
![Driver Analysis](images/DriverAnlaysis.png)

### Driver Performance
![Driver Performance](images/DriverPerformance.png)

### Driver Comparisons
![Head to Head I](images/Head-to-Head-I.png)

![Head to Head II](images/Head-to-Head-II.png)

### Teams Performance
![Teams Performance](images/TeamPerformance.png)

### Team Results
![Team Results](images/TeamResults.png)

### Team Car
![Team Car](images/teamCar.png)

### Races Analysis
![Races Analysis](images/RacesAnalysis.png)

### Qualifying Analysis
![Qualifying Analysis](images/QualifyingAnalysis.png)

### Lap Analysis
![Lap Analysis](images/LapAnalysis.png)

### Pit Stops Analysis
![Pit Stops Analysis](images/pitStops.png)

### Circuits Analysis
![Circuits Analysis](images/CircuitsAnalysis.png)

### DNF Analysis
![DNF Analysis](images/DNFAnalysis.png)

### Race Conditions
![Race Conditions I](images/Race-Conditions-I.png)

![Race Conditions II](images/Race-Conditions-II.png)

### Sprint Analysis
![Sprint Analysis](images/SprintAnalysis.png)

### Championship History
![Championship Hsitory](images/championshipAnalysis.png)


### Project Highlights

- **Historical scope:** dataset coverage from 1950 through 2026, subject to the records actually available in each source table.
- **13 source CSV tables:** integrated into a shared analytical model.
- **18 report pages:** overview, performance analysis, head-to-head comparisons, drill-through details, relibility, and championships.
- **Coverage-aware slicers:** season and related selections are filtered to match the supported coverage of the analysis.
- **Advanced DAX:** reusable measures, calculated columns, helper tables, dynamic comparisons, and race-relative benchmark.
- **Interactive exploration:** navigation, synced slicers, conditional formatting, and drill-through.
- **Consistent design:** A dark theme, Formula 1-inspired colors, standardized layouts, and reusable measures.

## 🎯 Project Objectives

1. Analyze Formula 1 history across seasons, decades, circuits, drivers, and constructors.
2. Evaluate driver performance through wins, podiums, poles, points, and finishing positions.
3. Compare two drivers independently using career statistics and shared-race results.
4. Investigate constructor performance, championship progression, and driver contributions.
5. Analyze qualifying sessions and the relationship between starting grid and finishing position.
6. Explore lap times, pace, consistency, and laps led where data is available.
7. Evaluate pit stop duration and patterns across supported seasons.
8. Investigate retirements, recorded failure causes, and high-attrition races.
9. Explore circuits histories, sprint races, championship margins, and historical records.
10. Build a maintainable Power BI model with reusable measures and transparent analytical assumptions.

## 📚 Data Source and Coverage

**Dataset:** Complete Formula 1 Dataset (1950-2026) - [Dataset on Kaggle](https://www.kaggle.com/datasets/binayas/f1-dataset)


The project uses only the supplied Kaggle dataset. No external APIs, databases, or additional web data were added.

The dataset combines historical records from the Ergast archive with more recent data associated with the Jolpica F1 API. A source columns identifies the origin of rows where provided.

It contains multiple CSV files covering different aspects of the sport, including races, drivers, constructors, results, standings, qualifying, lap times, pit stops, and sprint races.

### Source Files

The project works with the following 13 CSV files:

| File | Description |
| ------ | ----------- |
| circuits.csv | Circuit information and locations |
| constructor_standings.csv | Constructor championship standings |
| constructors.csv | Constructor and team information |
| driver_standings.csv | Driver championship standings |
| drivers.csv | Driver information |
| lap_times.csv | Individual lap-time records |
| pit_stops.csv | Pit-stop records and durations |
| qualifying.csv | Qualifying results and session times |
| races.csv | Race schedules, dates, rounds, and circuits |
| results.csv | Race results, positions, points, and related statistics |
| seasons.csv | Season information |
| sprint_results.csv | Sprint race results |
| status.csv | Race result status descriptions |

The availability and completeness of individual tables vary by season and by the type of racing data recorded.


### Historical Data Coverage

| Data Category | Coverage Begins | Main Analytical Use |
| ----------- | ----------------- | ---------------------------- |
| Race results | 1950 | Wins, points, grid positions, finishing positions |
| Driver standings | 1950 | Driver championship performance |
| Constructor standings | 1958 | Constructor championship performance |
| Qualifying positions | 1994 | Grid positions and qualifying results |
| Qualifying session times (Q1, Q2, Q3) | 2006 | Detailed qualifying session analysis |
| Fastest-lap records | 2004 | Fastest lap and lap-performance statistics |
| Lap-time records | 2011 | Individual lap times and race pace |
| Pit-stop records | 2012 | Pit-stop durations and operational performance |
| Sprint race results | 2021 | Sprint results and sprint-specific performance |

***Coverage dates are based on the dataset's intended historical scope and should be verified against the actual CSV contents before interpreting individual records.***

### Coverage-Aware Slicers

The dashboard uses slicers to filter data by dimensions such as season, race, driver, constructor, and other relevant categories.

For data categories with limited historical coverage, the filtering experience is designed to help users select periods supported by the relevant data.

For example:

- Lap-time analysis focuses on seasons for which lap-time records are available.
- Pit-stop analysis focuses on seasons with pit-stop records.
- Sprint analysis focuses on seasons in which sprint results are represented.
- Qualifying-session analysis distinguishes between qualifying positions and detailed session times.

This approach helps reduce misleading comparisons between periods with different levels of data availability.

**Important:** Filtering by supported seasons does not guarantee that every race, driver, or record within a selected season has complete data. Coverage-aware slicers should therefore be interpreted alongside the actual completeness of each source table.

## 🧹 Data Preparation and Transformation

Data preparation was performed in **Power Query** to improve data quality, consistency and compatibility with the Power BI data model.

### Key Transformation Steps

- Imported the CSV source files into Power BI.
- Reviewed table structures, column names, and data types.
- Corrected data types for dates, numeric values, identifiers, positions, and time-related fields.
- Handled missing values where appropriate for the analytical context.
- Reviewed duplicate records and data consistency.
- Prepared race dates and season-related fields for time-based analysis.
- Transformed qualifying-session times into suitable formats for analysis.
- Prepared lap-time and pit-stop duration fields for numerical calculations.
- Ensured that key used in table relationships had compatible data types.
- Reviewed data coverage to support meaningful filtering and comparisons.

### Time Data Preparation

Formula 1 datasets contain different time representations, including:

- Race dates and scheduled times.
- Qualifying-session times.
- Individual lap times.
- Pit-stop durations.

These values require appropriate data types and transformations before they can be used reliably in calculations and visualizations.

Time-related transformations were applied where necessary to support duration analysis, comparisons, and performance metrics.

## 🧩 Data Model

A structured data model was developed to connect the different Formula 1 datasets and support analysis across multiple dimensions.

The project uses a **multi-fact dimensional data model** that integrates multiple Formula 1 datasets with different levels of granularity.

Several fact tables share common dimensions, including Drivers, Constructors, Races, and Status, allowing analysis across different aspects of Formula 1 while maintaining appropriate filtering behavior.

Relationships are designed using active one-to-many, single-direction filtering where applicable, avoiding unnecessary fact-to-fact relationships.

### Main Tables

- **Races:** Season, round, date, and circuit information.
- **Drivers:** Driver identity and related attributes.
- **Constructors:** Constructor and team information.
- **Circuits:** Circuit details and geographical information.
- **Results:** Race-level driver results and performance statistics.
- **Driver Standings:** Championship positions and points.
- **Qualifying:** Grid positions and qualifying-session results.
- **Lap Times:** Lap-level timing records.
- **Pit Stops:** Pit-stop timing and duration records.
- **Sprint Results:** Sprint race performance.

### Modeling Considerations

The datasets have different levels of granularity.

For example:

- A race-results table contains driver results for individual races.
- A lap-times table contains multiple lap records per driver and race.
- A pit-stop table can contain multiple pit-stops per driver and race.
- Standings tables represent championship positions at particular points in a season.

These differences must be considered when creating relationships and aggregating measures.

### Handling Constructor Analysis

Constructor-level analysis involving lap times and pit stops requires careful handling because the detailed timing tables may not contain the same constructor information as the main race-results table.

The model uses the relevant relationships and, where required, DAX techniques such as *TREATAS* to transfer filter context between related tables.

This supports constructor-level analysis without assuming that every table can be joined directly at the same granularity.

## 🧮 Calculated Columns

Calculated columns were created row-level classifications, categorization, or reusable attributes were required.

These columns support filtering, grouping, and analysis across the report.

### Examples of the Calculated Categories

#### Race and result classifcation

- Race status and result categories.
- Finishing-position classifications.
- Winner and podium indicators.
- Points-related classifications.

#### Driver and Championship analysis

- Driver-related analytical attributes.
- Championship and position indicators.
- Categories supporting driver comparisons.

#### Lap-time and pit-stop analysis

- Time-related classifications.
- Duration and performance categories where appropriate.
- Fields supporting lap-time and pit-stop comparisons.

#### Constructor analysis

- Constructor-related classifications.
- Team result indicators.
- Attributes supporting constructor-level reporting.

The specific calculated columns depend on the field available in the source data and the analytical requirements of each report page.

## 🗃️ Supporting Tables

Additional tables were created to support the report's analytical structure and interactive features.

| Table | Purpose |
| ------- | -------- |
| _Measures | Centralized storage for DAX measures |
| Driver A | Driver selection for the first side of a comparison |
| Driver B | Driver selection for the second side of a comparison |
| Stats | Supporting statistics or analytical parameters |
| Metrics | Metric selection or supporting analytical logic |
| Duel | Supporting logic for driver head-to-head analysis |
| Nationality Groups | Grouping nationalities into broader categories |

### Disconnected Tables

Tables such as Driver A and Driver B can be used as disconnected selector tables.

They allow users to select two drivers independently, without one selection automatically restricting the other through a direct relationship.

DAX measures then retrieve the selected drivers and calculate the corresponding statistics.

This approach supports flexible comparisons across drivers, seasons, races, and performance indicators.

## 📐 DAX Measures

DAX was used to create reusable measures for the dashboard's KPIs, rankings, comparisons, and analytical calculations.

Measures are organized to make the report easier to maintain and extend.

### 1. Race Performance

Examples include:

- Total races
- Total race entries
- Race wins
- Podium finishes
- Points scored
- Average finishing position
- Best finishing position
- Retirements and non-finishes
- Finishing rate

### 2. Driver Analysis

Examples include:

- Total wins by driver
- Driver podiums
- Driver championship points
- Driver ranking
- Average driver performance
- Performance across selected seasons
- Driver comparison metrics

### 3. Constructor Analysis

Examples include:

- Constructor wins
- Constructor podiums
- Constructor points
- Constructor championship positions
- Constructor rankings
- Team performance across seasons
- Constructor-level race statistics

### 4. Championship Analysis

Example include:

- Championship standings
- Driver championship rankings
- Constructor championship rankings
- Season-level comparisons
- Championship-winning indicators
- Points-based comparisons

### 5. Qualifying Analysis

Examples include:

- Average qualifying position
- Best qualifying position
- Pole-position statistics
- Qualifying performance comparisons
- Qualifying-session time analysis where data is available

### 6. Lap-Time Analysis

Examples include:

- Average lap time
- Fastest recorded lap time
- Lap-time comparisons
- Driver pace analysis
- Constructor-level lap-time comparisons where supported by the model

### 7. Pit-Stop Analysis

Examples include:

- Total pit stops
- Average pit-stop duration
- Fastest pit stops
- Pit-stop comparisons
- Driver and constructor pit-stop analysis

### 8. Sprint Race Analysis

Examples include:

- Sprint race results
- Sprint wins
- Sprint podiums
- Sprint points
- Driver and constructor sprint comparisons

### 9. Head-to-Head Comparison

The driver comparison functionality supports selecting two drivers independently and comparing their performance using relevant statistics.

Depending on the selected metric and available data, the comparison can include:

- Race wins
- Podium finishes
- Championship points
- Average finishing positions
- Qualifying performance
- Other driver performance indicators

### DAX Techniques

The project applies DAX concepts such as:

- CALCULATE
- FILTER
- ALL and ALLSELECTED
- SELECTEDVALUE
- DIVIDE
- COUNTROWS
- DISTINCTCOUNT
- SUMX
- AVERAGEX
- RANKX
- SWITCH
- IF
- COALESCE
- Time-intelligence and date-filtering pattern where appropriate
- Filter-context manipulation
- Disconnected slicer logic
- TREATAS for transferring filter context

## 📊 Dashboard Pages

The Power BI report contains **18 analytical pages,** each designed to investigate a different aspect of Formula 1.

The following list describes the report's intended page coverage.
| No. | Page | Main Focus |
| ----- | ----- | ----- |
| 1 | Overview | High-level Formula 1 statistics and historical performance indicators, and an overall view of the sport |
| 2 | Driver | Historical driver statistics, achievements, rankings, and career performance |
| 3 | Driver Performance | Detailed analysis of driver results, wins, podiums, points, and performance trends across seasons |
| 4 | Head-to-Head Comparison I | Interactive comparison of two selected drivers using key performance indicators |
| 5 | Head-to-Head Comparison II | More detailed driver comparisons across race results, qualifying, and other available performance statistics |
| 6 | Teams Performance | Historical constructor performance, achievements, wins, podiums, and championship statistics |
| 7 | Team Results | Detailed constructor race results, points, finishing positions, and performance across seasons |
| 8 | Team Car | Drill-through analysis providing a more focused view of a selected team's car-related race performance using available dataset attributes |
| 9 | Races Analysis | Historical race analysis, race statistics, results, and trends across seasons |
| 10 | Qualifying Analysis | Qualifying performance, grid positions, and qualifying results |
| 11 | Lap Analysis | Lap-time analysis, driver pace comparisons, and lap-level performance patterns |
| 12 | Pit Stop Analysis | Pit-stop statistics, stop durations, and comparisons of pit-stop performance |
| 13 | Circuits Analysis | Circuit-level analysis, race history, and performance statistics across different Formula 1 venues |
| 14 | DNF Analysis | Analysis of Did Not Finish (DNF) results, retirement frequency, and recorded retirement causes |
| 15 | Race Conditions I | Analysis of race-condition-related information and available historical race-result patterns |
| 16 | Race Conditions II | Further analysis of race conditions and their relationship with race outcomes using available dataset fields |
| 17 | Sprint Analysis | Sprint race results, driver performance, constructor performance, and sprint statistics since their introduction |
| 18 | Championship Analysis | Historical driver and constructor championship results, standings, titles, and championship trends |

### Interactive Features

The report is designed to support interactive exploration through:

- Season and race filtering
- Driver and constructor selection
- Metric-specific filtering
- Coverage-aware slicers for data categories with different historical ranges.
- Driver A versus Driver B comparisons.
- Cross-filtering between compatible visualizations.
- Navigation between report pages.

The behavior of each slicer depends on its configuration and the relationships or DAX logic used by the relevant visualizations.

## 🎨 Design and Navigation

The dashboard uses a consistent visual structure to make complex historical data easier to explore.

### Design Principles

- Consistent formatting across report pages.
- Clear separation between KPIs, charts, and detailed analysis.
- Appropriate visualizations for different data types.
- Consistent use of titles, labels, and analytical categories.
- Interactive filters that support focused analysis.
- Navigation elements to move between related reports pages.
- Attention to readability when comparing drivers, constructors, and seasons.

### Visualization Types

Depending on analytical requirements, the report uses visualizations such as:

- KPI cards
- Bar and column charts
- Line Charts
- Tables and matrices
- Ranking visuals
- Comparative charts
- Time-based trend charts
- Slicers and interactive selectors

The choice of visualization depends on the metric, comparison, and level of detail being analyzed.

## 🛠️ Challenges and Solutions

### 1. Different Historical Coverage

**Challenge:** Not all Formula 1 statistics are available from the beginning of the dataset.

**Solution:** Data coverage was considered when designing filters and analytical pages. Coverage-aware slicers help users focus on periods supported by the relevant data category.

### 2. Different Level of Granularity

**Challenge:** Race results, lap times, pit stops, and championship standings represent different level of details.

**Solution:** The data model and DAX calculations account for differences in granularity to reduce misleading aggregations.

### 3. Cross-Table Filtering

**Challenge:** Some analytical questions require transferring filters between tables that do not share a simple direct relationship.

**Solution:** Appropriate data modeling and DAX techniques, including TREATAS where needed, support selected cross-table analyses.

### 4. Driver and Constructor Comparisons

**Challenge:** Comparing drivers or teams across different seasons can be complicated by changing rules, scoring systems, and available records.

**Solution:** Interactive comparisons and reusable measures provide a consistent framework for exploring available statistics while preserving the selected filter context.

### 5. Report Usability

**Challenge:** A report with +15 pages can become difficult to navigate.

**Solution:** Consistent page design, navigation, slicers, and clearly structured analytical sections help users move between topics.

## Validation and Optimization

Data Validation and report testing are important because historical racing datasets may contain missing records, inconsistent values, and different levels of detail.

### Validation Activities

- Reviewed table schemas and data types.
- Checked key columns used in relationships.
- Verified that measures respond to relevant filetrs.
- Reviewed totals and aggregations at appropriate levels.
- Tested driver and constructor selections.
- Checked coverage-aware filtering for relevant analytical pages.
- Reviewed comparisons across seasons and races.

### Optimization Considerations

- Centralized reusable measures in the **_Measures** table.
- Used an organized data model to support filtering.
- Used appropriate data types for time and numerical fields.
- Considered the impact of relationships and filter context on measure behavior.
- Designed pages around specific analytical questions rather that displaying unrelated visuals together.

## 🔎 Key Analytical Questions

The dashboard is designed to help explore questions such as:

### Drivers

- Which drivers have achieved the most race wins?
- Which drivers have the most podium finishes?
- How has driver performance changed over time?
- How do two selected driver compare in wins, points, and finishing positions?
- Which drivers have achieved the strongest qualifying results?

### Constructors

- Which constructors have achieved the most wins and championship points?
- How has team performance changed across different eras?
- Which constructors have consistently performed well?
- How do constructor results compare across seasons?

### Races

- Which circuits have hosted races across the longest historical periods?
- How have race outcomes changed over time?
- What trends appear in finishing positions and race results?
- How do qualifying positions relate to race outcomes?

### Lap Times and Pit Stops

- How do recorded lap times compare between drivers?
- Which drivers or teams have strong lap-time performance in the available records?
- How do pit-stop durations vary?
- How does pit-stop performance differ across available seasons?

### Championships and Historical Trends

- Which drivers and constructors have won championships?
- How have championship standings evolved?
- How has the sport changed across different periods?
- Which statistics can be compared reliably given the available data?

These questions provide a starting point for exploration rather than a claim that every question has a single definitive answer.

## ⚠️ Limitations

Several considerations are important when interpreting the dashboard:

- **Uneven historical coverage:*** Some datasets begin decades after the first Formula 1 season.
- **Incomplete records:** A season may be supported while individual records within that season are still missing.
- **Changing regulations:** Points systems, qualifying formats, and race procedures have changed over time.
- **Different data granularity:** Race-level and lap-level data should not be aggregated without considering their underlying grain.
- **Historical comparability:** Raw totals may favor drivers or teams with longer careers or more race opportunities.
- **Source dependency:** The report depends on the accuracy and completeness of the source dataset.
- **Current-season completeness:** The latest season may contain partial or evolving data depending on the dataset's update status.

For these reasons, historical comparisons should consider the relevant season, the metric being analyzed, and the availability of the underlying records.

## 🚀 How to Use

### Requirements

- Microsoft Power BI Desktop.
- The Formula 1 CSV dataset from Kaggle.
- The project .pbix file

### Steps

1. Clone or download this repository
2. Download the dataset from Kaggle
3. Place the CSV files in the appropriate local data folder
4. Open the Power BI .pbix file
5. If necessary, update the data-source paths in Power Query to match your local files.
6. Refresh the dataset
7. Explore the report using its navigation, slicers, and interactive visuals.

**Note:** The exact setup steps depends on how the .pbix file and source data are organized in the repository.

## 💡 Skills Demonstrated

This project demonstrates practical experience with:

### Data Analytics

- Exploratory data analysis
- Historical trend analysis
- Performance measurement
- Comparative analysis
- KPI development
- Data quality assessment

### Power BI

- Interactive dashboard development
- Report design and navigation
- Data modeling
- Relationship and filter context
- Slicers and cross-filtering
- KPI cards and analytical visualizations

### Power Query

- CSV data ingestion
- Data cleaning and transformation
- Data type management
- Time-related data preparation
- Handling missing and inconsistent values

### DAX

- Calculated columns and measures
- Filter-context manipulation
- Ranking and comparison calculations
- Disconnected selector tables
- Reusable analytical logic
- Cross-table filter transfer

### Data Modeling

- Multi-fact-dimensional modeling
- Fact and dimension table design
- Relationship and filter-context management
- Granularity awareness
- Cross-table analytical modeling
- Historical data coverage considerations


## 👨‍💻 Built With

- **Microsoft Power BI:** Dashboard development and visualization
- **Power Query:** Data cleaning and transformation
- **DAX:** Calculated columns, measures, and analytical logic
- **CSV Datasets:** Structured historical Formula 1 data
