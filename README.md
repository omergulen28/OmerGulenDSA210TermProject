# Step Count vs Weather Analysis
An analysis of how weather conditions especially temperature affect my daily step count and activity level using Apple Health and weather data.

Motivation
Many people notice that their physical activity changes with the weather — for instance, we walk less on cold or rainy days. Through this project, I want to understand whether temperature and other environmental factors influence my daily movement patterns.

Data Sources
Apple Health Data: Exported directly from the Apple Health app on my iPhone as XML/CSV files.
Weather Data: Collected using a public API such as Open-Meteo
 or Visual Crossing Weather API
The data includes temperature, humidity, and precipitation levels for the same days as my step data.

Data Collection Plan
Export Apple Health data (steps, walking distance, active energy).
Filter data by date (e.g., last 3–6 months)
Retrieve daily weather information for my location and merge with Apple Health data using date as the key.
Clean and preprocess the dataset (handle missing values, time zones, etc.).

Planned Analysis
Exploratory Data Analysis (EDA): Visualize step counts vs. temperature, humidity, and precipitation.
Correlation Analysis: Quantify relationships between temperature and activity level.
Statistical Testing: Test whether mean step counts differ significantly across temperature ranges (e.g., t-tests or ANOVA).
Machine Learning (later phase): Use regression models to predict daily step count based on weather data.

Expected Insights
Identify temperature ranges where step count is highest.
Observe how activity decreases on colder or rainy days.
Understand whether weather can predict physical activity trends.

Tools & Technologies
Python, Pandas, NumPy, Matplotlib/Seaborn for analysis and visualization
Jupyter Notebook for workflow documentation
GitHub for version control

Limitations & Future Work
Limited to one individual’s Apple Health data.
Weather data may not capture micro-climate variations.
Future work could include comparing results with data from other users or multiple cities.
