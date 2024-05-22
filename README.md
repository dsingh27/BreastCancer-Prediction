# BreastCancer-Prediction


#### Overview
A machine learning classification task to predict whether a breast mass is malignant or benign based on features derived from digitized images of fine needle aspirates (FNA) of breast masses. The goal is to aid in the early detection and diagnosis of breast cancer.

#### Dataset
The dataset includes the following information for each instance:
- **ID Number**: A unique identifier for each sample.
- **Diagnosis**: The target variable indicating the diagnosis ('M' for malignant and 'B' for benign).

For each cell nucleus, ten real-valued features are computed:
1. **Radius**: Mean distance from the center to points on the perimeter.
2. **Texture**: Standard deviation of gray-scale values.
3. **Perimeter**: The perimeter of the nucleus.
4. **Area**: The area of the nucleus.
5. **Smoothness**: Local variation in radius lengths.
6. **Compactness**: (Perimeter² / Area - 1.0).
7. **Concavity**: Severity of concave portions of the contour.
8. **Concave Points**: Number of concave portions.
9. **Symmetry**: Symmetry of the nucleus.
10. **Fractal Dimension**: "Coastline" approximation of the nucleus using fractal geometry.

These features provide quantitative measurements for distinguishing between malignant and benign breast masses.

#### Data Preprocessing
- Dropped unnecessary columns ('Unnamed: 32', 'id').
- Verified that there were no missing values.
- Examined data types and performed statistical descriptions of the columns.

#### Exploratory Data Analysis (EDA)
- **Correlation Analysis**: Identified that features such as perimeter, radius, and area had high correlations with the diagnosis.
- **Visualizations**: Created bar plots to display diagnosis counts and heatmaps to visualize feature correlations.

#### Model Training and Evaluation
Two machine learning models were employed: Decision Tree Classifier and Logistic Regression.

1. **Decision Tree Classifier**:
   - Split data into training and testing sets.
   - Achieved an accuracy of 93.5% on the test set.

2. **Logistic Regression**:
   - Encountered a convergence warning but completed training.
   - Achieved a higher accuracy of 97% on the test set.

#### Model Comparison and Conclusion
- **Accuracy**: Logistic Regression (97%) outperformed the Decision Tree Classifier (93.5%).
- **Recall**: Logistic Regression had a higher recall, making it more reliable for this task.

Based on these results, the logistic regression model is recommended as the superior model for predicting breast cancer diagnosis, offering better accuracy and reliability.
