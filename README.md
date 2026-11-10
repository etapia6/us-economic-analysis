# U.S. Economic Analysis: Unemployment and Economic Indicators (2000–2024)

## Project Overview

This project analyzes the relationship between U.S. unemployment and key economic indicators from 2000 to 2024 using Python and data from the World Bank API.

The analysis explores economic trends, examines correlations between economic variables, and develops regression models to evaluate how economic indicators relate to unemployment.

## Research Questions

- How has U.S. unemployment changed between 2000 and 2024?
- What relationships exist between unemployment, GDP growth, inflation, and GDP per capita?
- Can economic indicators help explain changes in unemployment?
- Does incorporating previous year's unemployment improve model performance?

## Data Sources

Data was retrieved from the **World Bank Open Data API** for the United States.

| Indicator | World Bank Indicator Code |
|---|---|
| Unemployment | SL.UEM.TOTL.NE.ZS |
| GDP Growth | NY.GDP.MKTP.KD.ZG |
| Inflation | FP.CPI.TOTL.ZG |
| GDP per Capita | NY.GDP.PCAP.KD |

The dataset contains 25 annual observations covering 2000–2024.

## Tools and Technologies

- Python
- Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- scikit-learn
- statsmodels
- World Bank API

## Methodology

The project followed these steps:

1. Retrieved economic indicators using the World Bank API.
2. Cleaned and merged datasets using pandas.
3. Conducted exploratory data analysis and descriptive statistics.
4. Examined correlations between economic indicators.
5. Created visualizations to identify economic trends.
6. Developed simple and multiple linear regression models.
7. Compared model performance using R-squared and RMSE.
8. Evaluated models using a chronological training and testing split.
9. Tested additional predictors, including GDP per capita and lagged unemployment.
10. Interpreted model coefficients, prediction errors, and economic findings.

## Model Development and Results

Three regression models were evaluated using a chronological split:

- Training period: 2000–2019
- Testing period: 2020–2024

| Model | Test R-squared | Test RMSE |
|---|---:|---:|
| GDP Growth + Inflation | 0.4215 | 1.2760 |
| GDP Growth + Inflation + GDP per Capita | -0.6293 | 2.1414 |
| GDP Growth + Inflation + Previous Unemployment | 0.6946 | 0.9271 |

The lagged unemployment model achieved the strongest test performance among the three models evaluated.

Its predictors were:
- GDP Growth
- Inflation
- Previous Year's Unemployment

The model achieved a test R-squared of **0.6946** and a test RMSE of **0.9271 percentage points**.

## Key Findings

- Unemployment increased during major economic downturns, particularly the 2008–2010 financial crisis and the 2020 pandemic.
- GDP growth and unemployment exhibited a moderate negative correlation.
- Inflation increased substantially during 2021–2022.
- Real GDP per capita generally increased over the 25-year period.
- Previous year's unemployment improved the predictive performance of the regression model.
- Adding GDP per capita did not improve out-of-sample model performance.

## Limitations

- The dataset contains only 25 annual observations.
- The testing period contains only five observations.
- The models use a limited selection of economic predictors.
- Major economic events may affect relationships between economic variables.
- Regression results identify statistical associations, not causation.
- The lagged model uses the previous year's actual unemployment rate and does not represent a five-year forecast made in advance.

## Repository Structure

```text
us-economic-analysis/
│
├── notebooks/
│   └── 01_economic_exploration.ipynb
│
└── README.md
```

## How to Run

1. Clone or download this repository.
2. Install the required Python libraries:

```bash
pip install pandas numpy matplotlib scikit-learn statsmodels requests jupyter
```

3. Open the Jupyter Notebook:

```bash
jupyter notebook
```

4. Navigate to `notebooks/01_economic_exploration.ipynb`.
5. Run the notebook cells in order.

The notebook retrieves economic data through the World Bank API, so an internet connection is required.

## Skills Demonstrated

- Data collection through APIs
- Data cleaning and preprocessing
- Exploratory data analysis
- Statistical analysis and correlation
- Data visualization
- Linear regression
- Model evaluation and comparison
- Residual analysis
- Multicollinearity analysis
- Chronological model validation
- Economic interpretation

## Author

**Eliane Tapia**

Bachelor of Arts in Interdisciplinary Mathematics and Economics  
Fordham University

[LinkedIn](https://www.linkedin.com/in/eliane-tapia/)
