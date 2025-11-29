# Datasets for ML Electrical Engineering Course

This directory contains information about datasets used in the course. All datasets are either generated synthetically within the notebooks or can be downloaded from public sources.

## Dataset Overview

### 1. Power System Measurements (Generated)
**Used in:** Module 1 - Data Foundations

**Description:** Synthetic power system sensor data including voltage, current, frequency, and power measurements with realistic noise and data quality issues.

**Generation:** Created programmatically in `Module_01_Data_Foundations/01_Data_Cleaning.ipynb`

**Features:**
- `timestamp`: DateTime (hourly measurements)
- `voltage_kv`: Voltage in kilovolts (kV)
- `current_a`: Current in amperes (A)
- `frequency_hz`: System frequency in hertz (Hz)
- `power_mw`: Power in megawatts (MW)

**Size:** ~1000 records (1 week of hourly data)

---

### 2. Energy Demand Data (For Forecasting Project)
**Used in:** Module 3 - PROJECT: Energy Demand Forecasting

**Option A - Kaggle Dataset (Recommended):**
- **Source:** [Hourly Energy Consumption](https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption)
- **Description:** Real hourly energy consumption data from multiple US regions
- **Download:** Visit the link above and download the dataset
- **Size:** Multiple years of hourly data

**Option B - Generated (Alternative):**
Generated within the project notebook with realistic patterns:
- Daily cycles (higher consumption during business hours)
- Weekly patterns (weekday vs. weekend differences)
- Seasonal variations (summer cooling, winter heating)
- Weather correlation (temperature, humidity)

---

### 3. Power System Fault Data (For Classification Project)
**Used in:** Module 4 - PROJECT: Fault Detection in Power Systems

