# Multi-Asset ETF Rotation Strategy

**Authors:** Thomas O'Neill, Conway Zhou

A machine learning-driven multi-asset ETF rotation strategy benchmarked against Mebane Faber's classic 10-month SMA momentum baseline.

Full details on the project can be read in the interactive report, under `Report/interactive_report.ipynb`.


## Project Structure

```
ml4t-etf-rotation/
├── phase1/
│   └── phase1_data_collection.ipynb   # Downloads ETF prices and macro data
├── phase2/
│   ├── ETF_EDA.ipynb                  # Exploratory data analysis
│   └── ETF_FeatureEngineering_Edited.ipynb  # Computes technical indicators
├── phase3/
│   ├── faber_baseline.ipynb           # Faber SMA strategy backtest
│   └── ml_strategy.ipynb             # LightGBM strategy backtest
├── phase4/
│   └── phase4_comparison.ipynb        # Performance comparison and charts
├── Report/
│   └── interactive_report.ipynb       # Full project report
├── figures/                           # Saved chart outputs
├── cleaned_prices.csv                 # Monthly ETF prices
├── cleaned_prices_daily.csv           # Daily ETF prices (for volatility)
├── cleaned_macro.csv                  # Monthly macro indicators
├── feature_engineer_csv.csv           # Engineered feature table
├── faber_returns.csv                  # Faber monthly returns
└── ml_returns.csv                     # ML strategy monthly returns
```

## How to Run

Run the notebooks in order:

1. `phase1/phase1_data_collection.ipynb` — downloads and cleans data
2. `phase2/ETF_FeatureEngineering_Edited.ipynb` — engineers features
3. `phase3/faber_baseline.ipynb` — runs Faber backtest
4. `phase3/ml_strategy.ipynb` — runs ML backtest
5. `phase4/phase4_comparison.ipynb` — generates comparison metrics and charts

---

## Dependencies

Install dependencies via:

```
install_dependencies.bat
```

Key packages: `yfinance`, `lightgbm`, `pandas`, `numpy`, `matplotlib`, `plotly`, `pyfolio`, `polars`, `ml4t-engineer`