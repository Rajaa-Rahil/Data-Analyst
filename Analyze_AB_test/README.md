## A/B Test Analysis for E-commerce Website Conversion Rates 

## Project Overview

In this project a dataset containing the conversion rates between new and old websites for an e-commerce website is going to be analyzed. The data will be used to perform an A/B test, the goal is to help the community understand if they should implement the new page, keep the old one or run the experiment longer to make their decision.
The analysis employs statistical methods including hypothesis testing, simulation, and logistic regression to provide data-driven recommendations.

## Project Structure

### Part I: Probability Analysis

#### Data Exploration and Cleaning

- The original dataset contains 294,478 rows, 290,584 of them unique users, and 11.97% overall conversion rate in original data.
- 3,893 mismatched records, where treatment/control groups didn't align with corresponding pages, have been removed.
- Duplicate user_id has been processed.

### Part II: A/B Hypothesis Testing

#### Hypotheses Formulation
- **H₀**: μ_new - μ_old ≤ 0 (new page is not better than or equal to old page)
- **H₁**: μ_new - μ_old > 0 (new page performs better than old page)

#### Methodology
- Simulated 10,000 iterations under null hypothesis using bootstrap sampling.
- Calculated p-value using both simulation and z-test for proportions.
- Significance level: α = 0.05.

#### Results
- **p-value (simulation)**: 0.90
- **p-value (z-test)**: 0.905
- **z-score**: 1.312
- **Critical value (95% confidence)**: 1.645

#### Conclusion
- Fail to reject null hypothesis at α = 0.05.
- No statistical evidence that new page improves conversions.
- The old page remains the better option based on current data.

### Part III: Regression Analysis

#### Models Implemented
1. **Basic Logistic Regression**: Conversion ~ Page Type.
2. **Extended Model**: Added country data (US, UK, CA) and interaction terms.

#### Results
- **Page type coefficient**: Not statistically significant (p = 0.190).
- **Country variables**: No significant impact on conversion rates.
- **Interaction terms**: No significant effects detected.
- Regression analysis confirms A/B test findings.

### Conclusions

### Statistical Findings
1. **No Significant Improvement**: The new landing page does not demonstrate statistically significant improvement in conversion rates.
2. **Consistent Results**: Both hypothesis testing and regression analysis yield the same conclusion.
3. **Data Quality**: Analysis accounts for data inconsistencies and validates results through multiple methods.

### Business Recommendations
Based on the statistical analysis, the company should:

- **Continue using the existing old page**
- Consider extending testing period if further validation is desired.
- Explore alternative optimization strategies beyond page design.
- Focus resources on other initiatives to improve conversion rate.

## Technical Implementation

### Tools & Technologies
- **Programming Language**: Python.
- **Libraries**: pandas, numpy, statsmodels, matplotlib, scipy.
- **Environment**: Jupyter Notebook.

### Statistical Methods
- Hypothesis testing.
- Bootstrap sampling.
- Logistic regression.
- Z-test for proportions.
- Data visualization and validation.

### Data Validation
- Comprehensive data cleaning and integrity checks.
- Handling of duplicate entries.
- Verification of treatment-control group alignment.
- Multiple validation methods for robustness.

## Future Considerations

- Longer testing period to caputre potential long-term impacts.
- Segmentation analysis based on demographics or user behavior.
- Multivariate testing of specific page elements.
- Consider seasonal effects on conversion rates.

## Note:

This project was submitted  as part of the Data Analyst Nanodegree Program at [Udacity](https://www.udacity.com/course/data-analyst-nanodegree--nd002).
