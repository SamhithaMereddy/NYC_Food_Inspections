# New York City Food Establishment Inspections

## Project Overview

This project focuses on the analysis of food establishment inspection data from three major U.S. cities: Chicago, Dallas, and New York. The goal is to harmonize the data from these cities, develop a dimensional data model, and create insightful business intelligence dashboards using Power BI and Tableau.

## Project Components

### 1. Data Extraction

**Objective**: Collect inspection data from the open data portals of the following cities:

- **Chicago**: [Chicago Open Data Portal](https://data.cityofchicago.org/)
- **Dallas**: [Dallas Open Data Portal](https://data.dallascityhall.com/)
- **New York**: [NYC Open Data Portal](https://opendata.cityofnewyork.us/)

**Files Included**:
- `data/chicago_food_inspections.csv`: Contains inspection data for Chicago.
- `data/dallas_food_inspections.csv`: Contains inspection data for Dallas.
- `data/ny_food_inspections.csv`: Contains inspection data for New York.

### 2. Data Staging

**Objective**: Load the raw data into staging tables to facilitate transformation and analysis.

**Procedure**:
- Create staging tables in your database with the prefix `stg_`. These tables will temporarily hold the raw data.
- Follow the [Staging Guidelines](docs/staging_guidelines.md) to ensure data integrity and consistency during this process.

### 3. Data Profiling

**Objective**: Assess the quality and structure of the data to understand its characteristics and identify any issues.

**Procedure**:
- Use data profiling tools or scripts to analyze the data in the staging tables.
- Document the findings regarding data completeness, consistency, and any anomalies.

### 4. Dimensional Modeling

**Objective**: Design a dimensional data model that organizes the data into dimensions and facts for efficient querying and reporting.

**Procedure**:
- Identify key dimensions (e.g., location, inspection type) and facts (e.g., inspection scores, violations).
- Develop the Dimensional Data Model using [ER/Studio](https://www.idera.com/er-studio-data-architect), which includes creating tables, defining relationships, and ensuring proper indexing.

### 5. Data Integration

**Objective**: Prepare and load the data into the Integration Schema, following the dimensional model.

**Procedure**:
- Develop ETL (Extract, Transform, Load) workflows using [Alteryx](https://www.alteryx.com/).
- The workflows should handle data transformation and loading into the Integration Schema based on the dimensional model.

### 6. Business Intelligence Dashboards

**Objective**: Create interactive dashboards to visualize the inspection data and provide actionable insights.

**Procedure**:
- **Power BI**:
  - Use [Power BI Desktop](https://powerbi.microsoft.com/desktop/) to build dashboards.
  - Publish the dashboards to [Power BI Service](https://app.powerbi.com/) for sharing and collaboration.
- **Tableau**:
  - Use [Tableau Desktop](https://www.tableau.com/products/desktop) to create visualizations.
  - Publish the dashboards to [Tableau Online](https://www.tableau.com/products/tableau-online) for access and sharing.

## Setup Instructions

### Prerequisites

- **Alteryx Designer**: Required for developing ETL workflows.
- **Power BI Desktop**: Required for creating and publishing Power BI reports.
- **Tableau Desktop**: Required for creating and publishing Tableau dashboards.
- **Database**: Set up your database environment and create the staging tables according to the [Staging Guidelines](docs/staging_guidelines.md).

### Steps

1. **Install Required Tools**:
   - Download and install Alteryx Designer, Power BI Desktop, and Tableau Desktop from their respective websites.

2. **Configure Database**:
   - Set up the database environment.
   - Create staging tables with the prefix `stg_` as described in the staging guidelines.

3. **Run ETL Workflows**:
   - Open Alteryx Designer and execute the ETL workflows provided in the `alteryx_workflows` directory.

4. **Create and Publish Dashboards**:
   - Develop Power BI and Tableau dashboards using the provided data and publish them to the respective services.

## Documentation

- [Staging Guidelines](docs/staging_guidelines.md): Guidelines for staging data.
- [Data Model Design](docs/data_model_design.md): Details of the dimensional data model.
- [ETL Workflows](docs/etl_workflows.md): Instructions for using Alteryx workflows.
- [Power BI Dashboards](docs/powerbi_dashboards.md): Guide to creating and publishing Power BI dashboards.
- [Tableau Dashboards](docs/tableau_dashboards.md): Guide to creating and publishing Tableau dashboards.


## License

This project is licensed under the MIT License. 
