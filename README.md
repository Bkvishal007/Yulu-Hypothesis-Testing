# Yulu-Hypothesis-Testing
A data-driven analysis of Yulu's bike-sharing operations using statistical hypothesis testing. The project applies t-tests, ANOVA, and chi-square tests to uncover usage patterns and generate actionable business insights through Python and visualization tools.
## Objective

The goal is to analyze Yulu’s operational data and validate key business assumptions using statistical techniques including:

- Independent t-tests  
- ANOVA (Analysis of Variance)  
- Chi-Square Tests  

## Key Components

- Data cleaning and exploratory analysis of the bike-sharing dataset  
- Statistical tests to evaluate user behavior and demand variations  
- Visualizations using Matplotlib and Seaborn  
- Actionable business recommendations based on findings  

## Tech Stack

- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- SciPy (ttest, ANOVA, chi-square)  

## Interpretation and Reporting:

(1) Visual Analysis:
(a) Temperature Distribution: The histogram of temperature shows a normal distribution with a peak around 20-25°C. This indicates that most of the rentals occur when the temperature is in this range.
(b) Feeling Temperature Distribution: Similar to the actual temperature, the feeling temperature also follows a normal distribution, peaking around 20-25°C.
(c) Humidity Distribution: The humidity distribution is slightly skewed to the right, with most values clustering between 50-80%. Higher humidity might slightly deter rentals.
(d) Windspeed Distribution: Windspeed is heavily right-skewed, with most values below 20 km/h. High wind speeds are relatively rare.
(e) Total Rental Bikes Distribution: The rental count distribution is right-skewed, indicating that on many days, rentals are lower, but there are a few days with very high rentals.
(f) Season Count Plot: The rentals are fairly evenly distributed across the seasons, but there might be a slight increase during summer (season 2) and fall (season 3).
(g) Holiday Count Plot: There are fewer data points for holidays, indicating that there are fewer holidays than non-holidays in the dataset.
(h) Working Day Count Plot: There are more working days than non-working days, which aligns with the typical 5-day workweek.
(i) Weather Count Plot: Most of the days have clear or misty weather conditions (categories 1 and 2).

(2) Hypothesis Formulation:

(1).Test: 2-Sample T-Test:
Null Hypothesis (H0): Working day has no effect on the number of electric cycles rented. Alternative Hypothesis (H1): Working day has an effect on the number of electric cycles rented.

(2).ANOVA for Weather:
Null Hypothesis (H0): The number of cycles rented is similar across different weather conditions. Alternative Hypothesis (H1): The number of cycles rented is different across different weather conditions.

(3).ANOVA for Season:
Null Hypothesis (H0): The number of cycles rented is similar across different seasons. Alternative Hypothesis (H1): The number of cycles rented is different across different seasons.

(4).Chi-Square Test:
Null Hypothesis (H0): Weather is independent of the season. Alternative Hypothesis (H1): Weather is dependent on the season.

Test Assumptions:
Normality: For the t-test and ANOVA, we assume that the rental counts are approximately normally distributed within each group. This can be visually checked using histograms or Q-Q plots.

Equal Variance: For ANOVA, we assume that the variances of rental counts are similar across different groups (weather conditions and seasons). Levene’s test can be used to check this assumption. Independence: For the chi-square test, we assume that the observations are independent.

Inference:
Based on the results of our analysis:

Working Days vs. Non-Working Days:
The significant difference in rentals between working and non-working days suggests that the company might experience higher demand on working days. This could be due to people using electric cycles for commuting purposes during workdays. Weather Conditions:

Weather significantly impacts the number of rentals. The company should consider weather forecasts to optimize the availability of cycles. For instance, fewer rentals might be expected in bad weather, and promotions could be targeted during such times to maintain usage levels. Seasonal Variations:

Rentals vary significantly across seasons. For instance, summer and fall may have higher rentals. The company could use this information to plan for seasonal maintenance and promotional activities to boost rentals during off-peak seasons.

Dependency of Weather on Season:
Since weather is dependent on the season, the company can anticipate weather patterns based on the season and plan their operations accordingly. For example, more clear days in summer might lead to higher rentals.


