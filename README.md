# Texas-Traffic-Accident-Duration-Prediction
In this project, we aimed to predict the duration of traffic delays following an accident in the state of Texas using various machine learning techniques. 


### Description:
The dataset consisted of **38,000 rows** from Texas, extracted from a larger dataset of **US accidents (2016 - 2023)**, which included variables related to **geography**, **weather**, and **road conditions**.

### Key Steps:
1. **Natural Language Processing (NLP)**:
   - We processed the description field to obtain a **usefulness score**, which improved the predictive power of our models. Factors like **length**, **key traffic-related terms**, and **clarity** (unique words) were considered to score descriptions.

2. **Data Exploration**:
   - We explored accident timing, weather conditions, and geographic data. Notably, **10% of accidents occurred near crossings**, and **30% occurred near traffic signals**. Variables such as population per city and per capita incident rates were also analyzed.

3. **Modeling Approaches**:
   - **Random Forest & Bagging**: Achieved a test RMSE of **23.20** minutes.
   - **XGBoost**: After grid search and hyperparameter tuning, RMSE was **27.06** minutes.
   - **Decision Tree**: Pruned decision tree model achieved a test RMSE of **22.93** minutes.
   - **BART Regression**: Best out-of-sample RMSE was **15.53** minutes after capping duration at 90 minutes.
   - **Clustering**: Analyzed clusters of accidents using elbow plots and silhouette scores for insights on accident types and patterns.

4. **Key Findings**:
   - **NLP scores** from accident descriptions significantly improved model predictions.
   - **Weather conditions, distance, and time of day** were critical predictors for traffic delay duration.
   - Peak traffic hours saw higher accident frequencies, leading to longer delays.

### Best Model:
The best-performing model was **Bagging**, with an RMSE of **20.38** minutes, showing strong predictive accuracy for traffic delay durations.

This project demonstrates the use of advanced machine learning techniques, including NLP, to enhance predictive modeling in real-world traffic scenarios.
