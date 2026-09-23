# London Bike Sharing Analysis

## Interactive Data Analysis with Python and Tableau

This project analyzes **London bike-sharing activity** to identify patterns in bike demand and examine how usage changes across **time, weather conditions, temperature, and wind speed**.

The project combines **Python-based data preparation** with an **interactive Tableau dashboard**, allowing users to explore bike-sharing trends dynamically rather than relying only on static visualizations.

---

## Project Details

- **Data Source:** [London Bike Sharing Dataset - Kaggle](https://www.kaggle.com/datasets/hmavrodiev/london-bike-sharing-dataset)
- **Dataset Size:** 17,414 observations
- **Tools Used:** Python, Pandas, Excel, Tableau
- **Main Analysis Areas:**
  - Bike-sharing trends over time
  - Moving-average analysis
  - Hourly bike-demand patterns
  - Weather conditions
  - Temperature and wind-speed relationships
  - Interactive time-period exploration

---

## Data Preparation

The original dataset was downloaded from Kaggle and processed using Python and Pandas.

The main preprocessing steps included:

- Loading and exploring the dataset
- Reviewing data types and variables
- Renaming columns to improve readability
- Converting season codes into descriptive categories
- Converting weather codes into readable weather conditions
- Preparing the cleaned dataset for Tableau
- Exporting the final dataset to Excel

The weather categories include:

- Clear
- Scattered clouds
- Broken clouds
- Cloudy
- Rain
- Rain with thunderstorm
- Snowfall

The cleaned dataset was exported as:

`london_bikes_final.xlsx`

and subsequently used as the data source for the Tableau dashboard.

---

# Tableau Dashboard

![London Bike Sharing Dashboard](https://github.com/DucTung269/London-Bike-Rides-/blob/main/images/london_bike_dashboard.png?raw=true)

The dashboard provides an interactive overview of London bike-sharing activity.

For the selected period between **01/01/2016 and 27/04/2016**, the dashboard records:

**2,522,108 bike rides**

The dashboard combines a total-rides KPI, a moving-average time-series visualization, and a temperature-versus-wind-speed heatmap.

---

## Interactive Moving Average

The time-series section allows the user to dynamically analyze trends in bike demand.

Users can:

- Select a specific period directly on the timeline
- Change the moving-average time unit between **day, week, and month**
- Change the **moving-average duration / window length**
- Adjust the analyzed date range
- Compare short-term and longer-term bike-demand trends

For example, selecting:

`Day + 5`

displays a **5-day moving average**.

Changing the period and duration allows the same dashboard to be used for both short-term and longer-term trend analysis.

---

## Interactive Temperature and Wind-Speed Analysis

![Interactive Dashboard Example](https://github.com/DucTung269/London-Bike-Rides-/blob/main/images/interactive_hover_weather_hour.png?raw=true)

The heatmap analyzes bike rides across combinations of:

- **Real temperature**
- **Wind speed**

Darker cells represent combinations associated with larger numbers of bike rides.

The visualization is also interactive.

When the user **points to or hovers over a heatmap cell**, Tableau displays additional information related to that specific temperature and wind-speed combination.

The additional information includes:

- Bike rides by **weather condition**
- Bike rides by **hour of the day**

This allows the user to move from a general overview to a more detailed analysis without leaving the dashboard.

---

## Interactive Drill-Down

![Temperature and Wind-Speed Interaction](https://github.com/DucTung269/London-Bike-Rides-/blob/main/images/interactive_hover_temperature_wind.png?raw=true)

For example, after selecting a particular combination of temperature and wind speed, the dashboard automatically updates the additional visualizations.

The user can therefore explore questions such as:

- Which weather conditions were associated with rides under these conditions?
- At what hours were most bikes used?
- Does the usage pattern correspond to morning or evening commuting?
- How does bike demand change when temperature or wind conditions change?

This creates an interactive **overview → selection → detailed analysis** workflow.

---

# Bike Demand by Hour

![Bike Demand by Hour](https://github.com/DucTung269/London-Bike-Rides-/blob/main/images/hourly_analysis.png?raw=true)

The hourly analysis shows a clear daily usage pattern.

The highest bike activity occurs around:

- **08:00** - approximately 308,277 rides
- **17:00** - approximately 264,562 rides
- **18:00** - approximately 239,810 rides

Bike usage is much lower during the night and increases rapidly during the morning.

The two major peaks around **08:00** and **17:00-18:00** suggest that London bike sharing is strongly associated with **commuting behavior**, with riders using bikes during morning and evening rush hours.

---

# Bike Demand by Weather

![Bike Rides by Weather](https://github.com/DucTung269/London-Bike-Rides-/blob/main/images/weather_analysis.png?raw=true)

The weather analysis shows how the total number of rides is distributed across different weather conditions during the selected period.

The largest numbers of rides occurred under:

- **Scattered clouds:** 798,175 rides
- **Clear weather:** 776,154 rides
- **Broken clouds:** 593,382 rides
- **Rain:** 284,742 rides

Considerably fewer rides occurred during more severe weather conditions such as thunderstorms and snowfall.

These values describe the **distribution of total rides across observed weather conditions**. They should not by themselves be interpreted as causal effects of weather, since different weather conditions may occur with different frequencies.

---

# Key Insights

### 1. Strong Commuting Pattern

Bike usage shows clear morning and evening peaks, particularly around **08:00 and 17:00-18:00**.

This suggests that bike sharing plays an important role in daily commuting.

### 2. Bike Demand Changes Strongly Over Time

The moving-average visualization reveals substantial changes in bike demand throughout the year.

Using different moving-average periods allows short-term fluctuations to be separated from longer-term trends.

### 3. Weather and Environmental Conditions Matter

Bike usage varies substantially across weather categories and combinations of temperature and wind speed.

Clear, scattered-cloud, and broken-cloud conditions account for a large proportion of observed rides, while severe weather conditions are associated with much lower total activity.

### 4. Interactive Analysis Provides Deeper Insights

Instead of displaying only static charts, the dashboard allows users to:

- Select specific periods
- Change moving-average settings
- Adjust the analysis window
- Hover over temperature and wind-speed combinations
- View detailed weather information
- View hourly ride distributions

This makes it possible to investigate bike-sharing behavior at different levels of detail within a single dashboard.

---

# Project Workflow

```text
Kaggle Dataset
      |
      v
Python / Pandas
      |
      |-- Data Exploration
      |-- Column Renaming
      |-- Weather Mapping
      |-- Season Mapping
      |-- Data Preparation
      |
      v
Cleaned Excel Dataset
      |
      v
Tableau
      |
      |-- Total Rides KPI
      |-- Moving Average
      |-- Time Selection
      |-- Temperature × Wind Heatmap
      |-- Weather Analysis
      |-- Hourly Analysis
      |
      v
Interactive Dashboard
