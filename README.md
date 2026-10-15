# Global Economic Outlook Dashboard | Power BI

**Exploring 20 Years of Global Economic Trends Across 196 Countries**

An interactive Power BI project analysing global economic indicators from 2001 to 2020, transforming a complex dataset into an accessible dashboard for exploring economic performance, government finances, employment, inflation, and international trade.

## Project Overview

The Global Economic Outlook Dashboard was developed using Microsoft Power BI to explore how economic indicators have changed across **196 countries over a 20-year period (2001–2020)**.

# Dashsboard Overview
![Dashboard]
The original dataset contains 44 economic indicators covering areas such as Gross Domestic Product (GDP), GDP per capita, population, unemployment, inflation, government revenue and expenditure, national savings, public debt, and international trade.

To keep the dashboard focused and easy to navigate, I selected the indicators most relevant to the project's objectives and developed an interactive, single-page dashboard that allows users to examine country-level economic performance and trends over time.

The project demonstrates my ability to prepare data, handle missing values, develop calculations, build interactive visualizations, and communicate analytical findings through business intelligence tools.

## Dashboard Preview

![Global Economic Outlook Power BI Dashboard](images/global-economic-outlook-dashboard.png)

*Add a screenshot of your completed Power BI dashboard to the `images` folder using the filename shown above.*

## Project Objectives

The main objectives of this project were to:

- Explore economic performance across 196 countries from 2001 to 2020.
- Identify and investigate missing values across the dataset.
- Clean and transform selected economic indicators using Power Query.
- Select relevant indicators for focused and meaningful visualization.
- Track changes in GDP, GDP per capita, inflation, and unemployment over time.
- Examine government revenue, expenditure, debt, savings, and net lending or borrowing.
- Explore changes in import and export volumes.
- Develop an interactive dashboard with country and year filters.
- Present high-level economic metrics alongside detailed country-level data.
- Identify limitations that could affect the accuracy and interpretation of aggregated results.

## Tools and Technologies

| Tool | Application |
|---|---|
| Microsoft Power BI | Dashboard development and interactive data visualization |
| Power Query | Data cleaning, transformation, and missing-value handling |
| DAX | Measures and calculations for dashboard metrics |
| Power BI Data Model | Organizing the data used by dashboard visuals |
| Interactive slicers | Filtering economic indicators by country and year |
| Time-series charts | Exploring economic trends from 2001 to 2020 |

## Dataset Overview

The dataset contains economic information for **196 countries and 44 indicators**, covering the period from 2001 to 2020.

The indicators cover several major areas of economic performance.

### 1. Economic Growth

- Gross Domestic Product (GDP)
- GDP per capita
- Total investment as a percentage of GDP
- Gross national savings as a percentage of GDP

### 2. Employment and Prices

- Unemployment rate as a percentage of the labour force
- Inflation rate and changes in prices

### 3. Government Finance

- General government revenue in national currency
- Government revenue as a percentage of GDP
- General government expenditure as a percentage of GDP
- Government gross debt in national currency
- Net lending or borrowing

### 4. International Trade

- Percentage change in import volumes
- Percentage change in export volumes

The dashboard uses a selected subset of these indicators to provide a clear overview of economic trends without overcrowding the visual interface.

## Data Preparation and Cleaning

During the initial exploration, I identified that approximately **85% of the indicators contained at least one missing value** in one or more records.

This made data cleaning an important part of the project.

Using Power Query in Power BI, I:

- Identified missing values across the selected indicators.
- Reviewed the nature of the indicators before deciding how to handle missing cells.
- Replaced missing values with zero where considered appropriate for the indicator.
- Calculated mean values and used them to fill selected missing observations.
- Prepared the selected indicators for analysis and visualization.
- Organized the data to support country-level and year-level exploration.

The cleaning process helped prepare the dataset for dashboard development. However, replacing missing values with zero or the mean can affect economic trends, so these decisions should be reviewed against the meaning of each indicator before using the dashboard for formal economic analysis.

## Dashboard Design and Visualizations

The dashboard combines summary cards, interactive slicers, time-series charts, and tables to support both high-level exploration and detailed country-level analysis.

### 1. KPI Cards

Visual cards display selected summary metrics, including:

- Population
- General government revenue

These cards provide quick access to key figures and respond to the selected country and year filters.

### 2. Interactive Slicers

Country and year slicers allow users to filter the dashboard dynamically.

Users can select a specific country and year to explore its economic profile or examine a longer period to understand historical changes.

### 3. Time-Series Charts

Line charts display economic indicators over time, helping users examine changes and identify patterns across the 2001–2020 period.

The indicators visualized include:

