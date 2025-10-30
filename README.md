# Predicting Muscle Injuries in Professional Soccer Teams  
To view the full project report please navigate to my GitHub Pages site at maxaclark.github.io and then select this [link](PredictingMuscleInjuriesInProSoccer.html) which takes you to the rendered HTML file.
 
The goal of this project is to predict the number of muscle injuries a professional soccer club will experience over the course of a season. The aim is to perform EDA for the purpose of feature selection, followed by training and tuning of the selected models. The 2 best performing models will then be applied to the testing set for final evaluations.

---

## Objectives  

- Analyze feature relationships and trends to aid in final feature selection
- Build and train models of varying levels of flexibility
- Tune the model hyperparameters to maximize validation performance
- Apply the best performing models to the testing set and evaluate for real-world application

---

## Repository Structure
```
```

## Methodology

### Dataset
- Manually sourced from transfermarkt.com: 116 observations in total from the Premier League, La Liga, and the Bundesliga
- Columns: `club`, `sqsize`, `sqval`, `sqage`, `ltinj`, `league`, `year`, and `match`
- Target: `musc` (continuous)

### Workflow
1. **EDA**: Variable correlation and distribution for feature selection
2. **Preprocessing and Data Split**: Center and scaling of relevant features and stratified splits into training, testing, and validation sets
3. **Modeling**:
   - KNN
   - Linear Regression
   - Elastic Net
   - Random Forest
   - Gradient-Boosted Tree
   - Polynomial Regression
4. **Testing and Evaluation**: RMSE used for testing metric

---

## Key Visualizations


---

## Validation Performance Summary

| Model                  | RMSE  |
|------------------------|-------|
| Gradient-Boosted Tree  | 4.84  |
| Random Forest          | 5.21  |
| Polynomial Regression  | 5.25  |
| KNN                    | 5.30  |
| Elastic Net            | 5.38  |
| Linear Regression      | 5.49  |

### Key Insights

- **Gradient-Boosted Tree** and **Random Forest** performed the best with regards to RMSE, likely due to their high complexity - Awareness should be raised for overfitting
- **Linear Regression** and **Elastic Net** performed the worst, indicating that the predictor-response relationship is likely non-linear
- High model complexity generally led to better results

---

## Testing Performance Summary

| Model                  | RMSE  |
|------------------------|-------|
| Gradient-Boosted Tree  | 5.06  |
| Random Forest          | 6.00  |

### Key Insights

- Testing performance wildly differed for **Random Forest**, confirming suspicion of overfitting
- **Gradient-Boosted Tree** testing performance was higher, but more comparable to validation performance - overfitting was less severe
- Data improvements required to improve viability in real-world applications

---

## Future Improvements

- Utilize webscraping to increase dataset size
- Acquire next-gen statistics such as average distance traveled per match or average running speed per match
- Investigate player-specific injury prediction on top of club-specific injury prediction





