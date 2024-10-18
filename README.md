# Columbia University Bootcamp Project 4

<h2>Healthcare - Diabetes Risk Prediction</h2>
<p>
  This healthcare related project utilizes machine learning to predict whethere a patient is at risk of diabetes based on various health indicators.
</p>
<p>
  The predictions made using the model do not replace a true diagnosis made by a healthcare professional.  Predictions made using the model are just to illustrate the skill of developing a machine learning model using responses of patients based on their age, gender, and risk factors.
</p>
<p>
  The dataset used for the analysis was found using Kaggle.com and is located within the Resources folder of this hub.
</p>
<p>
  Name of Dataset:  <b>diabetes_risk_prediction_dataset</b>
</p>
<p>
  <b>Since the notebook of the coding for this project was done through Google Colab, the dataset must be uploaded to the drive within the code file first.</b>
</p>

<h2>Project Overview</h2>
<ul>
  <li>Clean the dataset to use for analysis</li>
  <li>Train a machine learning algorithm to predict the risk of diabetes using a:</li>
    <ul>
      <li>logistic regression model</li>
      <li>neural network model</li>
    </ul>
  <li>Create analysis for each model using accuracy scores, classification report, or confusion matrix</li>
</ul>

<h2>Abstract</h2>
<p>Type 1 diabetes is a chronic autoimmune condition where the body’s immune system attacks and destroys insulin-producing beta cells in the pancreas, leading to elevated blood sugar levels. Unlike type 2 diabetes, which is often linked to lifestyle factors, type 1 diabetes typically develops during childhood or adolescence and requires lifelong management through insulin therapy.  Early diagnosis and effective risk prediction are crucial in mitigating complications such as heart disease, kidney failure, and nerve damage.</p>
<p>In this project, we aim to predict the risk of an individual developing diabetes using machine learning models trained on health data. The dataset includes various symptoms and health metrics such as age, gender, polyuria (frequent urination), polydipsia (excessive thirst), sudden weight loss, weakness, polyphagia (excessive hunger), genital thrush (yeast infection), visual blurring, itching, irritability, delayed wound healing, muscle stiffness, alopecia (hair loss), and obesity. By analyzing the relationships between these symptoms and the likelihood of diabetes, our model will provide a tool for early detection and intervention, improving patient outcomes through timely medical attention.</p>
<p>This predictive model offers healthcare professionals a valuable resource in identifying high-risk individuals for further diagnostic testing, promoting early diagnosis and management of diabetes.</p>

<h2>Ethical Considerations</h2>
<p>Several ethical considerations must be considered when developing and using machine learning models to predict the risk of diabetes or any health-related condition.</p>
<p>Data Privacy and Security have become huge concerns as technology advances. Health data is sensitive, and protecting patient information is crucial. Ensuring compliance with data protection regulations like HIPAA is essential. Strong encryption and security protocols must be employed to prevent unauthorized access to medical records and personal information.</p>
<p>Issues such as algorithm bias are important to note. Machine learning models can perpetuate biases if trained on data that is unrepresentative or skewed. It is important to ensure the training data is diverse and accounts for different demographics to avoid biased predictions that may disproportionately impact certain groups.  This tool would be great for predicting the risk of a patient having diabetes, but it is important for patients to understand that the tool may generate false predictions. This tool should be used as a possible insight; however, for diagnosis, if a person has diabetes, they should consult their medical doctor. </p>
<p>The tool may be confusing to some, but patients and healthcare providers must be educated on how to interpret the model's results appropriately. Providing clear guidance on what the risk scores mean and how to act upon them is necessary to ensure everything is clear.</p>
<p>While predictive modeling for diabetes has the potential to greatly improve early diagnosis and intervention, it must be implemented with a clear understanding of these ethical considerations to ensure fairness, accuracy, and respect for patient rights.</p>

<h2>Dataset Analysis</h2>
<p>The diabetes_risk_prediction dataset takes the responses of people of different ages and gender based on what symptoms they have been experiencing that are associated with diabetes, and if that person was positive or negative in terms of the diagnosis of the condition.  Based on this data, each of the risk symptoms, along with the gender and age of the patient has shown different results for a diagnosis of diabetes.  Not all of the symptoms are reported equally since they do not all lead to the conclusion that one may have diabetes.</p>
<p>The following bar graph, <i>Prevalence of Diabetes Symptoms</i>, shows the occurance of these symptoms in the diagnosis of diabetes.</p>
<p align = "center">
  <img src ="./ReadMe_Images/Prevalence_Diabetes_Symptoms.png" alt = "Prevalence of Diabetes Symptoms" width ="800">
