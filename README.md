# Used car price prediction

Build a linear regression model to recommend used-car prices from vehicle attributes. The notebook sets a marketing target that 80% of predictions should fall within ±15% of the actual price.

## Data

`cs_04.csv` includes city, brand, production year, colour, mileage, body/engine/chassis condition, remaining insurance, gearbox, fuel type, and price.

## Method

`Linear-Regression.ipynb` cleans the data and fits linear models in Python (pandas, scikit-learn / statsmodels). Variants include all features, a Box-Cox transform of the target, and a selected-feature model. Performance is reported with RMSE, MAPE, MAE, and R-squared.

## Findings

From the notebook comparison, a linear model on all features had MAPE 12% and R-squared 0.76. After a Box-Cox transform, MAPE improved to about 9% and R-squared to 0.914. Selecting a subset of features after Box-Cox gave essentially the same MAPE (9%) and R-squared (0.914). These figures are from the committed notebook outputs.

## How to run

```bash
pip install -r requirements.txt
jupyter notebook Linear-Regression.ipynb
```
