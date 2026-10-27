# Stock Market Risk Classification

This project uses machine learning and financial indicators to classify stock
observations into **Low Risk**, **Medium Risk**, and **High Risk** categories.
The workflow covers data cleaning, feature engineering, volatility-based
labeling, and exploratory visualization.

## Repository structure

```text
.
├── data/
│   ├── raw/                 # Original input data
│   └── processed/           # Cleaned, featured, and labeled datasets
├── docs/                    # Project synopsis and supporting documentation
├── notebooks/               # Reproducible analysis workflow
├── outputs/
│   └── figures/             # Generated charts and visualizations
├── .gitignore
├── README.md
└── requirements.txt
```

## Workflow

The notebook in [`notebooks/`](notebooks/) performs these steps:

1. Loads and sorts the raw stock data.
2. Cleans and exports the dataset.
3. Creates daily returns, a 10-day simple moving average, and rolling volatility.
4. Assigns risk categories using volatility quantiles.
5. Scales model features and exports the labeled dataset.
6. Generates exploratory visualizations.

## Getting started

```bash
python -m venv .venv
source .venv/bin/activate       # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

Open and run [`stock_market_risk_classification.ipynb`](notebooks/stock_market_risk_classification.ipynb)
from the `notebooks/` directory. Generated figures are saved under
`outputs/figures/`.

## Data

The raw dataset is stored at
[`data/raw/stock_data_july_2025.csv`](data/raw/stock_data_july_2025.csv).
Derived datasets are stored in [`data/processed/`](data/processed/).

## Documentation

See the [project synopsis](docs/project-synopsis.md) for the problem statement,
objectives, methodology, expected outcomes, and future scope.

## Disclaimer

This project is for educational and research purposes only. Its classifications
and predictions are not financial advice.
