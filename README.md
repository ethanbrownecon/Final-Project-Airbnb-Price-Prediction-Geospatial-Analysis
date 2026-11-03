# Predicting Airbnb Prices with Machine Learning

Final project for DAT 350, Data Management and Data Science, Berry College, Spring 2026.

## Question

What drives Airbnb listing prices, and which prediction model performs best?

## Why it matters

Prices vary widely across listings and markets. Knowing which features matter most, and how well common models predict price, is useful for hosts setting rates and for researchers studying short term rental markets.

## Data

More than 100,000 listings across U.S. cities from [Inside Airbnb](https://insideairbnb.com/get-the-data/). The data were collected with [fetch-insideairbnb-data](https://github.com/ethanbrownecon/fetch-insideairbnb-data). Raw files are not included. Prepare a combined file at `data/listings.csv` with the fields used in `airbnb_clean_chars.ipynb`, and follow Inside Airbnb's terms.

## Approach

1. Clean listing fields and normalize price and location values.
2. Engineer features and inspect their distributions.
3. Split the data into training and test sets.
4. Compare six models with cross validation: linear regression, lasso and other regularized regression, random forest, gradient boosting, and k nearest neighbors.
5. Explore spatial price patterns in an interactive Kepler.gl map (`kepler.gl.html`).

## Findings

Random forest achieved the highest R squared (0.502) and gradient boosting the lowest RMSE (197.04). Property size and capacity variables were the strongest predictors of price. These are predictive associations, not causal effects, and prices vary across markets and collection dates.

## Run

```bash
python -m pip install -r requirements.txt
jupyter lab airbnb_clean_chars.ipynb
```

Saved notebook outputs have been cleared.
