# Drug_Recommendation_Model
Classification Drug Recommendation Model exploration between two drugs based on patient data which included age, blood pressure, cholesterol, and Na/K.

Two drugs (Drug Q, aka 0 and Drug Z, aka 1)are administered to patients. The dataset metadata includes the patient's age, blood pressure, cholesterol, and NA/K ratio.  Data science strategies (EDA and 3 models) are employed to help doctors recommend the best type of drug treatment for at-risk patients. Models tested in this dataset include a Decision Tree Classifier, Logistic Regression, and KN nearest neighbors classifier.


![Drug correlations](https://github.com/khixson1/Drug_Recommendation_Model/assets/8357088/572186ae-d45a-4ecd-a137-4fafe4982888)
**Exploratory Visual 1: Correlation Heatmap**
1. This heatmap shows that 'drugZ' is most highly correlated with low-normal blood pressure, and high Na/K ratios. Drug Z was also given more to younger people.  
2. This heatmap also shows that 'drugQ' however is given to more older patients with high cholesterol and high blood pressure.
3. One can conclude from this heatmap that patients with low or normal blood pressure or who have high sodium to potassium blood ratio are most often given drugZ while patients with high blood pressure and low Na/K ratios are most often given drugQ




![Decision_Tree_Confusion_Matrix](https://github.com/khixson1/Drug_Recommendation_Model/assets/8357088/7222d07b-89cd-4e96-b0bb-79e01dca6521)
![Logistic_Regression_Confusion_Matrix](https://github.com/khixson1/Drug_Recommendation_Model/assets/8357088/2b46ce99-c9d3-4444-a1cd-d532817587cc)
![KNN_Confusion_Matrix](https://github.com/khixson1/Drug_Recommendation_Model/assets/8357088/6fcfd667-ccfa-478a-badb-31d5969d4db2)
![ROC Plot](https://github.com/khixson1/Drug_Recommendation_Model/assets/8357088/f21fcd76-82b3-4845-9d0e-2d405502a494)

Our exploratory data and our confusion matricies on all three models revealed that drugQ was only ever given to people with low Na/K ratios and who have high blood pressure.  It seems there is something critical about this combination that suggests that giving drugZ to someone with high blood pressure combined with a low Na/K would be harmful or ineffective. We don't know the consequence of giving one drug or the other to any given population.


All models performed similarly where the training data was overfit and despite trying to tune hyperparameters, in Logistical Regression and Deciscion Tree models, we could not improve the default model. KNN Classifier model could only be slightly improved from the default but still could not outperform the other two models in terms of accuracy.


The Decision Tree Classifier Model also had the highest level of Sensitivity because it produced the least number of false negatives. Tuning the model to increase Sensitivity would be good. It is difficult to know if tuning the model in such a way would produce false positives and if those false positives would be a detrimental event.

The Decision Tree Classification Model (w/ default hyperparameters), of the models tested was the best choice for determining which drug should be administered to specific patients. This choice is based on superior accuracy, sensitivity, and AUC ROC values.