- GDP and GDP per capita
- Inflation and unemployment rates
- General government revenue
- Government net lending or borrowing
- Government expenditure and gross debt
- Gross national savings
- Changes in import and export volumes

These visualizations make it easier to follow the direction of economic indicators over time for a selected country.

### 4. Country-Level Data Tables

Tables provide a structured view of selected economic indicators for individual countries.

They complement the charts by displaying precise values that users can compare across indicators and years.

## DAX Measures

I used DAX to create measures for aggregating population and government revenue.

**Total Government Revenue**

```dax
Total Government Revenue =
SUM('Data csv'[General government revenue,National currency])
```

**Total Population**

```dax
Total Population =
SUM('Data csv'[Population,Persons])
```

These measures were used in visual cards to display summary values according to the current filter context.

For percentage-based indicators, such as inflation and unemployment, the aggregation method must be selected carefully. Summing percentages across multiple countries can produce misleading results, so these measures should be evaluated for the intended analytical context.

## Key Findings and Insights

The Global Economic Outlook Dashboard provides an interactive view of economic indicators across 196 countries from 2001 to 2020. The analysis focuses on government finances, economic growth, inflation, unemployment, and international trade.

The following findings are based on the trends visible in the Power BI dashboard.

### 1. Government Revenue Trends

The government revenue visualization shows a noticeable upward trend in the later years, particularly from approximately 2014 to 2020.

**Key insight:** Government revenue values changed substantially over the period, with a sharper increase toward the end of the displayed timeline.

**Analytical implication:** Further analysis is needed to determine whether this pattern reflects changes in revenue collection, inflation, currency valuation, or other economic factors.

### 2. GDP and GDP per Capita Trends

The GDP and GDP per capita visualization shows changes in economic performance over time. The displayed GDP per capita series rises during the early years, declines around 2009, and subsequently recovers, with further fluctuations toward 2020.

**Key insight:** The trend was not consistently upward; periods of growth were followed by declines and recovery.

**Analytical implication:** Comparing annual growth rates across countries could help identify differences in economic performance and periods of greater volatility.

### 3. Government Financial Indicators

The dashboard brings together government revenue, net lending or borrowing, expenditure, and other fiscal indicators.

**Key insight:** The displayed financial indicators follow different patterns over time, highlighting the importance of examining each measure individually rather than assuming that all government financial variables move together.

**Analytical implication:** Comparing revenue and expenditure alongside net lending or borrowing could support further investigation into changes in government fiscal positions.

### 4. International Trade Trends

The imports and exports visualization contains a pronounced spike around 2018–2019, followed by a return toward the previous level.

**Key insight:** This unusual movement stands out from the relatively stable pattern visible in earlier years.

**Analytical implication:** The underlying country-level records should be investigated to determine whether the spike represents a genuine change in trade activity, an outlier, or a data-quality or aggregation issue.

### 5. Inflation and Unemployment Analysis

The dashboard includes a time-series visualization for inflation and unemployment.

**Key insight:** The visualization provides a way to explore changes in these indicators over time and investigate how their patterns differ.

**Analytical implication:** Inflation and unemployment should be treated as rates rather than automatically summed across countries. Country-level comparisons or appropriately weighted regional measures would provide a more meaningful basis for analysis.

### 6. Interactive Country-Level Exploration

The dashboard includes country and year slicers that allow users to examine selected economic indicators dynamically.

**Key insight:** Users can move from a broad overview to a country-specific economic profile without navigating multiple static reports.

**Analytical implication:** This functionality supports exploratory analysis, historical trend monitoring, and the identification of economic patterns that warrant further investigation.

## Summary of Findings

| Economic area | Key observation |
|---|---|
| Government revenue | Noticeable upward movement in the later years |
| GDP per capita | Early growth, a decline around 2009, and subsequent recovery |
| Government finances | Different indicators display different trajectories |
| International trade | A pronounced spike around 2018–2019 requires investigation |
| Inflation and unemployment | Time-series exploration is available, with careful treatment of rate aggregation required |
| Interactive reporting | Country and year filters support detailed economic exploration |

## Data Quality and Interpretation

During the initial exploration, approximately 85% of the dataset's indicators were found to contain at least one missing value.

Power Query was used to identify missing values and apply selected replacement methods, including zero replacement and mean imputation, depending on the indicator.

The analysis also identified an important limitation: summing percentage-based indicators across multiple countries can produce misleading results.

Consequently, the dashboard's trends should be interpreted alongside the underlying data, the selected country and year filters, and the aggregation method used for each measure.

## Overall Conclusion

This project demonstrates how Microsoft Power BI can transform a complex economic dataset into an interactive dashboard for exploring global economic trends.

