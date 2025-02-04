# **State Revenue Analysis: New Jersey & California**
---

## **Overview**
This project analyzes quarterly financial and tax-related metrics for New Jersey and California from 1997 to 2023. The primary goal is to examine the impact of economic indicators on state revenue using exploratory data analysis, correlation analysis, regression models, and ARIMA time-series forecasting.

## **Dataset**
- **State Revenue** (Target variable)
- **Year, Quarter** (Time features)
- **AvgTaxRate, TaxRateRank** (General tax metrics)
- **AvgTaxRateOnWages, AvgTaxRateOnWagesRank** (Tax rate on wages)
- **MinTaxWage** (Taxable wage base)
- **TrustFund, TFPerWages, TFWagesRank** (Trust fund balance metrics)
- **Interest** (Trust fund interest earned)
- **HighCostMultiple, AvgHCM, AvgHCMRank** (Economic stability metrics)

## **Exploratory Data Analysis (EDA)**
- **Missing Values Handling:** Rows with NA values were removed.
- **Dataset Size:**
  - **New Jersey:** 85 rows, 15 columns
  - **California:** 106 rows, 15 columns
- **Correlation Analysis:**
  - Identified relationships between tax rates, trust funds, and state revenue.
  - Positive correlation: **AvgTaxRate, TrustFund, and TFPerWages** with **StateRevenue**.
  - Negative correlation: **MinTaxWage** with **StateRevenue**.
- **Skewness Analysis:** Identified positively and negatively skewed features for both states.

## **Modeling Approaches**
### **Linear Regression Models**
- **Model 1:** Baseline model without time variables.
- **Model 2:** Added Year and Quarter as predictors (**best-performing linear regression model**).
- **Model 3:** Applied backward selection for feature optimization.

### **ARIMA Time-Series Models**
- **Model 1:** Simple ARIMA on revenue.
- **Model 2 (ARIMA 0,1,1):** Regression with ARIMA errors, incorporating economic indicators.
- **Model 3 (ARIMA 0,0,1):** Extended to include Year and Quarter variables (**best-performing ARIMA model**).

## **Key Findings**
- **New Jersey:** TrustFund and AvgTaxRate are the strongest predictors.
- **California:** MinTaxWage significantly impacts revenue.
- **Best Models:**
  - **NJ:** Linear Regression Model 2, ARIMA Model 2.
  - **CA:** Linear Regression Model 2, ARIMA Model 1.
- **Policy Implications:** Tax policy changes significantly influence economic growth and state revenue trends.

## **Conclusion**
- Higher tax collection and trust fund balance positively impact state revenue.
- Long-term economic trends are crucial in forecasting revenue changes.
- ARIMA models confirm revenue trends and seasonal patterns over time.

## **References**
- Gale, Krupkin, & Rueben (National Tax Journal, vol. 68(4))
- Bruce, Fox, & Luna (National Tax Journal, vol. 68(3S))
