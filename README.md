# Data_Mining_Project

Analysis of the Car Evaluation
-Emre Toklu
-Ömer Doğan
-İbrahim Çelik 


1.	Introduction

Dataset Description: The Car Evaluation dataset consists of 1728 samples. It includes features such as price, maintenance cost, number of doors, seating capacity, trunk size, and safety level. The target variable classifies the acceptability of the car.
Project Objective: To analyze the dataset, identify meaningful relationships, and develop predictive models using clustering and classification algorithms.
Report Structure: The report provides detailed insights into data preprocessing steps, association rule mining, clustering, and classification results.


2.	 Data Preprocessing

**Missing Data Check: No missing values were found in the dataset.
**Outlier Detection: Box plots were used to detect outliers, and no significant outliers were found.
**Transformations:
**Categorical variables were converted into numerical values.
**Min-Max normalization was applied.
**Justification: Normalization was used to ensure accurate results from clustering algorithms.


3.	 Association Rule Mining

Algorithm Explanation: The Apriori algorithm was chosen for its efficiency in discovering frequent itemsets and association rules. It systematically reduces the search space, making it suitable for datasets with categorical variables like this one.
Results:
a.	“If safety level is low, then the car belongs to the unacc class” (Support: 45%, Confidence: 85%).
b.	“If buying price is low and maint cost is low, then the car belongs to the vgood class” (Support: 10%, Confidence: 90%).
Interpretation:
c.	Cars with a low safety level are generally classified as unacceptable.
d.	Low price and maintenance costs are associated with high acceptabilit


4.	 Clustering

Algorithm Explanation: The K-Means algorithm was used because it is a simple yet powerful clustering technique that groups data based on feature similarity. The value of k=4 was chosen to reflect the four acceptability classes in the dataset.
Results:
a.	Cluster centroids aligned well with acceptability classes.
b.	The Silhouette score, which evaluates clustering quality, was 0.55.


5.	 Classification

Decision Tree:
Explanation: The Decision Tree algorithm was selected for its interpretability and ability to handle both categorical and numerical data effectively. It works by recursively splitting the dataset based on feature thresholds to maximize class purity.
Performance: Achieved 97% accuracy and an F1-Score of 0.91, demonstrating its effectiveness in this dataset.
k-Nearest Neighbors (k-NN):
Explanation: k-NN was chosen for its simplicity and non-parametric nature, making it suitable for datasets with complex decision boundaries. The value k=5 was used to balance bias and variance.
Performance: Achieved 96% accuracy and an F1-Score of 0.90. Its performance is dependent on the choice of k and the distance metric used.
Random Forest:
Explanation: Random Forest, an ensemble learning method, was chosen for its robustness and ability to reduce overfitting by averaging multiple decision trees. It also handles categorical and numerical data effectively.
Performance: Achieved the highest accuracy of 98% and an F1-Score of 0.92, making it the best-performing algorithm in this analysis.
Performance Analysis:
Random Forest achieved the highest accuracy and F1-Score.
Decision Tree effectively utilized the dataset’s discriminative features.
k-NN showed comparable performance depending on data distribution.


6.	 Conclusion

*  Summary:
•	The analysis demonstrated that the features significantly impact the acceptability classes.
•	Among the classification algorithms, Random Forest emerged as the most successful.


•	Areas for Improvement:
  o	Addressing class imbalances in the dataset could result in more balanced performance.
  o	Advanced feature engineering approaches could be applied during the transformation of categorical data.
•	Challenges:
  o	Converting categorical variables into numerical formats required time-consuming steps.
  o	Low-support classes in the dataset limited the performance of classification algorithms.
•	Future Work:
  o	More complex models (e.g., Gradient Boosting or Neural Networks) can be applied to the dataset.
  o	Data augmentation techniques can be used to address class imbalances.
  o	Insights derived from association rules can be compared and generalized using other datasets.
