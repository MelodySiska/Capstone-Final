# Capstone Project: Reducing Left Without Being Seen (LWBS) in a Pediatric Emergency Department

## Project Overview
This project focuses on understanding and reducing the **Left Without Being Seen (LWBS)** rates in a pediatric emergency department. **LWBS** occurs when patients leave the emergency department before receiving medical care, often due to overcrowding, long wait times, or insufficient staffing. 

The primary goal is to analyze the factors contributing to **overcrowding** (measured by the Pediatric Emergency Department Overcrowding Scale - **PEDOCS**) and explore how operational adjustments, especially **staffing**, can help reduce **LWBS** rates.

## Business Understanding
The project aims to help emergency department administrators understand:
1. How **overcrowding** (measured by **PEDOCS > 140 hours**) impacts **LWBS**.
2. How **patient arrivals** and **provider hours** influence overcrowding and LWBS rates.
3. The potential impact of staffing adjustments on **overcrowding** and **LWBS**.

The results provide actionable insights to guide hospital leadership in making data-driven decisions about staffing, patient flow management, and operational changes to reduce LWBS.

---

## Data Overview
The dataset consists of daily logs from the pediatric emergency department, including:
- **LWBS Cnt**: The count of patients who left without being seen.
- **Hrs > 140 PEDOCS**: Number of hours per day where **PEDOCS** exceeded 140, indicating overcrowding.
- **Provider Hours**: Number of hours worked by providers in the emergency department.
- **Arrivals**: The total number of patient arrivals in the emergency department.

---

## Key Analyses and Findings

### 1. Correlation Between PEDOCS and LWBS
- **Key Finding**: A strong positive correlation was found between **PEDOCS > 140 hours** and **LWBS counts**. As overcrowding increases, the number of patients leaving without being seen also increases.
- **Insight**: Reducing overcrowding, especially during hours where PEDOCS exceeds 140, can directly reduce LWBS.

### 2. Feature Importance in Predicting LWBS
- **Key Features**: 
  - **Hrs > 140 PEDOCS**: The most significant predictor, contributing nearly 69% to the predictive model.
  - **Arrivals**: Accounts for 21% of the model's predictive power.
  - **Provider Hours**: Contributes about 9%, indicating that staffing adjustments alone, while helpful, may not be enough to fully mitigate overcrowding.

### 3. Impact of Reducing Overcrowding (PEDOCS > 140) on LWBS
- **Scenario Analysis**: We simulated the effect of reducing **PEDOCS > 140 hours** by 20%, 30%, and 50%.
  - **Result**: Even a 20% reduction in overcrowding showed a noticeable drop in LWBS counts. A 50% reduction almost eliminated overcrowding and led to the lowest LWBS rates.
- **Recommendation**: Reducing overcrowding through better patient flow management, earlier discharge processes, and strategic use of overflow rooms can significantly reduce LWBS.

### 4. Staffing Adjustments and Overcrowding
- **Analysis**: We modeled the impact of increasing **Provider Hours** on **PEDOCS > 140 hours**.
  - **Finding**: A 20-30% increase in provider hours led to a substantial reduction in **PEDOCS > 140 hours**, especially for moderate overcrowding levels.
  - **Recommendation**: Increasing staffing during peak hours can reduce overcrowding, but additional strategies like improving patient flow and bed availability are also needed for extreme overcrowding.

---

## Modeling Overview
We developed multiple regression models to predict **LWBS** counts using key features such as **Provider Hours**, **PEDOCS > 140**, and **Arrivals**.

### Model Performance:
- **Cross-validation R²**: 64.4% — The model explains around 64% of the variance in **LWBS** counts.
- **Best Model**: RandomForestRegressor with optimized hyperparameters via grid search. Feature importance analysis showed that **PEDOCS > 140 hours** is the most critical factor.

---

## Key Recommendations
Based on the analysis, here are the top recommendations for reducing **LWBS** in the pediatric emergency department:
1. **Reduce Overcrowding**: Focus on reducing **PEDOCS > 140 hours** through better patient flow management, earlier discharge processes, and strategic use of overflow areas.
2. **Increase Provider Hours During Peak Times**: A 20-30% increase in provider staffing during peak arrival hours can help reduce overcrowding and thus lower LWBS rates.
3. **Manage Patient Inflows**: Implement policies or interventions that manage the inflow of patients, especially during peak times, to avoid overwhelming the emergency department.

---

## Next Steps
1. **Incorporate More Variables**: To refine the model further, consider including additional operational factors like **bed availability**, **discharge rates**, or **EMS diversions**.
2. **Develop Predictive Tools**: Use the insights from the feature importance analysis to build a real-time predictive tool that can forecast overcrowding and preemptively allocate staff and resources.
3. **Evaluate Additional Interventions**: Beyond staffing, explore other strategies such as improving the triage process, introducing fast-track lanes, and implementing telemedicine for non-urgent cases.

---

## Conclusion
This project highlights the importance of managing **overcrowding** and adjusting **staffing** levels to reduce **LWBS** rates in a pediatric emergency department. By focusing on reducing **PEDOCS > 140 hours** and strategically increasing **provider hours**, hospital leadership can improve patient flow, reduce wait times, and ultimately ensure that fewer patients leave without receiving care.

---

## Repository Structure:
- **Jupyter Notebooks**: Contains all the analysis, data cleaning, modeling, and visualization steps.
- **Data**: The cleaned dataset used in this analysis.
- **README.md**: This document, providing a summary of the project for non-technical readers.
- **Visualizations**: Includes charts and graphs used to support the analysis and recommendations.

---

This concludes the project summary for the Capstone Project on Reducing LWBS in a Pediatric Emergency Department. Please refer to the Jupyter Notebooks for a detailed breakdown of the code, models, and findings.
