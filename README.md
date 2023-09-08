# Predictive Modeling for Leukocyte Telomere Length

## Overview

This repository presents a data analysis project that focuses on building a predictive model for leukocyte (white blood cells) telomere length using a dataset of 864 adults. Leukocyte telomere length (LTL) is a trait associated with the risk of cardiovascular disease and cancer. The project encompasses exploratory data analysis (EDA), data preprocessing, and model development to understand the relationships among various covariates including exposure to PCBs (highly carcinogenic chemical compounds), dioxins, and furans, and categorical variables like male, age, smoking, and race. We use this to develop a suitable model to predict the LTL.

## Key Observations from EDA

- **High Correlation Among Exposures**: During the exploratory data analysis, we observed a substantial positive correlation among exposure variables, indicating potential collinearity in the dataset.

- **Age and Telomere Length**: An intriguing discovery was a negative correlation between age and telomere length, suggesting a potential relationship between aging and telomere health.

- **Data Normality Assumption**: Diagnostic plots revealed that the data did not adhere to the normality assumption. To address this, we applied a log transformation to the length variable, resulting in the fulfillment of all four assumptions.

## Data Preprocessing

- **Log Transformation**: To correct the normality assumption violation, we employed a log transformation on the length variable, ensuring that the data met all necessary assumptions for further analysis.

- **Variable Selection**: Utilized LASSO regression for variable selection to identify the most relevant predictors for our predictive model.

- **Education Category Removal**: To enhance predictive accuracy and minimize mean squared error, we excluded the education category from our analysis.

## Predictive Model

- **Furan3 as a Key Predictor**: Due to the high correlation among certain exposures, our predictive model primarily relies on the concentration of furan3 in an individual, in conjunction with other covariates, to predict mean leukocyte telomere length accurately.
