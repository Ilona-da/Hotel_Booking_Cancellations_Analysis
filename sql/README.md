# Hotel Cancellations Trends Analysis

## Data Preparation - cleaning and transformation (SQL)  

The dataset contained around 36,000 hotel reservation records in raw CSV format.
It was imported into Microsoft SQL Server and cleaned step by step to prepare a consistent analytical dataset.

The main goal was to perform as much data preparation directly in SQL as possible, simulating a real-world data engineering workflow before moving to Power BI. 

Key cleaning actions:

Standardized data types and date formats for consistency.
Removed invalid or incomplete records (e.g., zero-night stays, missing guest counts).
Normalized categorical values (e.g., room types, market segments, meal plans).
Verified logical consistency between fields (e.g., bookings vs. cancellations vs. stays).
Checked for NULL values - surprisingly, none were present in the dataset.

The cleaned dataset was stored in a new table called reservations_cleaned, which served as the foundation for further analysis and visualization in Power BI.

### Goal
To ensure clean, analysis-ready data and simulate a scalable approach where SQL handles the heavy lifting, leaving Power BI to focus on analysis and storytelling.

## Exploratory Data Analysis (SQL)  

After cleaning, the analysis continued in SQL using structured queries designed to explore patterns and relationships before visualization.
The EDA was divided into logical analytical themes, each focused on understanding different aspects of the data.

Each step focused on a different theme:

Key analysis areas:

**Time trends & seasonality** - booking and arrival patterns, monthly and weekly seasonality.
**Customer segmentation** - market segments (Online, Offline, Corporate, Aviation) and their booking/cancellation profiles.
**Guest behavior** - returning vs. first-time guests, special requests, average length of stay.
**Revenue & pricing** - price levels by room type, meal plan, and season.
**Operational metrics** – parking use, guest composition, presence of children.
**Lead time patterns** - binning lead times to evaluate cancellation risks.
**Cancellation risks** - identifying which combinations of time, guest, and price factors correlate with higher cancellation rates.
**Feature engineering** - creating helper columns (e.g., lead time bins, stay categories) to support Power BI visuals and insights.

### Outcome
This phase provided not only analytical inputs for Power BI but also early, data-driven hypotheses - e.g., that long lead times and first-time guests are strong predictors of cancellations.

## Repository Structure
- `data/` - folder containing raw dataset:
  - `raw_data.csv` - source data file
- `sql/` - folder containing SQL scripts:
  - `data_cleaning.sql` - SQL script for data cleaning
  - `exploratory_data_analysis.sql` - SQL queries for exploratory data analysis
- `powerbi/` - folder with Power BI file:
  - `report.pbix` - fully interactive report file
  - `preview/` - image preview of each report page
- `README.md` - project documentation

