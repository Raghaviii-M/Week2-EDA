# Week 2: Exploratory Data Analysis (UCI Wine Quality)

## Overview
This project is a comprehensive Exploratory Data Analysis (EDA) of the UCI Wine Quality dataset, completed as the Week 2 task of a Data Science internship. It covers data quality checks, descriptive statistics, univariate and multivariate visualisation, and hypothesis testing, with annotated inferences for every chart and test.

## Dataset
- **Source:** https://archive.ics.uci.edu/dataset/186/wine+quality
- **Content:** 1,599 red and 4,898 white Vinho Verde wines (6,497 rows), 11 physicochemical variables plus a sensory `quality` score (0 to 10). A `type` column (red/white) was added when combining the files.
- **Note:** files are semicolon-separated (`sep=";"`).

## Key findings
- No missing values; <N> exact duplicate rows were found and retained (see the report for the reasoning).
- Quality scores are concentrated between 5 and 7, so the target is imbalanced.
- Alcohol has the strongest positive correlation with quality (r = <VALUE>); density and volatile acidity are negatively correlated.
- Density and alcohol, and free and total sulfur dioxide, are strongly correlated, which indicates multicollinearity.
- Red and white wines differ significantly in chemistry and mean quality (Welch t-test, p = <VALUE>).

## Analysis performed
1. Data quality checks (types, missing values, duplicates)
2. Descriptive statistics (mean, median, std, IQR, skewness, kurtosis, CV)
3. Univariate analysis (histograms, boxplots, count plots, IQR outliers)
4. Bivariate and multivariate analysis (correlation heatmap, scatter plots, pairplot, group comparisons)
5. Hypothesis testing (Pearson/Spearman, Welch t-test, one-way ANOVA/Kruskal-Wallis, chi-square)
6. Key insights, assumptions and limitations

## Project structure
```
week2-eda/
├── data/raw/              original CSV files (red and white wine)
├── notebooks/eda.ipynb    full analysis code with commentary
├── report/                EDA report (.docx and .pdf)
│   └── figures/           saved charts used in the report
├── requirements.txt       Python dependencies
└── README.md
```

## How to run
1. Clone the repository and open the folder in VS Code.
2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   venv\Scripts\activate          # Windows
   source venv/bin/activate       # Mac/Linux
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Place `winequality-red.csv` and `winequality-white.csv` in `data/raw/`.
5. Open `notebooks/eda.ipynb`, select the `venv` kernel and choose **Run All**. Figures are saved to `report/figures/`.

## Tools
Python, pandas, NumPy, Matplotlib, Seaborn, SciPy, statsmodels, Jupyter, Git/GitHub

## Author
<Your Name>, Data Science Intern, <Organization>
