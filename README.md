## Project Overview
This project uses Gradient Boosting to forecast e-commerce sales and inform inventory decisions. After preprocessing and model comparison, Gradient Boosting achieved strong generalization. Sales predictions were then used in a simulation framework to identify inventory levels that maximize profit.
# Sales and Inventory Forecasting with Gradient Boosting

## Data Description
The dataset contains sales information for approximately 100 products observed over a 60-day period. Features include product attributes, customer demographics, pricing variables, and temporal indicators such as weekdays. The sales variable is available only in the training data and must be predicted for unseen observations.

## Data Preprocessing & Feature Engineering
Key preprocessing steps implemented in the notebook include:
- Log transformation of sales to reduce skewness and stabilize variance
- Standardization of numerical predictors
- One-hot encoding of categorical variables such as weekdays
- Creation of interaction terms based on domain knowledge (e.g., pricing and customer activity)
- Removal of irrelevant identifiers and weakly correlated features

These steps are designed to improve model stability and predictive performance.

## Modeling
Multiple regression-based models are explored and compared, including:
- Linear regression with Ridge and Lasso regularization
- Random Forest regression
- Gradient Boosting regression

Models are evaluated using mean squared error (MSE) and cross-validation. Special attention is given to the gap between training and validation errors to control overfitting. Gradient Boosting achieves the best balance between accuracy and generalization and is chosen as the final model.

## Inventory Decision Framework
Using predictions from the Gradient Boosting model, the project implements a simulation-based inventory decision framework. Inventory levels are adjusted by varying margins above predicted demand, and total profit is calculated by accounting for revenue, inventory cost, and salvage value. The simulation identifies an inventory strategy that maximizes overall profit.

## Files in This Repository
- `sales_inventory_gradient_boosting.ipynb`  
  The main notebook containing data exploration, preprocessing, model training, evaluation, and inventory simulation.

## Tools & Libraries
- Python
- pandas, numpy
- scikit-learn
- matplotlib / seaborn
- Jupyter Notebook

## Notes
This project emphasizes an end-to-end applied machine learning workflow, connecting predictive modeling with operational decision-making rather than focusing solely on model performance metrics.
