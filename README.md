# israel_palestine_conflict_data_analysis
# Cleaned Data for Israel-Palestine Conflict Analysis

This repository contains a cleaned dataset derived from the original `israel_palestine_conflict.csv` file. The cleaning process involved several steps to prepare the data for analysis and visualization.

## Data Cleaning and Preparation Steps:

1.  **Loading Data:** The original CSV file was loaded into a pandas DataFrame.
2.  **Numeric Column Cleaning:** Columns containing injury and fatality counts (`Palestinians Injuries`, `Israelis Injuries`, `Palestinians Killed`, `Israelis Killed`) were cleaned by:
    * Removing commas from string representations of numbers.
    * Converting the values to numeric data types.
    * Handling non-convertible values by setting them to `NaN`.
3.  **Missing Value Handling:** Missing values (`NaN`) in the 'Palestinians Injuries' and 'Israelis Injuries' columns were filled with 0.
4.  **Date Feature Engineering:**
    * The 'Month' column was standardized.
    * A new 'date' column was created by combining the 'Month' and 'Year' columns into a datetime object.
    * The DataFrame was sorted chronologically based on the 'date' column.
    * The original 'Month' and 'Year' columns were dropped.
5.  **Data Aggregation:** Total injuries and fatalities for both Palestinians and Israelis were calculated. Yearly totals were also computed.
6.  **Data Visualization:** Several visualizations were generated to explore the data:
    * Line plots showing monthly trends of injuries and fatalities for both groups over time.
    * Bar charts comparing total yearly injuries and fatalities for both groups.
    * Pie charts illustrating the overall proportion of total injuries and fatalities between Palestinians and Israelis.
7.  **Final Data Formatting:** The 'date' column was reformatted to 'YYYY-MM-DD' string format.
8.  **Saving Cleaned Data:** The processed DataFrame was saved to a new CSV file named `cleaned_israel_palestine_conflict.csv`.

## Contents:

* `cleaned_israel_palestine_conflict.csv`: The cleaned dataset ready for analysis.

## How to Use This Data:

This cleaned dataset can be used for various analytical purposes, including:

* Analyzing trends in injuries and fatalities over time.
* Comparing the impact of the conflict on Palestinians and Israelis.
* Identifying periods of increased conflict intensity.
* Further statistical analysis and modeling.

## Libraries Used:

* pandas
* numpy (implicitly)
* matplotlib.pyplot

## Note:

This dataset represents a specific collection of reported incidents and may not capture the full complexity and nuances of the conflict. Always consider the source and potential biases when interpreting the data.
