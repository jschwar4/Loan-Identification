# Loan-Identification
1)	Overview of the loan prediction risk analysis:

o	This analysis is designed to predict the riskiness of a loan based on a variety of financial and personal predictors. The risk of a loan is binary, classified as either “low-risk” or “high-risk.”
2)	Results:
o	Random oversampling: 
Balanced accuracy score: 83.38331%
<img width="745" alt="Random_Oversampling" src="https://user-images.githubusercontent.com/90073490/150862261-c2d91d4e-00c5-44a0-8325-23fe8295c606.png">

o	SMOTE oversampling: 
Balanced accuracy score: 83.26435%
<img width="709" alt="SMOTE_Oversampling" src="https://user-images.githubusercontent.com/90073490/150862273-23dcf6bb-31d3-4a2b-bd47-3e36d57b0d89.png">

o	CentroidClusters undersampling: 
Balanced accuracy score: 80.42213%
<img width="713" alt="CentroidClusters_Undersampling" src="https://user-images.githubusercontent.com/90073490/150862283-c44807bb-4226-4ffc-884c-378ae27d6cb9.png">

o	SMOTEENN sampling:  
Balanced accuracy score: 83.7166%
<img width="713" alt="SMOTEENN_Sampling" src="https://user-images.githubusercontent.com/90073490/150862300-9722c105-54fb-4d58-8265-bc0f1a92345f.png">

o	Random Forest model:  
Balanced accuracy score: 68.3051%
<img width="721" alt="Random_Forest_Model" src="https://user-images.githubusercontent.com/90073490/150862311-67f66a51-2d51-4a9f-86dc-f4d9c86bfe03.png">

o	Easy Ensemble model: 
Balanced accuracy score: 92.9311%
<img width="715" alt="Easy_Ensemble_Model" src="https://user-images.githubusercontent.com/90073490/150862324-c6ac346b-7f11-4e5f-801f-7ccdec5515a5.png">

3)	Summary:
o	The models are, generally speaking, atrocious at limiting the identification of bad loans to actually bad loans. The models have an extremely low rate of precision, indicating that they identify far more bad loans than actually exist. That being said, the recall of the models is quite high, indicating that they do catch nearly all true bad loans. 

o	If the goal is to limit the number of high-risk loans given, the Easy Ensemble Model is recommended. The recall rate of .91 indicates that the model correctly identifies 91% of high-risk loans. This would prevent over 9 in 10 bad loans from being made.

o	If the goal is to limit loan denials, then none of these models are correctly recommended. The top model, the Easy Ensemble Model, has a precision rate of .09. The top model marked over 9 times as many loans as high-risk than were in fact high-risk, indicating that many loans were denied than were necessary.  
