# Week-8-Final-Project-Python

### COVID-19 Analysis Report: Focus on Selected Countries and Africa-wide Overview

# 1. Introduction

This report presents an exploratory analysis of COVID-19 trends for eight key countries—South Africa, Kenya, Nigeria, Egypt, Morocco, Russia, China, and India—using global data from the Our World in Data COVID-19 dataset. Additionally, it provides an Africa-wide view of vaccination progress through a visual choropleth map.

# 2. Data Collection & Preparation

The data was sourced from owid-covid-data.csv.
Key steps included:
Checking the dataset: Verified rows, columns, missing values, and data types.
Filtering: Selected the eight focus countries.
Data Cleaning:
Converted the date column to datetime format.
Filled missing values for critical columns (total_cases, new_cases, total_deaths, new_deaths, total_vaccinations) with 0 to ensure completeness in time-series analysis.

# 3. Tech Stack
Python
Pandas (Data wrangling)
Matplotlib & Seaborn (Static plots)
Plotly Express (Interactive map)
Streamlit (Dashboard app)


# 4. Exploratory Data Analysis (EDA)

4.1 Total COVID-19 Cases Over Time
A time-series plot shows the growth of total confirmed COVID-19 cases in each country from the start of the pandemic to the latest available data.

Insights:

India and Russia reported the highest case numbers among the group.
South Africa leads in total cases within the African continent.
4.2 Total COVID-19 Deaths Over Time
A parallel plot tracks cumulative deaths.

Insights:

Again, India and Russia saw the highest death tolls.
South Africa had a noticeably high mortality burden in Africa compared to its peers.
4.3 Daily New Cases
We plotted new daily cases to capture infection waves.

Insights:

All countries experienced distinct surges, reflecting pandemic waves.
Peaks correspond to global pandemic phases, such as the Delta and Omicron waves.
4.4 Death Rate Over Time
The death rate (total deaths divided by total cases) was calculated and plotted.

Insights:

Death rates fluctuated over time, typically decreasing as vaccination and treatments improved.
Egypt and Russia showed relatively higher death rates compared to others.
4.5 Vaccination Progress
a. Total Vaccinations Over Time

This visualization tracks cumulative COVID-19 vaccinations.

Insights:

India and China ramped up vaccinations quickly and at massive scale.
Morocco led early in Africa, later joined by South Africa and Egypt in coverage.
b. People Fully Vaccinated (% of Population)

We examined the percentage of people fully vaccinated.

Insights:

Morocco and China achieved high full-vaccination percentages.
Nigeria and Kenya lagged behind in full coverage.
# 5. Africa-Wide Vaccination Status

A choropleth map was created using Plotly Express to display the latest percentage of fully vaccinated people per country across Africa.

Enhancements Made:

We ensured the data used the most recent available date per country and dropped rows where people_fully_vaccinated_per_hundred was missing, which resolved earlier map display issues.
Key Findings:

Countries like Morocco, Rwanda, and Tunisia displayed high vaccination percentages.
Several other countries remain below 20% full vaccination, highlighting ongoing public health challenges.
# 6. Sample Data Point Explanation

For example, one data point showed:

3.5578e+06

This is scientific notation meaning:

3,557,800 total vaccinations (or similar metric, depending on context).

# 7. How to run it 
How to Run

Clone the repository:
git clone https://github.com/yourusername/covid_dashboard.git
cd covid_dashboard
Install dependencies:
pip install -r requirements.txt
Run the app:
streamlit run app.py
# Data Source

Our World in Data COVID-19 Dataset:
https://github.com/owid/covid-19-data
#  Key Countries Analyzed

South Africa
Kenya
Nigeria
Egypt
Morocco
Russia
China
India
# Author

This dashboard was developed as part of an exploratory data analysis and visualization project to track COVID-19’s impact regionally and globally.

# 8. Conclusion

The analysis shows:

Significant disparities in both infection and vaccination rates across countries.
African countries continue to face challenges in vaccine rollout compared to global peers.
Regular data updates and ongoing monitoring are essential to track progress and inform public health strategies.
Appendix: Technical Highlights

Python Libraries Used:
pandas, matplotlib, seaborn, plotly.express
Key Techniques:
Time-series visualizations
Data cleaning with fillna
Choropleth mapping of geospatial data
