# Airbnb Boston Price Prediction

This project presents a comprehensive machine learning pipeline for predicting Airbnb listing prices in Boston. The notebook combines detailed exploratory analysis, sophisticated feature engineering, and cutting-edge modeling techniques, including ensemble methods, to deliver accurate price predictions.

---

## Table of Contents
1. Introduction  
2. Data Exploration  
3. Data Preprocessing  
4. Advanced Feature Engineering  
5. Model Building & Evaluation  
    - Baseline Models  
    - Ensemble Techniques  
6. Feature Importance  
7. Error Diagnostics  
8. Review Sentiment Analysis  
9. Conclusions & Recommendations  

---

## Project Overview

The rise of Airbnb has transformed the hospitality space, making it essential for hosts and analysts to understand what drives listing prices. This project uses a rich dataset that includes property features, host information, reviews, and amenities to develop a powerful predictive model.

The primary objective is to build a high-performing model using R-squared and RMSE as evaluation metrics. The project utilizes ensemble modeling and complex feature engineering to better capture the nuances influencing Airbnb pricing.

---

## Data Exploration & Cleaning

- The dataset includes structured (numerical, categorical) and unstructured (text) data.
- Missing values were treated using deletion and imputation techniques.
- Outliers in pricing were smoothed using winsorization.
- Notable skew in price distributions, with long tails in high-price listings.

---

## Feature Engineering Highlights

- **Location Features:** Distance to city center, neighborhood pricing stats, density metrics.
- **Property Features:** Price per room/bath, space efficiency, room and property types.
- **Host Metrics:** Response rate, verification status, experience, superhost flag.
- **Review Features:** Frequency, quality scores, recency, sentiment approximation.
- **Amenities & Text:** Amenity category scores, keyword richness, description complexity.
- **Interaction Terms:** Cross-features like accommodates × bedrooms, and polynomial variables.

---

## Model Development & Evaluation

### Baseline Models
- Random Forest, Gradient Boosting, XGBoost, LightGBM
- Ridge, Lasso, ElasticNet
- SVR, Huber Regression

### Ensemble Techniques
- **Voting:** Majority/average predictions from multiple models.
- **Stacking:** Meta-model built on base model predictions.
- **Blending:** Similar to stacking with a validation holdout.

**Result:** Ensemble models (especially stacking/blending) outperformed all baselines in R² and RMSE scores.

---

## Feature Importance Insights

Top predictors:
- Location-related features
- Number of reviews
- Host experience and listing count
- Review quality and sentiment
- Room type and amenity richness

---

## Error Analysis

- Most predictions clustered near actual values with balanced residuals.
- Larger prediction errors observed in rare or outlier listings.
- Residual plots used to detect variance shifts and bias.

---

## Review & Sentiment Analysis

- Applied NLP to extract sentiment scores from textual reviews.
- Generated word clouds to highlight commonly mentioned keywords.
- These qualitative signals were quantitatively integrated into the model.

---

## Conclusions & Recommendations

### Key Takeaways:
- Location, review quality, and host attributes are pivotal in price prediction.
- Text-based and interaction features significantly improve model performance.
- Ensemble methods are ideal for capturing non-linear patterns in pricing.

### Applications:
- Hosts can adjust pricing to maximize revenue.
- Travelers can identify listings offering better value.
- Analysts and platforms can detect pricing trends and market shifts.

### Future Work:
- Incorporate geolocation APIs for enhanced spatial features.
- Deploy as a pricing recommendation web app.
- Extend methodology to other cities or rental markets.