</p>
<p>Based on the bar graph, the listed symptoms have all been shown to be present when a positive diagnosis of diabetes was made, but this does not mean that each symptoms, or condition, occurs for the majority of diabetes diagnoses.  Polyuria, muscle weakness, and itching are just some of the top conditions reported by people that ended up having a positive diagnosis for diabetes.  It is important to note the difference between Type 1 and Type 2 Diabetes when understanding why certain symptoms have not been reported as much as others.  For example, obesity is known to be a risk factor that can potentially lead to poor sugar control and even heart conditions, but this dataset is showing that obesity is the least prevalent condition that can be used to diagnosis someone with diabetes.  Since the dataset examined the prevalence of these symptoms in a positive diagnosis of Type 1 Diabetes, that could be the reason for the high prevalence of the other symptoms.</p>
<p>Polyuria, sudden weight loss, and delayed healing are the diabetes symptoms that are analyzed with the following histograms.  Each of the histograms shows the amount of people in the dataset that have reported to have and not to have that respective condition while having a positive diagnosis for diabetes.  Age has been used as the measure that separates each patient, which allows visualizations that illustrate how age may effect the count of people with these symptoms and what age ranges may still have the overall diagnosis.  The purpose of the histograms is to show that even some of the more prevelant symptoms do not have to be present for a person to have diabetes.</p>
<p align = "center">
  <img src ="./ReadMe_Images/Polyuria.png" alt = "Polyuria" width ="500">
  <img src ="./ReadMe_Images/Sudden_Weight_Loss.png" alt = "Sudden_Weight_Loss" width ="500">
  <img src ="./ReadMe_Images/Delayed_Healing.png" alt = "Delayed_Healing" width ="500">
</p>
<p>The histograms illustrate the amount of people that have a positive diagnosis for diabetes and if they reported to have the symptoms that were checked for in the dataset.  With the polyuria histogram, more people have reported to have this condition as they were diagnosed positive for diabetes.  The frequency of people with this symptom has an increase between the ages of 35-47 years and a spike at the age range of about 52-54 years.  Within the same histogram, it is shown that there are a lot of people that did not have this symptom, but they were still diagnosed with diabetes.</p>
<p>When comparing the polyria with the sudden weight loss histograms, they look similar in the sense that there are certain age ranges that have an increase of reporting having the respective symptoms and having a positive diagnosis, and similar frequencies of people that are still positive, but did not experience that symptom.  These similarities can explain the fact that one of the underlying conditions used in the dataset is not enought to guarantee a positive diagnosis of diabetes.</p>
<p>The delayed healing histograms show a balance of people that were reported to have diabetes, but had varying answers as to if they experienced dealyed healing.  The peaks of the delayed histograms do not reach the peaks of the polyuria and sudden weight loss histograms, which shows that not all symptoms are built the same.</p>

<p>The following histogram shows the amount of people in the dataset that have reported struggling with or not experiencing polyuria with a negative diabetes diagnosis.  The purpose of this histogram is to show that the symptoms in the dataset are commonly used to diagnosis a patient with the condition, but they may not be the main factor in the final diagnosis of the condition.</p>
<p align = "center">
<img src ="./ReadMe_Images/Negative_Polyuria.png" alt = "Negative Diabetes with/without Polyuria" width ="600">
</p>
<p>This hi</p>

