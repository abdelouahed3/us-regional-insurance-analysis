# Does Where You Live Impact Your Insurance Premium Cost?
# Project Overview
A comprehensive data science project analyzing health insurance premiums across US regions and states, combining demographic, health metric, and population data to uncover patterns and build predictive models.

This project integrates multiple public datasets (Census, CDC PLACES, and insurance data) to perform a complete analysis of health insurance charges. It explores regional and state-level variations, identifies key drivers of premium costs, and builds machine learning models to predict insurance charges.

# Key Features
Data Integration: Merges Census population data, CDC health metrics, and insurance records

Regional Analysis: Comparative analysis across 4 US regions (Northeast, Southeast, Northwest, Southwest)

State-Level Insights: Granular analysis of all US states with premium rankings

Statistical Testing: T-tests, ANOVA, correlation analysis, and post-hoc testing

Predictive Modeling: 3 ML models with feature importance and residual analysis

Visualization Suite: Comprehensive plots for distributions, comparisons, and correlations

# 1. Data Processing & Integration
Census data cleaned and reformatted

CDC data filtered for smoking, obesity, and diabetes rates

Weighted random assignment of states based on population

Regional average imputation for missing health metrics

# 2. Exploratory Data Analysis
Regional Metrics Snapshot
| Region | Avg Charge | Smoking Rate | Obesity Rate | Diabetes Rate |
|--------|------------|--------------|--------------|---------------|
| Southeast | $14,643 | 18.5% | 35.2% | 14.3% |
| Northeast | $12,834 | 16.2% | 30.1% | 12.8% |
| Northwest | $11,432 | 14.8% | 29.8% | 11.9% |
| Southwest | $12,056 | 15.9% | 31.4% | 12.5% |

## Model Performance

| Model | R² Score | RMSE | Key Features |
|-------|----------|------|--------------|
| Linear Regression (Baseline) | 0.752 | $6,324 | Age, BMI, Smoker, Children |
| Linear Regression (Enhanced) | 0.768 | $5,987 | + Obesity, Smoking Rate |
| Random Forest | **0.849** | **$4,871** | All features + region |

 ## Data Sources

| Dataset | Source | Year | Variables |
|---------|--------|------|-----------|
| Insurance | Kaggle/US Data | 2020 | Age, Sex, BMI, Smoker, Charges |
| Census | US Census Bureau | 2020 | State, Population |
| CDC PLACES | CDC | 2025 | Smoking, Obesity, Diabetes Rates |

## Statistical Analysis Results

| Test | Purpose | Result |
|------|---------|--------|
| T-Test | Region vs Others | Southeast significantly higher (p<0.001) |
| ANOVA | Across all regions | Significant differences (p<0.001) |
| Dunn's Test | Pairwise comparisons | Multiple significant pairs |
| Correlation | Variable relationships | Smoking (0.72), Age (0.65), BMI (0.43) |

# Key Findings
Southeast has highest average premiums (+22% vs national average)

Smoking is the strongest predictor of high charges

Obesity rate correlates strongly with regional premium differences

State-level variation is significant (range: $8,000 - $18,000)

# Business Insights
Southeast requires targeted premium reduction interventions

Smoking cessation programs could significantly reduce costs

5 states show significant overpricing patterns

Best practices from low-cost states could be adopted

# Author
# Abdelouahed Gmiha

GitHub: @abdelouahed3

LinkedIn: Abdelouahed Gmiha
