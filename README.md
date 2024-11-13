#  A machine learning approach: Generational trends and predictors of hormonal contraceptive use in Germany
Authored by [Theresa Nutz](https://theresanutz.github.io/), [Nora Müller](https://nrmllr.github.io/), and [Hao-Ting Chan](https://www.linkedin.com/in/bryanchan97/)

Also, check out the [project-contraception website](https://projectcontraception.github.io/sp1.html).

## Abstract
The introduction of the contraceptive pill in the 1960s revolutionized women’s reproductive health by providing a convenient and effective method of contraception. This allowed women greater control over their reproductive choices, enabling them to plan families and pursue professional careers. However, in recent years, there has been a decline in the use of hormonal contraception among younger women, as evidenced by cross-sectional data. This decline has coincided with increased public scrutiny of oral contraceptives, which have highlighted a range of potential health risks associated with their use. Our study makes four key contributions. Applying multilevel mixed-effects logistic regression analyses, we first examine whether the decline in hormonal contraceptive use among women is consistent across different birth cohorts or exhibits generational variation. Using two different supervised machine learning models for classification problems, namely Random Forest and XGBoost, we second analyze how well a broad set of 25 potential independent variables can predict the use of hormonal contraception across three different birth cohorts. Third, we identify the key predictors among this set of 25 potential independent variables of hormonal contraceptive use and analyze how they change across cohorts. Fourth, we interpret the prediction patterns, including non-linearities and two-way interactions and their differences across cohorts. We carry out our analyses with data from the Panel Analysis of Intimate Relationships and Family Dynamics (pairfam) for Germany, where hormonal contraception rates among women have been traditionally very high in international comparison.

### Key Contributions
- Examine generational variation in hormonal contraceptive use across birth cohorts.
- Analyze the predictive power of 25 variables on hormonal contraceptive use using Random Forest and XGBoost models.
- Identify key predictors across cohorts and interpret prediction patterns, including non-linearities and interactions.
- Analyze data from the pairfam (Panel Analysis of Intimate Relationships and Family Dynamics) study.

## Data Source
This study utilizes data from the [pairfam](https://www.pairfam.de/en/data/) (Panel Analysis of Intimate Relationships and Family Dynamics) for Germany.

## Machine Learning Models
This project will compare the performance of Decision Tree, Random Forest, and XGBoost models to determine which approach is most effective for predicting hormonal contraceptive use. The final results and metrics will be documented in the full report.

A preliminary comparison of our Random Forest and XGBoost model on the Validation set shows us that the Random Forest model performs better.
![Model Performance on Validation Set](model_comparison_CVset.png)

We employed a custom **Recursive Feature Elimination** (RFE) step to narrow-down the top most relevant predictors based on F-score and the ROC-AUC metric.
<table>
  <tr>
    <td><img src="RFE_plot_X1.png" alt="RFE Plot - Cohort 1 (Age 27)" style="width: 100%; height: auto;"></td>
    <td><img src="RFE_plot_X2.png" alt="RFE Plot - Cohort 2 (Age 27)" style="width: 100%; height: auto;"></td>
  </tr>
  <tr>
    <td><img src="RFE_plot_X3.png" alt="RFE Plot - Cohort 2 (Age 37)" style="width: 100%; height: auto;"></td>
    <td><img src="RFE_plot_X4.png" alt="RFE Plot - Cohort 3 (Age 37)" style="width: 100%; height: auto;"></td>
  </tr>
</table>

## Results
- We observed a 'period differences', with a shift from **family-demographic** to **personality** factors throughout the 2010s
- We also observed variations of key predictors among cohorts in the same survey years: cohort differences
<table>
  <tr>
    <td><img src="plot_SHAP_beeswarm_coh1_27.png" alt="SHAP Beeswarm Plot - Cohort 1 (Age 27)" style="width: 100%; height: auto;"></td>
    <td><img src="plot_SHAP_beeswarm_coh2_27.png" alt="SHAP Beeswarm Plot - Cohort 2 (Age 27)" style="width: 100%; height: auto;"></td>
  </tr>
  <tr>
    <td><img src="plot_SHAP_beeswarm_coh2_37.png" alt="SHAP Beeswarm Plot - Cohort 2 (Age 37)" style="width: 100%; height: auto;"></td>
    <td><img src="plot_SHAP_beeswarm_coh3_37.png" alt="SHAP Beeswarm Plot - Cohort 3 (Age 37)" style="width: 100%; height: auto;"></td>
  </tr>
</table>

