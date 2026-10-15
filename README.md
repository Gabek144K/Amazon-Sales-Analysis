# What Drives Amazon Product Ratings?

An end-to-end data analysis project in Python: cleaning messy e-commerce data, exploring it with charts, and building machine learning models to predict product ratings.

**Data:** [Amazon Sales Dataset (Kaggle)](https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset), 1,465 Amazon India listings (1,348 unique products after cleaning).

## Key findings
- **Ratings are tightly clustered:** 88% of products are rated between 3.8 and 4.5 stars.
- **Deeper discounts go with lower ratings:** 83% of products discounted 0–20% are rated 4+ stars, compared with 57% of products discounted more than 80%.
- **Ratings are hard to predict from listing data alone:** the best model explains about 16–17% of the variation (5-fold CV R²) and cuts the average error from 0.23 to 0.20 stars.
- **Popularity and price matter most:** the number of ratings is the strongest predictor, followed by price and category.

![Share of products rated 4+ stars by discount band](charts/04_discount_band_share_4plus.png)

## What's inside
| File | Description |
|---|---|
| `amazon_rating_analysis.ipynb` | The full analysis, with commented code and outputs |
| `amazon.csv` | Raw data |
| `amazon_clean.csv` | Cleaned data (also usable in R) |
| `charts/` | All charts as high-resolution PNGs |

## Methods
Data cleaning (currency/text-to-number conversion, de-duplication, category parsing) · feature engineering (log transforms, discount bands) · EDA and visualization (matplotlib, seaborn) · regression models (Linear Regression, Random Forest) compared against a baseline · 5-fold cross-validation · permutation feature importance

## Run it yourself
```bash
pip install -r requirements.txt
jupyter notebook amazon_rating_analysis.ipynb
```
