# 🌐 Global Health Dataset Project

### 📝 Project Summary
This Tableau project visualises global health trends and disparities across countries, continents, genders and time. The dashboard allows the user to understand historical key health trends and disparities across different countries and continents. The aim was to provide an interactive tool for public health analysis, to highlight historical global patterns.

🔗 [View dashboard on Tableau Public](https://public.tableau.com/app/profile/liannebaff/viz/GlobalHealthDashboard_17615617876560/GlobalHealthInsights)

### 🎯 Key Skills Demonstrated:
`TABLEAU DESKTOP` &nbsp; `TABLEAU PUBLIC` &nbsp; `CALCULATED FIELDS` &nbsp; `TREND ANALYSIS` &nbsp; `DATABASE DESIGN` &nbsp; `FILTERS & DASHBOARD INTERACTIVITY` &nbsp; `COMPARATIVE ANALYSIS` &nbsp; `DATA VISUALISATION`

### 🗂️ Dataset Overview
The dataset is from **Gapminder Health** and comprises global health indicators including blood pressure, cholesterol and cancer rates (lung, liver and stomach) by country from 1990 to 2008. The dataset also includes country population and population growth (%).

---
### 🧩 Data Preparation
- No data cleaning required. Most of the preparation, such as, defining data types and creating calculated fields was completed in Tableau.
- The dataset was already structured in a suitable format for analysis. A snapshot of the original dataset is included below:

<img width="1899" height="340" alt="image" src="https://github.com/user-attachments/assets/12ba004d-fe62-4bc0-93f1-d49eb5dd2dac" /> <br>


- Created the following calculated fields:
  - **Total Cancer Cases:** combined the total cases of all the types of cancer within the dataset to create a unified count per country.
    - `Total Cancer Cases = [Liver Cancer]+[Stomach Cancer]+[Lung Cancer]`
  - **Cancer Case Rate:** calculated cases per population to allow a meaningful comparison across differently sized countries.
    - `Cancer Case Rate = ([Lung Cancer]+[Liver Cancer]+[Stomach Cancer])/[Population]`
- Filters were also applied in order to filter by:
  - Country
  - Continent
  - Year range
  - Top 5 countries (using Top N filter)
- Sorting also used to sort the continents by life expectancy

---
### 🎨 Dashboard Creation
This section describes the technical work carried out inside Tableau to create the dashboard:

#### 🔎 Filters
- Filters applied to visualisations to allow users to filter by country and continent and choose a specific year range.
- The filters were applied to all relevant worksheets to illustrate a unified story across the dashboard and also improve interactivity.  

#### 🖼️ Design & Layout
- Colour used in order to more easily differentiate countries and continents. Colours for continents kept consistent across dashboard.
- Titles added to each worksheet for clarity.
- Clean card-based layout used to allow quick scanning.

---
### 📊 Dashboard Overview
All worksheet combined into a single interactive dashboard. The dashboard included filter controls for exploratory analysis

**1) Life Expectancy Trend**
- Multi-line chart visualising changes in life expectancy between 1990-2008 for each country.
- VThe chart has been set to "Use as Filter" and applied to all data using the same source, so selecting a country updates the entire dashboard.

**2) Life Expectancy by Continent**
- A bar chart showing the average life expectancy for each continent, sorted in descending order.
- The chart has been set to "Use as Filter" and applied to all data using the same source, so selecting a continent updates the entire dashboard.

**3) Life Expectancy vs. BMI**
- Scatter plot illustrating the relationship between BMI and life expectancy.
- Each point indicates a country and each colour indicates a continent.
- Allows users to spot patterns in life expectancy and BMI.

**4) BMI vs. Cholesterol**
- Scatter plot illustrating the relationship between BMI and cholesterol.
- Each point indicates a country and each colour indicates a continent.
- Allows users to spot patterns in BMI and cholesterol.

**5) Population by Gender**
- Pie chart showing the male and female distributions.
- Visualisation has been used as a filter and applied to all data using the same source, allowing users to focus on gender-specific health patterns.
- Clearly demonstrates whether there is a demographic imbalance or parity.

[![Global Health Insights Dashboard](https://github.com/user-attachments/assets/58b456e5-055a-442c-87a0-793abd91344d)](https://public.tableau.com/app/profile/liannebaff/viz/GlobalHealthDataset/GlobalHealthInsightsDashboard)

🔗 [View dashboard on Tableau Public](https://public.tableau.com/app/profile/liannebaff/viz/GlobalHealthDashboard_17615617876560/GlobalHealthInsights)

---
  ### 🪞 Insights & Reflections
- There is a variation in life expectancy across continents, Europe has the highest life expectancy (76.07) whereas Africa had the lowest (55.91). The Americas (72.20), Asia (69.57) and Oceania (69.90) had similar life expectancies, however Africa's life expectancy was significantly lower the other continents.
- Countries with a higher average BMI do not always have lower life expectancy, indicating complex relationships between lifestyle health and environment.
- Countries with a higher cholesterol do not always have a higher average BMI which suggests there are other factors at play that cause increased cholesterol.
- A limitation of the dataset is that it does not include detailed socioeconmic variables or demographic breakdowns (e.g., age, household income), limiting deeper analysis.
- This is a historical dataset and so cannot be used infer global health insights for the present day, however a possible next step would be to use current data and assess whether global health as improved or worsened in recent years.
- Calculated metrics like cancer case rates or total cancer cases rely on aggregated data, which may mask local variability.
- Overall, the project demonstrated how interactive dashboards can help communicate complex global health trends in an accessible way.
  
---
 ### 📁 Files in This Repository  
- **[GapminderHealth.xlsx](GapminderHealth.xlsx)**
  
  **Worksheet(s):**
  - **Gapminder Health:** dataset showing key health indicators, population and population growth per country over the years 1990 - 2008. <br>
  

### 📋 Dataset Structure
Each metric is reported separately for each gender within each country at each time point.

| Column Name           | Description                                                                |
|-----------------------|----------------------------------------------------------------------------|
| Continent             | Continent Name                                                             |
| Country               | Country name                                                               |
| Year                  | Year of observation                                                        |                                                 
| Life Expectancy       | Average life expectancy for the country                                    |
| Gender                | Population gender (male/female)                                            |
| BMI                   | Average Body Mass Index (BMI) for that gender in that country              |
| Blood Pressure        | Average blood pressure for that gender in the country                      |
| Cholesterol           | Average cholesterol levels for that gender in the country                  |
| Lung Cancer           | Total reported lung cancer cases for that gender in the country            |                                                 
| Liver Cancer          | Total reported liver cancer cases for that gender in the country           |
| Stomach Cancer        | Total reported stomach cancer cases for that gender in the country         |
| Population            | Total population of that gender in the country                             |
| Population Growth     | Population growth for that gender in the country                           |