<h2>Model Analysis</h2>
<h3>Logistic Regression</h3>
<p>When asking to predict if someone could have diabetes, the final result will be one of two responses, positive or negative.  With the various symptoms, age, and gender, a person using any model would only get one of those two predictions.  In this case, a logisitic regression would be a good first model to attempt to predict an accurate diagnosis for diabetes.  The independent variables for this kind of model would be the risk symptoms, age, and gender that each patient would report.  Since they are not affected by anything else in the data, they will be factors that determine the final prediction.  The dependent variable is the diagnosis for diabetes.  Based on the pattern of symptoms, age, and gender these will determine if that person is at risk for acquiring diabetes.  The logisitic regression model is ideal in showing us the actual diagnosis of a person based on the dataset compared the prediction made for that person.  The following dataframe shows a sample of the results created by this logistic regression model: </p>
<p align = "center">
<img src ="./ReadMe_Images/Logistic_Regression_Prediction_VS_Actual.png" alt = "Prediction VS Actual" width ="600">
</p>
<p>This dataframe only shows the initial results of the model, but there are many patients to still go through.  A classification report can help create the calculations for the overall efficiency of the model.  The following classification report shows the results of the predictions created by the logisitc regression model: </p>
<p align = "center">
<img src ="./ReadMe_Images/Classification_Report.png" alt = "Classification Report" width ="600">
</p>
<p>The precision of the model shows the amount of cases that were predicted positive, how many of them were actually positive.  This value goes for a negative diagnosis as well, out of the cases were predicted negative, how many were actually negative.  Based on this classification report, the logistic regression model has a 95% precision for predicting a positive diagnosis and a 94% precision for predicting a negative diagnosis.  These results for precision should be as high as possible, and have a rating of over 90% would be considered very high.  In this case, from all the cases that are predicted as positive, 95% of the predictions were correct, and from all the cases that are predicted as negative, 94% of the predictions were correct.</p>
<p>The recall of the model takes into consideration all the positive cases, and how many were predicted correctly.  This goes for a negative diagnosis as well, it takes into consideration all the negative cases, and how many of predicted to be negative.  The recall value should be as high as possible, with a recall of 96% for a positive diagnosis and a 93% for a negative diagnosis.</p>
<p>Simply put, the F1-score can be explained as the combination of the precision and recall scores.  This value can be used to just have one value to explain how many accurate predictions were made.  If the precision and recall values were smaller it would be a lot harder to compare them, which is why the F1-score can help as a harmonic average by eliminating the extreme values from both.  This score can show how well the model is working, and with a positive diagnosis F1-score of 95% and negative diagnosis F1-score of 93%, the model seems to be running effectively and efficiently.</p>
<p>The accuracy score tells us the ratio of correctly predicted predictions to the total amount of predictions made.  This model is reporting an accuracy score of 95%, so it can be considered effective for its function.</p>
<p>The following visualization is a confusion matrix that shows the instances caught by the model.  Since the model is not 100% accurate, and people should still reach out to a healthcare professional to have a proper diagnosis, there can be some errors in the model.  This confusion matrix is a good visualization because it can evaluate how well the logistic regression model performs by comparing the predicted responses to the actual diagnoses.</p>
<p align = "center">
<img src ="./ReadMe_Images/Confusion_Matrix.png" alt = "Confusion Matrix" width ="450">
</p>
<p>The top left rectangle of the confusion matrix shows the true negative value, which shows the amount of instances the model correctly predicted that are actually negative.  With this model, there are 50 instances that the logistic regression model correctly predicted as negative.</p>
<p>The top right rectangle of the confusion matrix shows the false positive value, which shows the amount of instances the model incorrectly predicted that are actually negative.  With this model, there are 4 instances that the logistic regression model incorrectly predicted as positive.  The bottom left rectangle shows the false negative, which shows the amount of instances the model incorrectly predicted that are actually positive.  With this model, there are 3 instances that the logistic regression model incorrectl predicted as negative.  Both of these false values are low, which shows the effectiveness of the model.  In this case, it is a good thing that the false negative is slightly higher than the false positive.  Giving someone a false positive result will have less consequences than a false negative.  If someone received a false negative result, and it turns out that they have a positive diagnosis after seeing the doctor, that is more life altering than receiving a positive prediction, but the actual diagnosis turns out to be negative.</p>
<p>The bottom right rectangle of the confusion matrix shows the true positive value, which shows the amount of instances the model correctly predicted that are actually positive.  With this model, there are 73 instances that the logistic regression model correctly predicted as positive.</p>

<h3>Neural Network</h3>
<p>A neural network would work well as a model to predict a diabetes diagnosis, however no one knows what a machine is thinking and how it will teach itself.  Even though a neural network is more complicated to implement than a logistic regression, a neural network is good in the sense that it improves its accuracy over time. 
 For this project, three optimized neural networks were created to form the highest accuracy possible.  </p>

<h2>References</h2>
<ul>
  <li>Dataset:  https://www.kaggle.com/datasets/rcratos/diabetes-risk-prediction</li>
</ul>
