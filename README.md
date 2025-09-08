# UCI Human Activity Recognition Classification

## Project Overview
Advanced machine learning system for classifying human activities using smartphone sensor data. Implements comprehensive feature engineering and hyperparameter optimization to achieve 95.7% accuracy on 6-class activity recognition.

## Dataset & Problem
- **Source**: UCI Machine Learning Repository - Human Activity Recognition Using Smartphones
- **Activities**: Walking, Walking Upstairs, Walking Downstairs, Sitting, Standing, Laying
- **Data**: 7,352 training samples, 2,947 test samples, 561 sensor features
- **Challenge**: Multi-class classification with high-dimensional sensor data

## Methodology

### Data Processing & Feature Engineering
- Comprehensive data cleaning with duplicate feature handling
- Statistical feature selection using ANOVA F-tests
- Correlation-based feature reduction (95% threshold)
- Multiple feature set creation: All features (561), Mean/Std (66), Optimized sets (25-53 features)

### Model Development
- **Algorithms**: Random Forest and XGBoost with extensive comparison
- **Optimization**: Two-stage hyperparameter tuning (RandomizedSearch + GridSearch)
- **Validation**: 5-fold stratified cross-validation for robust performance estimation
- **Evaluation**: Accuracy, F1-macro, and custom efficiency metrics

## Key Results

| Feature Set | Features | Test Accuracy | F1-Macro | Efficiency Score |
|-------------|----------|---------------|----------|------------------|
| All Features | 561 | 95.7% | 95.7% | 1.63 |
| Research Baseline | 66 | 92.4% | 92.2% | 12.91 |
| XGB Optimized | 54 | 92.0% | 91.9% | 15.66 |
| RF Efficient | 26 | 91.5% | 91.4% | 32.17 |

## Technical Highlights
- **95% Feature Reduction**: Maintained 91.5% accuracy with only 26 features (vs 561 original)
- **Automated Pipeline**: Systematic feature selection and model optimization
- **Production Ready**: Sub-10ms inference time with comprehensive evaluation framework

## Project Structure

- Initial_Data/              (Original UCI HAR dataset)
- Jupyter_Notebooks/         (4 analysis notebooks)
- Processed_Data/            (Feature-engineered datasets)
- Final_Feature_Sets/        (Optimized feature combinations)

## Technologies Used
Python, Pandas, Scikit-learn, XGBoost, Matplotlib, Seaborn, Plotly

## Key Insights
This project demonstrates that intelligent feature engineering can achieve strong performance with dramatically reduced computational requirements, making the solution practical for real-time mobile applications while maintaining over 91% accuracy with 95% fewer features.
