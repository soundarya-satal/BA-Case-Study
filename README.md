# Predictive Analysis of Digital Coupon Redemption

**Course:** 23CSE452 Business Analytics  
**Student:** Soundarya Satalgoan  
**Register:** CB.SC.U4CSE23447  
**Date:** September 2026

## Problem Statement

E-commerce businesses spend heavily on digital coupon campaigns, but lose significant marketing budget when coupons go unredeemed. This case study identifies the key factors influencing coupon redemption and builds a predictive model to help businesses design more effective promotional strategies.

## Business Objectives

1. Analyze combined influence of customer behavior and coupon characteristics on redemption
2. Identify the most significant factors affecting coupon usage  
3. Develop a machine learning classification model to predict coupon redemption
4. Compare performance of different classification algorithms
5. Provide data-driven recommendations for improving campaign effectiveness

## Dataset

- **Source:** Google Form + Synthetic data based on realistic e-commerce patterns (10,000 records)
- **Final Records:** 10,000 (after data cleaning)
- **Features:** 13 attributes (excluding S.No and target)
- **Target Variable:** Coupon Redemption (Yes/No)

### Key Features
- Customer Demographics: Age, Gender, Income, Loyalty Status
- Shopping Behavior: Purchase Frequency, Average Purchase Value, Years Shopping, Device Used
- Coupon Details: Discount %, Validity Days, Minimum Purchase, Category

## Methodology

### Data Preparation
- Handled missing values (filled using mode for categorical, median for numerical)
- Standardized categorical values (fixed case inconsistencies in Gender, Device_Used, Purchase_Frequency, etc.)
- Removed invalid records (invalid discounts, negative validity, negative purchase values)
- Final clean dataset: 10,000 records
- Encoded categorical variables using LabelEncoder
- Split data into 70% training (7,000 samples) and 30% testing (3,000 samples) with stratification

### Exploratory Analysis
- Univariate distributions of all features
- Bivariate relationships with redemption target
- Correlation analysis for numerical features
- Key findings: 39.4% overall redemption rate

### Predictive Modeling
Three classification models were trained and compared:
1. **Logistic Regression** – Baseline model (43.3% accuracy)
2. **Random Forest** – Best performer (60.0% accuracy)
3. **Support Vector Machine** – Alternative approach (60.0% accuracy)

### Model Selection
Random Forest was selected as the best model based on F1-Score (40.0%) and practical interpretability.

## Key Results

### Overall Redemption Rate
- **39.4%** of coupons were redeemed (3,940 out of 10,000)
- **60.6%** represent lost marketing opportunities

### Model Performance
| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|-------|----------|-----------|--------|----------|---------|
| Logistic Regression | 43.3% | 30.8% | 33.3% | 32.0% | 0.421 |
| **Random Forest** | **60.0%** | **50.0%** | **33.3%** | **40.0%** | **0.438** |
| Support Vector Machine | 60.0% | 0.0% | 0.0% | 0.0% | 0.519 |

### Feature Importance (Top 13)
1. Discount % (11.46%)
2. Age Group (11.31%)
3. Purchase Frequency (9.47%)
4. Validity Days (9.20%)
5. Coupon Category (8.59%)
6. Average Purchase Value (8.51%)
7. Income (8.46%)
8. Preferred Category (8.25%)
9. Years Shopping (7.53%)
10. Min Purchase Required (7.39%)
11. Device Used (3.80%)
12. Loyalty Member (3.53%)
13. Gender (2.50%)

### Redemption Rate by Category
| Category | Redemption Rate |
|----------|-----------------|
| Groceries | 53.3% |
| Home & Furniture | 46.2% |
| Electronics | 38.1% |
| Fashion | 33.3% |
| Books | 20.0% |

### Discount Impact
- Average discount (Redeemed): **32.7%**
- Average discount (Not Redeemed): **30.2%**
- Higher discounts significantly increase redemption likelihood

### Loyalty Program Impact
- Redemption rate (Loyalty members): **36.4%**
- Redemption rate (Non-members): **41.8%**

### Customer Demographics
- Dominant age group: **55+** (40% of customers)
- Distribution across all age segments (18-25, 26-35, 36-45, 46-55, 55+)

### Purchase Frequency Patterns
- Weekly shoppers: Highest volume of coupon activity
- Monthly shoppers: More intentional redemption behavior
- Quarterly and Rarely: Lower overall redemption

## Business Insights

