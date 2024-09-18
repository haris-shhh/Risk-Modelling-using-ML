
# Scorecard Analysis

This project involves analysing and evaluating multiple variables using the Kolmogorov-Smirnov (KS) statistic to determine their effectiveness in distinguishing between classes for risk prediction. The scorecards are assessed to understand their discrimination ability.

## Contents

- **scorecard_analysis.ipynb**: Jupyter Notebook containing the analysis of the scorecards.
- **dataset.xlsx/**: Datasets used for the scorecard evaluation.

## Libraries required
- pandas
- numpy
- matplotlib
- scikit-learn

## Analysis Overview

The primary analysis involves calculating the ANOVA scores for each feature to understand it's significance in predictions.![image](https://github.com/user-attachments/assets/1f3f9202-d693-4c49-ac62-942b25200d67)

The variables are then chosen based on the highest ANOVA scores and the criteria that each scorecard should have 2 continuous variables and 2 categorical variables. Then each scorecard should classify the customers' risk with linear and logistic regression models. KS statistic for each scorecard  is used to evaluate its performance. The KS statistic measures the maximum distance between the cumulative distributions of the scores of the positive and negative classes.

## Linear Regression ROC plots for both scorecards
![image](https://github.com/user-attachments/assets/d3181398-34d5-4035-a9a3-733a298d2556)

## Logistic Regression ROC plots for both scorecards
![image](https://github.com/user-attachments/assets/e02df729-70b0-4b55-94f4-11f291687f57)

### Statistics Results and Interpretation

1. **Scorecard 1: KS = 0.2080**
   - **Interpretation**: A KS statistic of 20.80% indicates good discrimination ability. This value suggests that the model can effectively differentiate between the classes, identifying potential defaults with reasonable accuracy. A value above 20% is typically considered good in many financial applications.

2. **Scorecard 2: KS = 0.0386**
   - **Interpretation**: A very low KS statistic of 3.86% suggests poor discriminatory power. This model struggles significantly to differentiate between the positive and negative classes, almost approaching random guessing. This is indicative of a model that may not be useful for practical decision-making without substantial improvement.

3. **Scorecard 3: KS = 0.4042**
   - **Interpretation**: An exceptionally high KS statistic of 40.42% shows excellent discrimination capability. This scorecard is highly effective at distinguishing between the two classes, making it potentially very reliable for predicting outcomes. Such a high value is indicative of a strong model, although it's also prudent to ensure it's not overfitting.

4. **Scorecard 4: KS = 0.0375**
   - **Interpretation**: Similar to Scorecard 2, a KS statistic of 3.75% is extremely low, indicating that the model performs only slightly better than random guessing at separating the classes. This model likely requires a complete overhaul or reconsideration of the approach used.

## Usage

To run the analysis, open the Jupyter Notebook `scorecard_analysis.ipynb` and execute the cells sequentially. Ensure that the datasets are placed in the `data/` directory and the necessary Python packages are installed.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any improvements or suggestions.
