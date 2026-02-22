# Why Employees Leave: Data-Driven HR Analytics & Attrition Modeling

## Project Overview

Employee attrition poses a major strategic and financial challenge for organizations. 
High turnover disrupts productivity, increases recruitment costs, and weakens institutional continuity.

This project develops an interpretable machine learning framework to:

- Predict employee attrition probability
- Identify structural and psychosocial drivers of turnover
- Optimize recall for at-risk employee detection
- Provide explainable AI insights using SHAP
- Segment employees into actionable risk tiers

The goal is not only predictive performance, but also transparent and decision-support oriented workforce analytics.

---

## Dataset

The analysis is based on structured HR data containing:

- Demographic attributes (Age, Marital Status, Distance from Home)
- Organizational factors (Job Role, Business Travel, Overtime)
- Career progression metrics (Years Since Last Promotion, Total Working Years)
- Psychosocial indicators (Job Satisfaction, Environment Satisfaction, Work-Life Balance)
- Compensation-related variables (Monthly Income, Stock Option Level)

Target Variable:
- `Attrition` (Yes / No)

---

## Methodology

### 1. Exploratory Data Analysis
- Class distribution analysis
- Correlation inspection
- Feature group comparison (economic, psychosocial, environmental)

### 2. Modeling Approach

This is a supervised binary classification problem.

**Final Model: Logistic Regression**
- Selected for interpretability
- Scaled features using StandardScaler
- Probability-based prediction

### 3. Threshold Optimization

Rather than using the default 0.50 threshold, classification thresholds were evaluated to improve recall performance.

The optimized threshold improved detection of at-risk employees while maintaining balanced precision.

### 4. Model Explainability (SHAP)

To enhance transparency:

- Global SHAP analysis identified dominant attrition drivers
- Individual SHAP waterfall plots explained employee-level risk construction

Key insight:
Structural factors (e.g., overtime, promotion delay, travel frequency) showed stronger influence than purely psychosocial factors, although satisfaction variables acted as protective elements.

### 5. Risk Segmentation

Predicted probabilities were converted into actionable tiers:

- Low Risk (< 0.30)
- Medium Risk (0.30 – 0.60)
- High Risk (≥ 0.60)

Results:
- 84% Low Risk
- 9% Medium Risk
- 7% High Risk

This segmentation enables targeted workforce monitoring instead of broad interventions.

---

## Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Emphasis was placed on recall optimization to better detect potential attrition cases.

---

## Key Findings

- Overtime and frequent business travel significantly increase attrition risk.
- Delayed promotion is a strong structural predictor.
- Job satisfaction and environmental satisfaction reduce risk but are secondary to structural factors.
- Approximately 7% of employees were classified as high risk, forming a manageable intervention segment.

---

## Business Implications

This framework demonstrates how interpretable machine learning can:

- Support proactive retention monitoring
- Provide transparent risk explanations
- Enable targeted workforce prioritization
- Bridge predictive modeling and strategic HR decision-making

---

## Tools & Libraries

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- SHAP

---

## Project Structure
employee-attrition-project/
│
├── hr_attrition_analysis.ipynb
├── README.md
├── hr_attrition_analysis.html
└── requirements.txt


---


---

## Conclusion

This project illustrates how predictive modeling, threshold optimization, explainable AI, and risk segmentation can be integrated into a transparent workforce analytics pipeline.

The approach prioritizes interpretability and operational usability over black-box complexity, making it suitable for real-world HR decision-support systems.

---

## Author

Metin Faruk Us
Public Administration (BA) | Data Science & Machine Learning 
