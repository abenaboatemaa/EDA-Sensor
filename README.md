[README.md](https://github.com/user-attachments/files/23658292/README.md)

# Exploratory Data Analysis of Sensor Data

This repository contains the results of an Exploratory Data Analysis (EDA) performed on sensor data, including temperature, humidity, light, pH, and electrical conductivity (EC). The analysis covers data extraction, cleaning, trend visualization, correlation analysis, identification of day-night cycles, basic statistics computation, and a summary of key findings.

## Project Structure

```
.
├── EDA_Sensor_Data.ipynb
├── README.md
├── 28667981.zip
├── sensor_data/
│   ├── sensor_data_2025-03-01.csv
│   ├── ...
└── plots/
    ├── trends_over_time.png
    ├── correlation_heatmap.png
    ├── pairwise_scatter_plots.png
    ├── light_day_night_cycles.png
    └── temp_humidity_trends.png
```

## Data Analysis Key Findings

*   The dataset comprises 120,960 entries across 6 columns (`timestamp`, `temperature`, `humidity`, `light`, `pH`, `electrical_conductivity`) with no missing values, and all data types are appropriate for analysis.
*   **Sensor Reading Statistics**:
    *   **Temperature** ranged from 20.0°C to 25.0°C with a mean of 22.50°C and a variance of 2.08.
    *   **Humidity** ranged from 40.0% to 60.0% with a mean of 50.03% and a variance of 33.26.
    *   **Light** intensity showed significant variation, ranging from 100.0 Lux to 999.99 Lux, with a mean of 549.10 Lux and a high variance of 67457.73, indicative of day-night cycles.
    *   **pH** values were between 6.0 and 8.0, averaging 7.00, with a variance of 0.33.
    *   **Electrical Conductivity** spanned from 0.5 to 2.0, with a mean of 1.25 and a variance of 0.19.
*   **Trends and Cycles**: Clear day-night cycles are evident in the light intensity data, showing regular increases and decreases corresponding to daytime and nighttime. Temperature and humidity also exhibit cyclical trends over time.
*   **Correlations**: The correlation analysis revealed very weak linear relationships between `temperature`, `humidity`, and `light`. For instance, the correlation between temperature and humidity was 0.003655, temperature and light was -0.000423, and humidity and light was -0.001196.
*   **Inverse Relationships**: While the correlation coefficients were low, visual inspection of the temperature and humidity trends over time suggests a general inverse relationship; as one tends to rise, the other often falls, although this relationship is not strongly linear or consistently proportional.

## Insights or Next Steps

*   The very weak linear correlations between environmental factors like temperature, humidity, and light suggest that their interactions might be non-linear, delayed, or influenced by other unmeasured variables. Further investigation using non-linear correlation methods or time-series analysis could reveal more complex relationships.
*   Given the strong day-night cycles observed in light data, incorporating a 'time of day' or 'day/night' feature could enhance predictive models or further analysis requiring an understanding of diurnal patterns for all sensor readings.
## Visualizations

### Trends over Time (Temperature, Humidity, Light)
![Trends Over Time](plots/trends_over_time.png)

### Correlation Matrix Heatmap
![Correlation Heatmap](plots/correlation_heatmap.png)

### Pairwise Scatter Plots
![Pairwise Scatter Plots](plots/pairwise_scatter_plots.png)

### Light Intensity Over Time (Day-Night Cycles)
![Light Day-Night Cycles](plots/light_day_night_cycles.png)

### Temperature and Humidity Over Time
![Temperature and Humidity Trends](plots/temp_humidity_trends.png)
