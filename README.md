# actuary-salary-prediction
Machine learning model to predict actuary salaries using Python and scikit-learn

## Project Overview
This project builds an end-to-end machine learning model to predict actuary salaries using demographic, educational, and job-related features.

## Problem Statement
Actuary salaries vary depending on several factors such as:
- Industry
- Education level
- Years of experience
- Job role and location

Can we predict an actuary’s salary using observable characteristics

## Skills & Concepts Demonstrated
- Data cleaning and preprocessing  
- Handling missing data correctly  
- Exploratory Data Analysis (EDA)  
- Feature engineering  
- Machine learning pipelines  
- Model comparison and evaluation  
- Reproducible research practices

## Key Findings & Insights
 1.Salary grows monotonically with actuarial exam credentials across all four industry sectors, confirming the premium placed on professional qualification in the actuarial labour market.
 
2.The Pension sector exhibited the widest salary range, while the Health sector showed the most compressed distribution — suggesting Pension roles command higher pay variability based on seniority and specialism.

3.Years of experience has a consistent positive impact on salary_mid, with the steepest gains occurring in the first ten years before plateauing.

4.The near-deterministic relationship between salary_low, salary_mid, and salary_high is structurally inherent to the dataset. This simplifies the prediction task considerably but underscores the need for a robustness-testing exercise using features-only models.

5.The Linear Regression model outperformed all regularised and ensemble alternatives, reinforcing that the underlying data-generating process is well-described by a linear function.

 ## Limitations & Risks
1.Small sample size: With only 138 records, the model may not generalise to salary survey data from different years or geographic regions without retraining.

2.Feature dependency: The inclusion of salary_low and salary_high as predictors means the model requires access to partial salary band information — an assumption that may not hold in all real-world scenarios.

3.Temporal drift: Actuarial salaries evolve with market conditions. The model should be retrained periodically as new survey data becomes available.

4.Limited feature scope: Variables such as geographic location, employer type (insurer vs. consulting firm), educational background, and Fellowship status were not available in the dataset.

5.Single target: The current model predicts salary_mid only; a multi-output variant targeting salary_low and salary_high simultaneously could be more informative.

## Conclusion
This project successfully delivers a fully operational actuarial salary prediction system, demonstrating the feasibility of applying machine learning to compensation benchmarking in a specialised professional domain. The Linear Regression pipeline, guided by a robust preprocessing architecture, achieved perfect predictive accuracy on the test set — a result underpinned by the structural coherence of the underlying salary survey data.

The interactive prediction widget bridges the gap between the technical model and its business users, enabling compensation professionals to generate salary estimates directly within a Jupyter environment. The documented limitations and forward-looking recommendations provide a clear roadmap for extending the system into a production-grade compensation intelligence platform.

As the actuarial profession continues to evolve, particularly with the growth of data science roles within insurance and risk management, maintaining an accurate and current salary prediction model will be an important tool for talent acquisition, retention, and internal equity — areas where data-driven decision-making has an immediate and measurable impact.
