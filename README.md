# NYC Flight Delays Analysis — R

## Project Overview
Analyzed flight delay data for all flights departing from New York City airports (JFK, LGA, EWR) in 2013 using the `nycflights13` dataset. The goal was to uncover patterns in flight delays, identify factors influencing delays, and provide actionable insights for travelers and airlines.

## Key Skills
- Data cleaning and preprocessing in R
- Exploratory Data Analysis (EDA) with `dplyr` and `ggplot2`
- Hypothesis testing (ANOVA)
- Correlation analysis of numeric variables
- Data visualization: bar charts, scatterplots, boxplots
- Insight interpretation and reporting

## Dataset
- Source: [`nycflights13` R package](https://cran.r-project.org/web/packages/nycflights13/index.html)
- Number of flights: 336,776
- Key variables:
  - `dep_delay`: Departure delay (minutes)
  - `arr_delay`: Arrival delay (minutes)
  - `carrier`: Airline
  - `origin`: Airport of departure (JFK, LGA, EWR)
  - `distance`: Flight distance (miles)

## Analysis Highlights
1. **Airline Delays**  
   - Average departure delays vary by airline, visualized with bar charts.

2. **Monthly Trends**  
   - Summer months show slightly higher delays; visualized with line plots.

3. **Arrival vs Departure Delay**  
   - Strong positive correlation; scatterplots show flights that depart late also tend to arrive late.

4. **Airport Comparison**  
   - Boxplots reveal differences in departure delays across JFK, LGA, and EWR. ANOVA confirms the differences are statistically significant.

5. **Correlation Analysis**  
   - Departure and arrival delays are strongly correlated. Distance and air time show weak correlation with delays.

## Insights
- Departure delays are the strongest predictor of arrival delays.  
- JFK has the highest median delays, LGA has the lowest.  
- Most flights have small delays (0–20 minutes), but extreme outliers exist (some flights delayed up to 500–1000 minutes).  
- Seasonal trends indicate slightly longer delays during summer months.  
- Airlines vary in punctuality, with some carriers consistently performing better.

## How to Run
1. Clone the repository.
2. Open `NYC_Flight_Delays.qmd` in RStudio (Quarto).
3. Install required packages:

```r
install.packages(c("tidyverse", "nycflights13", "GGally", "lubridate"))
