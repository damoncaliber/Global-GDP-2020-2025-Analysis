# Global GDP(2020-2025) Analysis

![World Map](https://upload.wikimedia.org/wikipedia/commons/c/cf/A_large_blank_world_map_with_oceans_marked_in_blue.PNG)

# Introduction
What is GDP?
__Gross Domestic Product (GDP)__ is the total monetary value of all goods and services produced within a country’s borders over a specific period, typically measured annually or quarterly. It serves as a primary indicator of a nation’s economic performance and is widely used to compare the relative economic strength of countries. GDP can be calculated using three approaches: the production (or output) approach, which sums the value added at each stage of production; the income approach, which totals all incomes earned by factors of production; and the expenditure approach, which aggregates consumption, investment, government spending, and net exports.

Understanding GDP provides insights into economic growth, living standards, and the health of different sectors within an economy. High GDP growth typically indicates a thriving economy, while stagnant or negative growth may signal recession or economic challenges. GDP can be expressed in nominal terms, which reflects current market prices, or real terms, which adjusts for inflation to allow comparisons over time. Additionally, GDP per capita offers a perspective on individual prosperity by dividing total GDP by the population. For global analyses, GDP is essential in assessing regional contributions, emerging market trends, and shifts in economic rankings, making it a critical metric for policy-making, investment decisions, and development planning.

# Problem Statement

The global economy is dynamic and complex, with countries and regions contributing differently to worldwide production and wealth. Between 2020 and 2025, the world experienced significant economic fluctuations influenced by factors such as pandemic recovery, regional trade shifts, technological advancements, and emerging market growth. Understanding how GDP—one of the most critical measures of economic output—evolves over time is essential for identifying trends in economic power, investment opportunities, and global development patterns.

Despite the abundance of economic data, there remains a need to systematically analyze trends at both global and regional levels, uncover which countries are rising or falling in economic rankings, and highlight disparities between developed and emerging economies. By examining country-level GDP data across years, this project aims to provide actionable insights for policymakers, investors, and researchers, enabling them to make informed decisions based on historical trends, regional contributions, and shifts in economic dominance.

This analysis is motivated by the desire to answer questions such as:

Which regions are driving global GDP growth, and how has their share changed over time?

Are there emerging economies that are gaining prominence in global rankings?

How do economic shocks or recovery periods affect the distribution of wealth across continents?

By tackling these questions, the project not only highlights the current state of global economic balance but also uncovers patterns and trends that can inform future strategies in investment, trade, and development planning.

# Objectives

The main goal of this project is to analyze global GDP trends between 2020 and 2025 to understand how economic output is distributed across countries and regions, and how it evolves over time. Specifically, the project aims to answer the following key questions:

### Global Trends:

How has total global GDP changed from 2020 to 2025?

What are the yearly growth rates, and are there periods of acceleration or slowdown?

### Regional/Continental Contributions:

Which continents contribute the most to global GDP?

How have these shares changed over the five-year period?

### Country-Level Insights:

Which countries contribute the most to global GDP and hold the largest share of economic output?

### Comparative Analysis:

How do developed economies compare to emerging and developing economies in terms of growth and contribution?

Are there noticeable disparities or convergences in continental performance?

# Data Description

The dataset used in this project contains GDP values for 197 countries from 2020 to 2025, providing a comprehensive view of global economic performance. The data was sourced **Kaggle**, ensuring it reflects official and consistent economic statistics.

#### Structure of the dataset:

Columns:

Country – Name of the country.

2020, 2021, 2022, 2023, 2024, 2025 – GDP values in millions of USD for each year.

Continent column (added via mapping) to group countries by region.

Rows: Each row represents a single country’s GDP across the six years.

#### Data characteristics:

Some GDP values are missing for certain countries and years due to incomplete reporting. These missing values were handled carefully during preprocessing.

The data was initially in wide format (one column per year) and reshaped into long format (columns: Country | Year | GDP) to facilitate analysis.

Special cases like __Kosovo__ and __Timor-Leste__ were manually assigned continents because automated mapping tools (pycountry_convert) did not recognize them.

Why this dataset is useful:

It allows for temporal analysis (GDP trends over years) and cross-country comparison.

Enables regional aggregation to study continental contributions to global GDP.

Supports the analysis of rank changes, identifying emerging economies and shifts in global economic power.

# Data Cleaning & Preparation

Before performing any analysis, the raw GDP dataset required cleaning and restructuring to ensure accuracy and consistency. Key steps included:

#### Reshaping the Dataset:

The original dataset was in wide format, with one column per year (2020, 2021, …, 2025).

It was converted into long format using pd.melt(), resulting in three columns: Country | Year | GDP. This makes it easier to analyze trends over time.

#### Handling Missing Values:

Some countries had missing GDP values for certain years.

These were imputed using the mean GDP of the respective continent for that year, maintaining overall data consistency while avoiding bias.

#### Mapping Countries to Continents:

Using the pycountry_convert library, countries were assigned to their respective continents.

Special cases like Kosovo and Timor-Leste were manually assigned, as the library did not recognize them.

#### Data Type Conversion:

The Year column was converted to integers, and GDP to numeric type to facilitate calculations and visualizations.

#### Validation:

Checked for duplicates and outliers to ensure no erroneous data would skew the analysis.

##### Why these steps matter:

Reshaping allows flexible time-series and comparative analysis.

Imputing missing values ensures that trends and regional aggregations are meaningful.

Mapping to continents enables analysis at both country and regional levels, which is essential for understanding global economic contributions.

# Exploratory Data Analysis (EDA)

The EDA phase focuses on understanding global GDP trends, regional contributions, and country-level dynamics from 2020 to 2025. 

### Global Trends:
How has total global GDP changed from 2020 to 2025?

What are the yearly growth rates, and are there periods of acceleration or slowdown?

### Regional Contributions:

Countries were grouped by continent to calculate each region’s share of global GDP.

Donut pie charts and bar plots were used to visualize the contribution of continents like Asia, North America, and Europe.

Insights highlighted that Asia dominated global GDP, followed by North America and Europe, while Africa and Oceania contributed smaller shares.

#### Country-Level Analysis:

Countries were ranked by GDP for 2020 and 2025 to identify top gainers and losers.

Bar charts and tables were used to showcase countries with the largest rank improvements (e.g., Eritrea, Afghanistan) and declines (e.g., Nigeria, Yemen).

### Comparative Insights:

Emerging economies were compared to developed nations to understand shifts in global economic power.

Continental and country-level comparisons highlighted disparities, growth patterns, and potential investment opportunities.








