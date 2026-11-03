# Airbnb Price Prediction and Geospatial Analysis

An exploratory workflow for cleaning multi-market Airbnb listings, engineering
listing features, comparing regression models, and visualizing spatial price
patterns. The repository also contains an interactive Kepler.gl map generated
from the project data.

## Preview

Open [`kepler.gl.html`](./kepler.gl.html) in a browser to explore the existing
interactive map.

## Data

Raw listing data is not included. The original source files were several
gigabytes across many markets, and listing data should be obtained and cited
from [Inside Airbnb](https://insideairbnb.com/get-the-data/) under its current
terms. For the notebook, prepare a combined listing file at
`data/listings.csv` with the fields referenced in `airbnb_clean_chars.ipynb`.
The generated map is retained as a project artifact.

## Run the notebook

```bash
python -m pip install -r requirements.txt
jupyter lab airbnb_clean_chars.ipynb
```

The notebook's saved cell outputs have been cleared. Its results are
exploratory: associations and feature importance do not establish causal
effects, and listing prices may vary across markets and collection dates.

## Workflow

1. Clean listing fields and normalize price and location values.
2. Engineer analysis features and inspect their distributions.
3. Split the data into training and test sets.
4. Compare linear, regularized, tree-based, boosting, and nearest-neighbor
   regressors with cross-validation.
5. Explore price patterns with an interactive geospatial visualization.
