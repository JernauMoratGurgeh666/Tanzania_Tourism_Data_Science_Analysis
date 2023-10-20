# 🦁 Tanzania Tourism ML Project – by ELIAS KOULOURES

This repo is for Tanzania Tourism prediction model.

<br>

Data & info: https://zindi.africa/competitions/tanzania-tourism-prediction/data

<br>

## 🍿 Video of my presentation:

https://www.linkedin.com/posts/eliaskouloures_tanzania-tourism-datascience-activity-7120355344614047745-J1DT

<br>

## 📊 Charts of my presentation:

www.eliaskouloures.com/portfolio-collections/portfolio/tanzania-tourism-creative-data-science-solutions



<br>

## 💪🏻 Requirements & Environment

Requirements:
- pyenv with Python: 3.11.3

Environment: 

For installing the virtual environment you can either use the Makefile and run `make setup` or install it manually with the following commands: 

```Bash
pyenv local 3.11.3
python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```
<br>
<br>

## 👍🏻 Usage

In order to train the model and store test data in the data folder and the model in models run:

```bash
#activate env
source .venv/bin/activate

python example_files/train.py  
```

In order to test that predict works on a test set you created run:

```bash
python example_files/predict.py models/linear_regression_model.sav data/X_test.csv data/y_test.csv
```
<br>

## ⚡️ Limitations

Development libraries are part of the production environment, normally these would be separate as the production code should be as slim as possible.
<br>
<br>
<br>

# 📝 Project Overview

- Goal is to predict how much money a tourist will spend when visiting Tanzania using ML models.

- This can help tour operators and Tanzania Tourism Board estimate tourist spending.

- Dataset has information on 6476 tourists collected by the National Bureau of Statistics in Tanzania.

- Majority of visitors are aged 25-44 and visit for business or leisure/holidays.

- Data covers 7 departure points: 4 airports and 3 land border crossings.
<br>
<br>

# 🌟 Key Challenges

- Build an accurate ML model to predict tourist spending using the provided dataset.

- Choose the right evaluation metrics and optimization techniques.

- Handle any data quality issues and biases.

- Interpret model results for actionable insights.
<br>
<br>

# 👣 Step-by-Step Data Science Process

1. **Data Cleaning**

- Check for missing values in each column using `.isnull().sum()` and decide whether to drop rows/columns or impute missing values based on analysis.

- Identify and remove any duplicate rows using `df.duplicated()`. 

- Check for invalid/inconsistent values like negative numbers for spending, invalid country codes etc. and fix or remove as needed.

- Encode categorical columns like country, age group etc. using one-hot encoding or label encoding.
<br>
<br>

2. **Exploratory Data Analysis** 

- Compute summary statistics like mean, median, min, max for numerical columns using `df.describe()`.

- Create histograms and density plots for numerical columns to analyze distributions. 

- For categorical variables, plot bar charts or countplots to see frequencies using `sns.countplot()`.

- Compute correlation matrix between all variables using `df.corr()` to identify highly correlated variables.

- Analyze univariate distributions, bivariate relationships with target, correlations etc. to gain insights.
<br>
<br>

3. **Model Building**

- Split data into 80% train and 20% test sets using `train_test_split`.

- Train a linear regression model on the train set with tourist spending as the target.

- Evaluate on test set using RMSE, R^2, MAPE. Interpret coefficients.
<br>
<br>

4. **Advanced Models**

- Try other models like random forest, SVM, gradient boosting using Sklearn.

- Use `cross_val_score` to evaluate each model with k-fold cross validation. 

- Report performance metrics like RMSE, R^2 for each model.
<br>
<br>

5. **Model Comparison** 

- Plot model performance metrics side-by-side in a bar plot for comparison.

- Use box plots to show distribution of scores across cross-validation folds.
<br>
<br>

6. **Model Optimization**

- For best model, use grid search to tune hyperparameters.

- Evaluate using cross-validation to avoid overfitting. 

- Reduce search space for efficiency.
<br>
<br>

7. **Parameter Performance**

- For key hyperparameters like max_depth, n_estimators etc. create line plots to analyze impact on model score.
<br>
<br>

8. **Model Interpretation**

- For tree-based methods, use `.feature_importances_` to get importance of each feature.

- Create plots to visualize and explain feature effects.
<br>
<br>

9. **Project Report**

- Document data cleaning, EDA, feature engineering steps in detail. 

- Include methodology, results, interpretations for each model tried.

- Summarize performance comparison, final model details, limitations and recommendations.
<br>
<br>

10. **Additional Data Sources**

- Gather country-level data like GDP, population, tourism infrastructure to provide more context.

- Incorporate seasonal factors, events data that may affect tourist visits.

<br>
<br>

# 🌍 External datasets to improve Tourism advice:

1. **Economic Indicators by Country**: GDP, income levels, and unemployment rates could help understand the spending capabilities of tourists from different countries.
   
2. **Flight Data**: Information on flight frequencies, costs, and durations from different countries to Tanzania could help correlate ease of travel with tourist numbers.

3. **Global Tourism Statistics**: Data on global travel trends could offer a comparison point for Tanzania's tourism performance.

4. **Currency Exchange Rates**: Fluctuations in currency exchange rates could affect tourism and spending. Historical data could be valuable.

5. **Hotel Rates and Availability**: Data on accommodation could be used to understand its correlation with tourist numbers and spending.

6. **Weather Data**: Information on climate and weather patterns could help in understanding seasonal trends in tourism.

7. **Event Calendar**: Data on major events, festivals, or conferences in Tanzania could explain spikes in tourism numbers.

8. **Social Media or Review Data**: Data from platforms like TripAdvisor could offer insights into tourist preferences and satisfaction levels.

9. **Political Climate Index**: A stable political environment often correlates with higher tourist numbers. Indices that measure political stability could be beneficial.

10. **Competitive Analysis**: Data on similar tourist destinations could help in understanding what Tanzania is up against and what it could improve.

11. **Covid-19 Statistics**: Current health advisories and COVID-19 statistics can also play a significant role in travel plans.

12. **Public Transport Information**: Accessibility within the country could also be a factor affecting tourist preferences.

Adding these datasets could introduce a multi-dimensional aspect to the analysis, allowing for more robust models and insights. However, it's important to be mindful of the challenges in integrating these datasets, such as missing values and the need for data transformation or encoding.
