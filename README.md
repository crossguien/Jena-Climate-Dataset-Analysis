# Jena-Climate-Dataset-Analysis
Comprehensive analysis of Jena, Germany climate data (2009-2016). Performs time-series preprocessing, daily/monthly aggregation, data reshaping, and statistical analysis. Includes temperature trend visualizations (heatmaps, line plots) and extreme weather event analysis. Built with Python, pandas, matplotlib, and seaborn.

## Dataset

**Source:** https://www.kaggle.com/datasets/mnassrib/jena-climate

**Details:**
- **Time Period:** January 2009 - December 2016
- **Frequency:** 10-minute intervals (144 observations per day)
- **Total Records:** 420,000+ observations
- **Variables:** Temperature, Pressure, Humidity, Wind Speed, Dew Point, and more

## Technologies Used

- **Python 3.x**
- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computing
- **matplotlib** - Data visualization
- **seaborn** - Statistical visualization
- **Jupyter Notebook** - Interactive development environment

## Project Structure
├── jena_climate_2009_2016.csv          # Raw dataset

├── Climate_Analysis.ipynb               # Main Jupyter notebook

├── daily_averages.csv                   # Processed daily data

├── monthly_aggregations.csv             # Monthly extreme values

├── daily_averages_long_format.csv       # Reshaped data

├── monthly_temperature_by_year.csv      # Temperature pivot table

├── top_5_windiest_days_all_metrics.csv  # Extreme wind events

├── monthly_temperature_heatmap.png      # Visualization

├── monthly_temperature_trends.png       # Visualization

└── windiest_days_detailed_analysis.png  # Visualization

## Analysis Tasks

### 1. Data Preprocessing
- Converted Date Time strings to datetime objects
- Set Date Time as index for time-series operations
- Created temporal features (Date, Month, Year, Month_Year)
- Verified data types and data completeness

### 2. Daily and Monthly Aggregation
- **Daily Averages:** Temperature, Humidity, Wind Speed (2,921 days)
- **Monthly Extremes:** Maximum Pressure, Minimum Dew Point (96 months)

### 3. Data Reshaping
- Transformed daily averages from wide format to long format
- Converted 2,921 rows × 3 columns → 8,763 rows × 3 columns
- Implemented tidy data principles for flexible analysis

### 4. Monthly Temperature Trends
- Created pivot table: Years (rows) × Months (columns)
- Generated heatmap visualization showing seasonal patterns
- Produced line plot for year-over-year temperature comparison

### 5. Extreme Weather Analysis
- Identified top 5 windiest days
- Analyzed all meteorological conditions during extreme wind events
- Created multi-panel visualization comparing wind, pressure, and temperature

## Key Findings

**Climate Characterization:**
- **Classification:** Temperate continental climate (Cfb/Dfb transition)
- **Mean Temperature:** ~9°C with ~50°C annual range
- **Humidity:** Consistently high (>75%) indicating moist climate
- **Wind:** Generally calm with occasional storm events (3-5× normal speeds)

**Seasonal Patterns:**
- **Winter (Dec-Feb):** Coldest months, high variability
- **Summer (Jun-Aug):** Warmest months, most stable temperatures
- **Spring/Autumn:** Clear transition periods with predictable trends

**Data Quality:**
- Zero missing values across 420,000+ observations
- Consistent 10-minute sampling intervals
- Professional meteorological equipment evident
