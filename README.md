# Stock KPIs
## Project Overview
### Business Problem
### Data Source
### Repository Structure
```
├── archive/                 # Archived SEC data and notebooks
├── data/                    # See more detailed explanation below
│    ├── merged_data/
│    ├── preprocessed_data/
│    ├── price_histories/
│    ├── simfin/
│    └── sp500.csv
├── images/                  # Exported images of plots
├── models/                  # Exported models using joblib
├── notebooks/               # Notebooks used for prep, modeling, etc.
├── submissions/             # Files used for the project submissions
├── .gitignore
├── LICENSE
└── README.md
```

Further explanation of the `data` directory is warranted given the multiple subdirectories. 
- `merged_data` contains files for companies where the price histories and fundamental data has been merged together.
- `preprocessed_data` contians files for each file in the `merged_data` directory that has had its missing values handled.
- `price_histories` contains historical share price data for each company.
- `simfin` contains fundamanetal data for each company's Income Sheet, Balance Sheet, and Cash Flow Statement.
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