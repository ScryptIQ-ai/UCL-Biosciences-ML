# Dataset description

## Knowing your dataset

Why is it important to understand the origins of your dataset? While the data points (features) collected in a new sample may theoretically be the same, the hardware used to collect them and the processing methods may differ. To the eye, they could look identical, but there might be subtle changes in the patterns within the data. A model learns the patterns and properties present in whatever data it is trained on, not necessarily the "true" characteristics of the phenomenon being studied. When asked to predict on newly collected data, it might give us incorrect answers, and if we weren't careful we might mistakenly trust these answers, given the model's strong performance on historical data. This phenomenon is called "dataset shift" or "distribution shift," and it's something you should always keep in mind when using someone else's data, or even your own. Reproducibility is key!

## Breast cancer

The dataset is the Wisconsin Breast Cancer Diagnostic Database, publicly available from the [University of California Irvine (UCI) Machine Learning Repository](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic). It consists of characteristics, or features (the machine learning term), of cell nuclei taken from breast masses which were sampled using fine-needle aspiration (FNA), a common diagnostic procedure in oncology. 

The clinical samples used to form this dataset were collected from January 1989 to November 1991. Relevant features were extracted from the digital images using Multisurface Method-Tree (K.P. Bennett 1992). This is a classification method that uses linear programming to construct a decision tree - a form of machine learning! 

The features are observable characteristics of the cells in the images - for example, radius, concavity, and texture. An example of one of the digitised images from an FNA sample is given below.

## Heart attack prediction

### Context
The Heart Attack Risk Prediction Dataset serves as a valuable resource for delving into the intricate dynamics of heart health and its predictors. Heart attacks, or myocardial infarctions, continue to be a significant global health issue, necessitating a deeper comprehension of their precursors and potential mitigating factors. This dataset encapsulates a diverse range of attributes including age, cholesterol levels, blood pressure, smoking habits, exercise patterns, dietary preferences, and more, aiming to elucidate the complex interplay of these variables in determining the likelihood of a heart attack. By employing predictive analytics and machine learning on this dataset, researchers and healthcare professionals can work towards proactive strategies for heart disease prevention and management. The dataset stands as a testament to collective efforts to enhance our understanding of cardiovascular health and pave the way for a healthier future.

### Content
This synthetic dataset provides a comprehensive array of features relevant to heart health and lifestyle choices, encompassing patient-specific details such as age, gender, cholesterol levels, blood pressure, heart rate, and indicators like diabetes, family history, smoking habits, obesity, and alcohol consumption. Additionally, lifestyle factors like exercise hours, dietary habits, stress levels, and sedentary hours are included. Medical aspects comprising previous heart problems, medication usage, and triglyceride levels are considered. Socioeconomic aspects such as income and geographical attributes like country, continent, and hemisphere are incorporated. The dataset, consisting of 8763 records from patients around the globe, culminates in a crucial binary classification feature denoting the presence or absence of a heart attack risk, providing a comprehensive resource for predictive analysis and research in cardiovascular health.

## Heart attack 

This file describes the contents of the heart-disease directory.

This directory contains 4 databases concerning heart disease diagnosis.
All attributes are numeric-valued. The data was collected from the
four following locations:

 1. Cleveland Clinic Foundation (cleveland.data)
 2. Hungarian Institute of Cardiology, Budapest (hungarian.data)
 3. V.A. Medical Center, Long Beach, CA (long-beach-va.data)
 4. University Hospital, Zurich, Switzerland (switzerland.data)