The analysis highlights changes in government revenue, fluctuations in GDP per capita, different patterns across government financial indicators, and an unusual movement in the trade visualization that warrants further investigation.

Beyond visualization, the project demonstrates the importance of data preparation, appropriate calculations, and critical interpretation when working with large economic datasets.

**The main outcome is an interactive analytical tool that helps users explore economic indicators, identify patterns, and formulate questions for deeper economic investigation.**

**Country-level economic profiles**

Users can select a country and examine its GDP, population, unemployment, inflation, government revenue, expenditure, and trade indicators.

**Long-term economic trends**

Time-series charts allow users to explore changes in economic indicators over the 20-year period.

**Government financial patterns**

Users can investigate how revenue, expenditure, debt, and net lending or borrowing have changed over time.

**Employment and inflation trends**

The dashboard allows users to examine unemployment and inflation patterns for selected countries and years.

**International trade movements**

Import and export volume changes can be explored to understand how trade indicators fluctuate over time.

These are analytical capabilities of the dashboard. Specific claims about which countries performed best or worst should be established through a documented analysis of the underlying data.

## Dashboard Interactivity

One of the key strengths of this project is the ability to explore economic data dynamically.

- Selecting a country updates the dashboard to display its relevant economic indicators.
- Selecting a specific year narrows the view to that period.
- Selecting a country without restricting the year allows users to examine its trends across the available period.
- Tables complement the charts by providing more detailed numerical information.

This approach enables users to move from a broad overview to a more focused examination of individual countries and economic indicators.

## Limitations and Data Considerations

Although the dashboard provides an accessible way to explore global economic indicators, several limitations should be considered.

### Missing-Value Treatment

The original dataset contained substantial missingness. Replacing missing values with zero or mean values may introduce bias or alter trends if the replacement is not appropriate for the indicator.

### Aggregation of Economic Indicators

Some indicators are percentages or rates and should not automatically be summed across countries. For example, a combined sum of national inflation rates does not represent a meaningful global inflation rate.

The dashboard's percentage-based indicators should therefore be interpreted at the country level unless a suitable aggregation method has been defined.

### Indicator Selection

The dataset contains 44 indicators, but the dashboard uses a selected subset to maintain clarity and usability. Some potentially useful variables are therefore not included in the visual interface.

### Interpretation of Trends

Changes in economic indicators show patterns over time but do not, by themselves, explain the causes of those changes. Additional economic analysis and contextual information would be needed to establish causal explanations.

## Skills Demonstrated

This project demonstrates practical skills in:

- Power BI dashboard development
- Power Query data transformation
- Missing-value identification and treatment
- DAX measure creation
- Interactive data visualization
- Time-series analysis
- Economic indicator analysis
- KPI development
- Dashboard layout and user experience
- Data aggregation and filter context
- Analytical interpretation and documentation
- Identifying data-quality and reporting limitations

## Potential Future Improvements

Future versions of the project could include:

- A dedicated data-quality report showing missingness by indicator and country.
- A comparison page for selected countries or regional economic groups.
- Measures designed specifically for percentage-based indicators.
- A clearer distinction between sums, averages, and weighted economic rates.
- Regional comparisons of GDP growth, unemployment, and inflation.
- Additional drill-through pages for country-level economic profiles.
- More robust missing-data methods based on indicator definitions and time-series patterns.
- A dedicated methodology page documenting data sources, transformations, and calculation assumptions.

## Repository Structure

```text
global-economic-outlook-powerbi/
│
├── README.md
├── images/
│   └── global-economic-outlook-dashboard.png
├── dashboard/
│   └── global-economic-outlook.pbix
└── reports/
    └── global-economic-outlook-report.pdf
```

## How to Explore the Project

1. Clone or download this repository.
2. Download the Power BI `.pbix` file
3. Open it using Microsoft Power BI Desktop.
4. Use the country and year slicers to explore the available economic indicators.
5. Review the time-series charts, KPI cards, and tables to investigate country-level patterns.

## Conclusion

The Global Economic Outlook Dashboard demonstrates how Power BI can transform a complex, multi-country economic dataset into an interactive analytical tool.

By combining Power Query, DAX measures, time-series visualizations, KPI cards, and interactive filtering, I developed a dashboard that supports the exploration of economic performance across 196 countries over two decades.

The project also strengthened my understanding of data preparation, indicator selection, aggregation, and the importance of presenting economic data accurately.

My goal is to use data analytics and business intelligence to make complex information easier to understand and support more informed, evidence-based decisions.

---

**Author:** Bolade Oloruntayo  
**Project Type:** Business Intelligence & Data Visualization  
**Tool:** Microsoft Power BI  
**Focus Areas:** Data Analytics | Economic Trends | Dashboard Development | Power Query | DAX