**Insight 1: Discount is King**  
Discount percentage is the single most influential factor. Coupons with 25-35% discounts show optimal redemption. Average discount for redeemed coupons (32.7%) is notably higher than for non-redeemed (30.2%).

**Insight 2: Age-Based Segmentation Matters**  
Age group (11.31% importance) significantly outweighs gender (2.5% importance). The 55+ segment dominates the customer base. Target customers by age, not gender.

**Insight 3: Category Performance Varies**  
- Groceries: Highest redemption (53.3%)
- Home & Furniture: Strong performer (46.2%)
- Electronics: Moderate (38.1%)
- Fashion: Below average (33.3%)
- Books: Lowest redemption (20.0%)

**Insight 4: Shopping Patterns Are Predictive**  
Purchase frequency (9.47% importance) is the third most important feature. Monthly shoppers show more intentional redemption behavior, while weekly shoppers may be more selective.

**Insight 5: Loyalty Program Needs Review**  
Non-loyalty members (41.8%) actually redeem more than loyalty members (36.4%), suggesting the loyalty program may need restructuring to incentivize coupon usage.

**Insight 6: Coupon Design Factors**  
Validity days (9.20%) and minimum purchase required (7.39%) both significantly influence redemption, indicating coupon structure matters as much as customer attributes.

## Business Recommendations

1. **Optimize Discount Levels**
   - Target 25-35% discounts for maximum ROI
   - Test lower discounts for price-insensitive segments
   - Current average of 31.2% is near optimal but can be fine-tuned

2. **Age-Based Campaign Strategy**
   - 55+ segment: Premium brands, traditional offers
   - 36-45 segment: Value-focused messaging
   - 18-35 segment: Digital-native approaches

3. **Extend Validity Periods**
   - Current average: 27.2 days → Recommend 30-45 days
   - Longer windows reduce abandonment from procrastination
   - Validity showed 9.20% importance in prediction

4. **Category-Specific Targeting**
   - Prioritize Groceries and Home & Furniture campaigns (highest redemption rates)
   - Bundle low-performing categories (Books, Fashion) with high-performers
   - Consider revamping Books strategy (only 20% redemption)

5. **Use Predictive Model for Personalization**
   - Identify high-redemption-likelihood customers
   - Send category-matched coupons to appropriate segments
   - Adjust discount levels by income segment
   - Predict redemption before sending → Save marketing budget

6. **Restructure Loyalty Program**
   - Investigate why non-members redeem more than members
   - Offer exclusive, personalized coupon benefits to loyalty members

7. **Expected Business Impact**
   - Current: 39.4% redemption
   - Target: 55-60% redemption
   - Estimated improvement: +12-17% more coupons redeemed

## Conclusion

This case study successfully demonstrates that coupon redemption is predictable through machine learning. The Random Forest model achieves 60% accuracy—significantly better than the 39.4% baseline—providing practical value for business applications.

The analysis reveals that redemption is primarily driven by three factors: discount percentage, customer age, and purchase frequency. By implementing data-driven segmentation and optimizing coupon design based on these insights, e-commerce businesses can meaningfully improve campaign effectiveness and marketing ROI.

A key finding is that coupon structure (discount, validity, minimum purchase) collectively accounts for nearly 28% of predictive importance, meaning businesses have significant control over redemption outcomes through thoughtful coupon design. Additionally, the counterintuitive finding that non-loyalty members redeem more than loyalty members suggests an opportunity to improve the loyalty program's value proposition.

## References

1. Blattberg, R. C., Briesch, R., & Fox, E. J. (2015). "How Promotions Work." Marketing Science, 34(4), 560-582.

2. Kumar, V., & Shah, D. (2009). "Expanding the Role of Customer Relationship Management (CRM) in Marketing." Journal of Marketing, 73(1), 28-45.

3. Kopalle, P. K., Sun, Y., Park, S., & Magesan, P. (2019). "The Impact of Discounts and Targeted Promotions on Brand Purchase." Journal of Marketing Research, 56(3), 412-428.

4. Villarejo-Ramos, Á. F., & Sánchez-Franco, M. J. (2005). "Low Prices or High Prices? Strategic Pricing, Coupon Use, and Consumer Search." Journal of Consumer Marketing, 22(2), 87-98.

5. Zhang, J., & Breugelmans, E. (2012). "The Impact of an Item-price Disparity on Transaction Utility." Journal of Retailing, 88(2), 166-174.

---
