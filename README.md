# Time Series Forecasting - M5 Demand Forecasting

This repository contains a time series forecasting project focused on demand prediction using the M5 dataset.

## Project Structure

```
demand-forecasting-notebook/
└── m5-forecasting-accuracy/
    ├── calendar.csv           (excluded from repo - see setup below)
    ├── sales_train_evaluation.csv (excluded from repo - see setup below)
    ├── sales_train_validation.csv (excluded from repo - see setup below)
    ├── sell_prices.csv        (excluded from repo - see setup below)
    └── sample_submission.csv  (excluded from repo - see setup below)
```

## Setup Instructions

### 1. Environment Setup

Activate the conda environment:
```bash
conda activate ./.env
```

Or create a new environment if needed:
```bash
conda create -y -p ./.env python=3.10
conda activate ./.env
```

### 2. Dataset Setup

The large CSV data files are not included in this repository to keep it lightweight. You need to download them manually:

**Option A: Download from Kaggle**
1. Go to the [M5 Forecasting Accuracy Competition](https://www.kaggle.com/competitions/m5-forecasting-accuracy)
2. Download the dataset files
3. Extract and place the CSV files in: `demand-forecasting-notebook/m5-forecasting-accuracy/`

**Option B: Use Kaggle API**
```bash
# Install kaggle API
pip install kaggle

# Configure credentials (~/.kaggle/kaggle.json)
# Then download:
kaggle competitions download -c m5-forecasting-accuracy
unzip m5-forecasting-accuracy.zip -d demand-forecasting-notebook/m5-forecasting-accuracy/
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt  # if available
# or manually:
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

## Files Excluded from Git

The following large CSV files are tracked locally but not committed to git:
- `calendar.csv` (~116 MB)
- `sales_train_evaluation.csv` (~116 MB)
- `sales_train_validation.csv` (~114 MB)
- `sell_prices.csv` (~194 MB)
- `sample_submission.csv`

See `.gitignore` for exclusion patterns.

## Usage

1. Activate the environment
2. Download the datasets (see above)
3. Start Jupyter: `jupyter notebook`
4. Open and run the notebooks in `demand-forecasting-notebook/`

## Notes

- The `.env/` folder contains the conda environment and is excluded from git
- CSV files are excluded from git tracking to keep repository size manageable
- Data should be stored locally after download