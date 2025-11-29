# Machine Learning for Electrical Engineering: Power Systems Applications

A comprehensive, hands-on Python course designed specifically for electrical engineering students to master machine learning techniques applied to power systems challenges.

## Course Overview

This course bridges the gap between machine learning theory and practical electrical engineering applications. Students will learn essential ML techniques through four complete real-world projects focused on power systems, smart grids, and renewable energy.

### What Makes This Course Unique?

- **Power Systems Focused**: Every concept taught with electrical engineering context
- **Project-Based Learning**: 4 complete, industry-relevant projects
- **Hands-On Approach**: All code works out of the box with detailed explanations
- **Beginner-Friendly**: Assumes only Python basics and Pandas knowledge
- **Modern Stack**: Industry-standard libraries and best practices

## Learning Objectives

By completing this course, you will be able to:

- Clean and prepare electrical engineering datasets for ML applications
- Perform exploratory data analysis on power systems data
- Build and evaluate regression models for energy demand forecasting
- Develop classification models for fault detection in power systems
- Implement neural networks for smart grid load classification
- Create time series models for renewable energy prediction
- Apply feature engineering techniques specific to electrical systems
- Interpret and communicate ML results to engineering stakeholders

## Prerequisites

- **Python Fundamentals**: Variables, loops, functions, basic data structures
- **Pandas Basics**: DataFrames, reading CSV files, basic data manipulation
- **Mathematics**: High school algebra (linear equations, basic statistics)
- **Domain Knowledge**: Undergraduate electrical engineering concepts

## Course Structure

### Module 1: Data Science Foundations (12-14 hours)
Learn to handle electrical engineering datasets effectively.

**Notebooks:**
1. Data Cleaning for Electrical Datasets
2. Exploratory Data Analysis and Visualization
3. Time Series Data Handling
4. Feature Engineering for Energy Systems

**Key Skills:** Data preprocessing, visualization with Matplotlib/Seaborn, handling time series, domain-specific feature creation

---

### Module 2: Machine Learning Fundamentals (6-8 hours)
Master the core concepts of machine learning.

**Notebooks:**
1. Introduction to Supervised and Unsupervised Learning
2. Model Evaluation and Validation Techniques

**Key Skills:** Train-test splitting, cross-validation, performance metrics (MAE, RMSE, R², Accuracy, F1), scikit-learn fundamentals

---

### Module 3: Regression Techniques (10-12 hours)
Predict continuous values in electrical systems.

**Notebooks:**
1. Linear and Multiple Regression
2. Polynomial Regression and Regularization
3. **PROJECT: Energy Demand Forecasting**

**Key Skills:** Linear models, feature scaling, regularization (Ridge, Lasso), time-based forecasting

**Project Outcome:** Complete energy demand forecasting system with hourly predictions

---

### Module 4: Classification Techniques (10-12 hours)
Categorize and detect patterns in power systems.

**Notebooks:**
1. Classification Basics (Logistic Regression, Decision Trees)
2. Advanced Classification (Random Forests, SVM)
3. **PROJECT: Fault Detection in Power Systems**

**Key Skills:** Binary and multi-class classification, ensemble methods, imbalanced datasets, confusion matrices

**Project Outcome:** Automated fault detection system identifying normal vs. fault conditions

---

### Module 5: Deep Learning Basics (10-12 hours)
Harness neural networks for complex patterns.

**Notebooks:**
1. Neural Network Fundamentals
2. TensorFlow and Keras Essentials
3. **PROJECT: Load Classification for Smart Grids**

**Key Skills:** Neural network architecture, activation functions, backpropagation, Keras API, model optimization

**Project Outcome:** Deep learning model classifying residential, commercial, and industrial loads

---

### Module 6: Time Series and Advanced Topics (10-12 hours)
Master sequential data and forecasting.

**Notebooks:**
1. Time Series Models (ARIMA, SARIMA)
2. LSTM Neural Networks for Sequential Data
3. **PROJECT: Renewable Energy Output Prediction**

**Key Skills:** ARIMA modeling, stationarity testing, LSTM architecture, sequence prediction

**Project Outcome:** Renewable energy forecasting system using weather data

---

## Installation

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/ML_Electrical_Engineering_Course.git
cd ML_Electrical_Engineering_Course
```

### Step 2: Create Virtual Environment (Recommended)

```bash
# Using venv
python -m venv ml_env

# Activate on Windows
ml_env\Scripts\activate

# Activate on macOS/Linux
source ml_env/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Launch Jupyter Notebook

```bash
jupyter notebook
```

Navigate to the module folders and start with Module 1!

## Datasets

All projects use either:
- **Real datasets** from Kaggle (links provided in notebooks)
- **Realistic synthetic data** generated within notebooks

See `datasets/README.md` for detailed information on data sources and generation methods.

### Dataset Overview:

1. **Energy Demand Data**: Hourly electricity consumption with timestamps (2+ years)
2. **Power System Fault Data**: Voltage, current, frequency measurements (normal + fault conditions)
3. **Smart Grid Load Data**: Load profiles with residential/commercial/industrial classifications
4. **Renewable Energy Data**: Solar irradiance, wind speed, temperature + power output

## Course Projects

### 1. Energy Demand Forecasting
**Module 3 | Regression Techniques**

Build a complete forecasting system to predict hourly energy demand using historical consumption patterns, weather data, and temporal features.

**Real-World Impact:** Helps utilities optimize generation schedules and reduce costs.

---

### 2. Fault Detection in Power Systems
**Module 4 | Classification Techniques**

Develop an automated fault detection system that identifies abnormal conditions in power systems by analyzing voltage, current, and frequency measurements.

**Real-World Impact:** Enables predictive maintenance and prevents equipment failures.

---

### 3. Load Classification for Smart Grids
**Module 5 | Deep Learning**

Create a neural network that classifies different types of electrical loads to enable demand response and grid optimization.

**Real-World Impact:** Supports smart grid management and energy efficiency programs.

---

### 4. Renewable Energy Output Prediction
**Module 6 | Time Series & LSTM**

Build an LSTM-based forecasting system that predicts solar or wind power output using weather forecasts and historical generation data.

**Real-World Impact:** Improves renewable energy integration and grid stability.

## Completion Certificate

To earn your course completion certificate:

1. Complete all 17 notebooks (including 4 projects)
2. Run all code cells successfully
3. Submit project notebooks with results
4. Pass the final assessment (optional capstone project)

Contact **BUILD_it** or **ELEESA** organizations for certificate verification and submission details.

## About the Organizations

### BUILD_it
An organization dedicated to building innovative technology solutions for engineering education and industry applications.

### ELEESA (Electrical Engineering Student Association)
A community of electrical engineering students and professionals committed to advancing technical skills and fostering collaboration.

## Contact and Support

- **Questions**: Open an issue on GitHub or contact BUILD_it/ELEESA
- **Contributions**: Pull requests welcome! See CONTRIBUTING.md
- **Discussions**: Join our Discord/Slack community (link in course portal)

## License

This course is provided for educational purposes. Please see LICENSE file for details.

## Acknowledgments

Developed with contributions from electrical engineering faculty, industry professionals, and the BUILD_it/ELEESA communities.

---

**Ready to start?** Navigate to `Module_01_Data_Foundations/01_Data_Cleaning.ipynb` and begin your ML journey!

**Course Version:** 1.0
**Last Updated:** November 2025
**Maintained by:** BUILD_it & ELEESA
