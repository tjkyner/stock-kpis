# Stock KPIs
## Project Overview
### Business Problem
As [defined by Investopedia](https://www.investopedia.com/terms/k/kpi.asp), a Key Performance Indicator (KPI) is "... a set of quantifiable measurements used to gauge a company's overall long-term performance." While KPIs are typically used internally to measure goal-specific progress, this project aims to extend the idea and provide a proof-of-concept analysis of the most important fundamental factors with regard to a given company's share price.

Traditional equity valuation models rely on some form of forecasting the evolution of income sheet, balance sheet, and cash flow statement line items into the near future combined with an expected terminal value. While this methodology is the theoretically "correct" way to value a company's equity, there is no inherent check for the relative importance of each line item beyond the valuation analyst's domain expertise. Enhanced insight into these relative importances would allow for more efficient utilization of the analyst's focus and could ultimately lead to more accurate valuations and price predictions. A simplified workflow incorporating the Stock KPIs project would look as follows:

![Workflow](images/workflow.png)

### Data Sources
Multiple data sources were used in order to complete this project. Initially, all fundamental data was downloaded in bulk directly from the SEC using their relatively new [EDGAR API](https://www.sec.gov/edgar/sec-api-documentation). However, due to lack of documentation, support, and missing values, this data was scrapped in favor of alternative sources of fundamental data such as [SimFin](https://simfin.com/). Historical pricing data and miscellaneous company information (website, business summary, etc.) was obtained from Yahoo! Finance via the [`yfinance`](https://github.com/ranaroussi/yfinance) package. Finally, the current S&P 500 constituents (as of late August 2021) was retrieved from the *[List of S&P 500 companies](https://en.wikipedia.org/wiki/List_of_S%26P_500_companies)* article on Wikipedia.

![Data sources](images/data_sources.png)

### Repository Structure
```
├── archive/                 # Archived SEC data and notebooks
├── data/                    # See more detailed explanation below
│    ├── merged_data/
│    ├── preprocessed_data/
│    ├── price_histories/
│    ├── simfin/
│    └── sp500.csv
├── images/                  # Images used in the readme, presentation, etc.
├── models/                  # Exported models using joblib
├── notebooks/               # Notebooks used for data gathering, prep, modeling, etc.
├── submissions/             # Files used for the project submissions
├── .gitignore
├── LICENSE
└── README.md
```

Further explanation of the `data` directory is warranted given the multiple subdirectories. 
- `merged_data` contains files for companies where the price histories and fundamental data has been merged together.
- `preprocessed_data` contians files for each file in the `merged_data` directory that has had its missing values handled.
- `price_histories` contains historical share price data for each company.
- `simfin` contains fundamanetal data for each company's income sheet, balance sheet, and cash flow statement.
- `sp500.csv` is a file that contains a list of each company in the S&P 500 with basic information such as the ticker, company name, industry, etc.

## Preprocessing
### Merging Data
### Handling Missing Values

## Modeling
### `XGBRFRegressor`
### Hyperparameter Tuning
### Example Feature Importances
### Exporting Models

## Interactive Dashboard
### Overview Tab
### Features Tab
### SHAP Analysis Tab