# Red Wine Quality Prediction — Linear Regression

## Project Overview
This project uses **Orange Data Mining** to build and evaluate a Linear Regression model for predicting red wine quality from physicochemical measurements.

- **Problem type:** Regression
- **Target variable:** `quality`
- **Tool:** Orange Data Mining (`.ows` workflow)
- **Workflow file:** `wine red.ows`

The aim is to estimate a numerical wine-quality score from measurements such as acidity, residual sugar, chlorides, sulfur dioxide, density, pH, sulphates, and alcohol.

## Dataset
The workflow screenshot shows 1,120 rows being evaluated. The visible attributes include:

- `quality` (target)
- `fixed acidity`
- `volatile acidity`
- `citric acid`
- `residual sugar`
- `chlorides`
- `free sulfur dioxide`
- `total sulfur dioxide`
- `density`
- `pH`
- `sulphates`
- `alcohol`

**Note:** The README is based on the supplied Orange workflow and screenshot. Confirm the exact dataset source, number of rows, and any preprocessing steps from your original data file before publishing.

## Workflow
The supplied Orange workflow contains these widgets:

1. **File** — loads the dataset.
2. **Data Sampler** — samples the data for the workflow.
3. **Linear Regression** — trains a regression learner.
4. **Test and Score** — evaluates the learner.
5. **Predictions** — displays predictions and prediction errors.

The workflow connects the sampled data to the model evaluation and prediction widgets.

## Evaluation Results
The supplied screenshot reports the following Linear Regression scores:

| Metric | Result |
|---|---:|
| MSE | 0.429 |
| RMSE | 0.655 |
| MAE | 0.515 |
| MAPE | 9.334 |
| sMAPE | 9.122 |
| R² | 0.352 |

These results are specific to the run shown in the screenshot. They may change with a different sample, train/test split, preprocessing, or Orange settings. An R² of 0.352 means the model explains about 35.2% of the variation in the target on that evaluation; there is room to improve predictive performance.

## How to Run
1. Install [Orange Data Mining](https://orangedatamining.com/).
2. Open Orange.
3. Open the supplied `wine red.ows` workflow.
4. In the **File** widget, ensure the correct red-wine dataset is selected and loaded.
5. Check the connections and settings in **Data Sampler**, **Linear Regression**, and **Test and Score**.
6. Open **Test and Score** to review metrics.
7. Open **Predictions** to inspect predicted quality and errors.

## Possible Improvements
- Compare Linear Regression with Random Forest Regression, Gradient Boosting, and other regression learners.
- Inspect missing values, duplicates, outliers, and feature distributions.
- Use a reproducible train/test split or cross-validation.
- Compare models using RMSE and MAE, not R² alone.
- Check for target leakage and document the evaluation method.
- Add charts showing actual versus predicted quality and residual errors.

## Project Goal
Demonstrate an end-to-end introductory regression workflow: data loading, model training, evaluation, and reviewing predictions in Orange Data Mining.

## Files
- `wine red.ows` — Orange workflow.
- `README.md` — project documentation.