**Option A - Kaggle Dataset (Recommended):**
- **Source:** [Electrical Fault Detection and Classification](https://www.kaggle.com/datasets/esathyaprakash/electrical-fault-detection-and-classification)
- **Description:** Power system fault data with various fault types
- **Download:** Visit the link above

**Option B - Generated (Alternative):**
Synthetic data generated in the project notebook with:
- Normal operating conditions
- Various fault types (line-to-ground, line-to-line, three-phase)
- Voltage sags, current spikes, frequency deviations
- Realistic fault signatures

**Features:**
- Voltage phase A, B, C
- Current phase A, B, C
- Frequency
- Fault type (label)

**Size:** 5000-10000 records (balanced classes)

---

### 4. Smart Grid Load Profiles (For Deep Learning Project)
**Used in:** Module 5 - PROJECT: Load Classification for Smart Grids

**Generated in notebook** with three load types:

**Residential Loads:**
- Morning and evening peaks
- Lower consumption overnight
- Weekend variations

**Commercial Loads:**
- Business hours (9 AM - 5 PM) peaks
- Minimal consumption overnight
- Lower weekend consumption

**Industrial Loads:**
- Consistent high consumption
- 24/7 operation patterns
- Less daily variation

**Features:**
- Hourly load profile (24 values)
- Day of week
- Month
- Total daily consumption
- Peak demand
- Load factor
- Load type (label)

**Size:** 3000-5000 records

---

### 5. Renewable Energy Data (For Time Series Project)
**Used in:** Module 6 - PROJECT: Renewable Energy Output Prediction

**Option A - Kaggle Datasets (Recommended):**

**Solar Power:**
- **Source:** [Solar Power Generation Data](https://www.kaggle.com/datasets/anikannal/solar-power-generation-data)
- **Description:** Solar panel generation with weather data
- **Features:** Irradiation, temperature, power output

**Wind Power:**
- **Source:** [Wind Power Forecasting](https://www.kaggle.com/datasets/theforcecoder/wind-power-forecasting)
- **Description:** Wind farm data with weather conditions
- **Features:** Wind speed, direction, temperature, power output

**Option B - Generated (Alternative):**
Synthetic renewable energy data with:
- Solar: Diurnal patterns, cloud cover effects, seasonal variation
- Wind: Stochastic wind speed variations, cut-in/cut-out speeds
- Weather: Temperature, irradiance, wind speed correlations

**Features:**
- Timestamp
- Solar irradiance (W/m²) or Wind speed (m/s)
- Temperature (°C)
- Cloud cover (%) or Wind direction (degrees)
- Power output (MW)

**Size:** 2+ years of hourly data

---

## How to Use Datasets

### Method 1: Using Kaggle Datasets (Recommended for Projects)

1. **Create a Kaggle Account:**
   - Visit [kaggle.com](https://www.kaggle.com) and sign up

2. **Download Datasets:**
   - Navigate to the dataset links provided above
   - Click "Download" button
   - Extract the ZIP files

3. **Place in Course Directory:**
   ```
   ML_Electrical_Engineering_Course/
   └── datasets/
       ├── energy_consumption/
       ├── fault_detection/
       ├── solar_power/
       └── wind_power/
   ```

4. **Update Notebook Paths:**
   - Modify file paths in notebooks to point to downloaded data
   - Example: `pd.read_csv('../datasets/energy_consumption/data.csv')`

### Method 2: Using Generated Data (Easier for Beginners)

1. **No Downloads Needed:**
   - All data generation code is included in project notebooks
   - Simply run the data generation cells

2. **Advantages:**
   - No external dependencies
   - Controlled data quality
   - Customizable parameters

3. **Disadvantages:**
   - Not real-world data
   - May not capture all real-world complexities

---

## Data Generation Code Examples

All project notebooks include comprehensive data generation code. Here's what you'll find:

### Energy Demand Generation:
```python
# Creates realistic hourly demand with:
# - Base load component
# - Daily cycles (peak during day)
# - Weekly patterns (weekday vs weekend)
# - Seasonal trends (summer/winter peaks)
# - Random variations (noise)
```

### Fault Detection Data:
```python
# Generates labeled fault data:
# - Normal operation (80% of data)
# - Line-to-ground faults (8%)
# - Line-to-line faults (7%)
# - Three-phase faults (5%)
# Each with realistic voltage/current signatures
```

### Load Profile Generation:
```python
# Creates three distinct load types:
# - Residential: Morning/evening peaks
# - Commercial: Business hours peak
# - Industrial: Flat 24/7 profile
# With realistic variations
```

### Renewable Energy Data:
```python
# Solar: Simulates daily solar curves
# - Peak at solar noon
# - Zero at night
# - Cloud effects (random dips)
# - Seasonal variation
#
# Wind: Simulates stochastic wind
# - Weibull distribution for speed
# - Cut-in/cut-out thresholds
# - Temporal correlation
```

---

## Dataset Quality and Validation

### Quality Checks Performed:
- No missing values in generated data (or controlled missingness)
- Realistic value ranges based on electrical engineering standards
- Temporal consistency (no time gaps in time series)
- Label balance (for classification datasets)
- Physical consistency (power = voltage × current relationships)

### Validation Steps:
1. Statistical summaries (mean, std, min, max)
2. Distribution plots (histograms, box plots)
3. Time series plots (identify patterns)
4. Correlation analysis (check relationships)

---

## Adding Your Own Datasets

To use your own power systems data:

1. **Format Requirements:**
   - CSV format preferred
   - DateTime column for time series
   - Consistent column names
   - No special characters in headers

2. **Place in datasets/ folder:**
   ```
   datasets/
   └── your_dataset/
       ├── data.csv
       └── description.txt
   ```

3. **Update Notebook:**
   - Modify data loading cell
   - Adjust column names if different
   - Verify data types

4. **Data Cleaning:**
   - Use techniques from Module 1
   - Handle missing values appropriately
   - Detect and treat outliers

---

## Support and Resources

### Need Help with Data?
- Check Module 1 notebooks for data handling techniques
- Review example code in project notebooks
- Consult course README.md for setup instructions

### Data Issues?
- Verify file paths are correct
- Check CSV format (comma-separated, UTF-8 encoding)
- Ensure no special characters in data
- Review data types (datetime, float, int)

### Want to Contribute Datasets?
- Submit via GitHub pull request
- Include dataset description
- Provide source/generation method
- Document all features

---

## License and Attribution

- **Generated Data:** Free to use for educational purposes
- **Kaggle Datasets:** Follow individual dataset licenses
- **Real-World Data:** Check with data provider for usage rights

---

**Last Updated:** November 2025
**Maintained by:** BUILD_it & ELEESA
