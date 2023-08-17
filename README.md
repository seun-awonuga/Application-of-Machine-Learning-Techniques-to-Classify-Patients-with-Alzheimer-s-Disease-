# Application-of-Machine-Learning-Techniques-to-Classify-Patients-with-Alzheimer-s-Disease-
************************

# Project Summary
This research will evaluate the efficiency of supervised and unsupervised learning methods in categorizing patients with Healthy Control (HC) and non-HC diagnosis, which is Alzheimer’s Disease. Four supervised ML algortithms and One unsupervised ML algortihm was used to evaulate the efficiency of the research method

******************

# Dataset Description
- The dataset was acquired by researchers from the Alzheimer’s Disease Neuroimaging Initiative (ADNI). It was based on the studies of Ageing data related to Australian Imaging Biomarkers and Lifestyle
- The dataset was collected for the purpose of applying ML algorithms to effectively categorize three diagnostic results -
  healthy control (HC), mild cognitive impairment (MCI), and Alzheimer’s disease (AD)
- categorization of the three diagnostic results was carried - healthy control  using a patient’s health assessment and medical history available on the dataset
- The dataset was collated as a Microsoft Excel comma separated value (CSV) format. It is in a structured format with dimensions of 862 observations and 32 features
- The first 31 variables are explanatory features while the last column (“diagnosis”) represents the multiclass clinical outcomes

![image](https://github.com/seun-awonuga/Application-of-Machine-Learning-Techniques-to-Classify-Patients-with-Alzheimer-s-Disease-/assets/61943241/54888e78-6f10-4b17-ba76-8f64751a5b9a)

*********************

# Methodology
A. Exploratory Data analysis: - R programming language will be used to conduct exploratory statistical analysis and preprocessing actions 
B. Data Preprocessing:
- The target variable is transformed from a 3-class outcome to a binary class outcome. The diagnosis outcome (class ‘2’ and ‘3’) in the target variable is reclassified as non-healthy control (‘non-HC’) while class = ‘1’ is reclassified as healthy-control (‘HC’). Mode Imputation technique is employed to replace negative data values [7] in categorical columns and the target class (diagnosis), while the mean imputation method was used to replace incorrect values in columns with continuous values

C. Feature Selection
 - In this study, wrapper feature selection approach using Boruta ML algorithm was applied on the dataset to find relevant features affecting diagnosis outcome. Boruta algorithms promise better results in reducing the complexity of medical datasets with large number of variables. The Boruta function is tuned using maxrun = 500 iterations.

D. Class Balancing
 - The Random Up-Sampling (RUS) balancing technique is applied because the ratio of majority (“HC = 0’) and minority (non-HC = 1) class is 66% and 33% respectively

******************

# Data Modelling
- Four supervised ML algortithms (Decision Tree , Logistic Regression, Random Forest, K-nearest Neighbour) was used to evaulate the efficiency of the research method
- One unsupervised ML algortihm (K-means algorithms) was used to evaulate the efficiency of the research method
- The model performance is evaluated with metrics used in mental health analysis like prediction accuracy, confusion matrix, negative prediction value (NPV), and positive prediction value (PPV)

********************

# Results

![image](https://github.com/seun-awonuga/Application-of-Machine-Learning-Techniques-to-Classify-Patients-with-Alzheimer-s-Disease-/assets/61943241/b2c0bc2a-239c-485b-8eb4-a8f13c59b362)
- Also, it was observed in the right section above (distribution plot) that the distribution of patient’s age across each diagnosis type follows a gaussian distribution
- cases of non-HC diagnosis were observed to be prevalent among patients who are above 73 years, and this trend continued until patients reached 80 years.
- Cases of non-HC (Alzheimer disease) experienced a decline among patients who are above 80 years.

---

![image](https://github.com/seun-awonuga/Application-of-Machine-Learning-Techniques-to-Classify-Patients-with-Alzheimer-s-Disease-/assets/61943241/9ca82e23-397d-4ee1-8690-95bf99349982)
- The numbers 1- 4 represent the ratings of the Mini Mental Score Exam. The exam was scored from 0 to 30. The ratings are defined as; 1 = Normal (30-25), 2 = Mild/early (24-21), 3 = Moderate (20-10), and 4 = Severe (9-0)
- it is observed that majority of both male and female patients have a normal mental health rating score, however, there were few cases of both gender groups having patients with mild/early symptoms

---

![image](https://github.com/seun-awonuga/Application-of-Machine-Learning-Techniques-to-Classify-Patients-with-Alzheimer-s-Disease-/assets/61943241/03d7efb9-69c3-461a-a59b-b001d675a320)
- the boxplot shows the decreasing order of importance of each feature linked to the diagnosis outcome
- nine (9) variables were considered important, however considering the boxplot; five features - CDGLOBAL, LDELTOTAL, LIMMTOTAL, MMSCORE and RCT20 will be considered in fitting the classifier model because their importance is significantly greater than other features
