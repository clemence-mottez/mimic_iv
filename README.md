# ** Enhancing Performance and Interpretability of Machine Learning for Chest X-ray Diagnosis using Transfer Learning on the MIMIC-IV dataset**
### **Introduction**
The goal of this project is to predict lung disease or dysfunction from X-ray images and other relevant clinical features and measurements using the MIMIC-4 dataset. Recently, the use of Deep Learning for CXR has been a common technology in detecting Chronic Respiratory Diseases (CRD) with high or even human-level accuracy. But current techniques only focus on CXR images, they often neglect the potential advantages of incorporating non-imagery information of patients. 
The goal of this project is to combine imagery and non-imagery data in order to advance CXR diagnostics. Our method aims to increase prediction accuracy while maintaining the speed and efficiency of deep learning through the concept of transfer learning. Our goal is to optimize machine learning's effectiveness in supporting medical professionals.  

### **Research Aim**
In this work, we propose a multi-faceted predictive system that uses TL to infuse EHR data into the ML-based CRD diagnosis using CXR. The system is expected to maintain the highly accurate nature of DL and the informativeness of Electronic Health Records (HER) and classical ML models. Rigorous testing and validation will be carried out in 2 stages, the first stage will evaluate the performance of the proposed system, and the second stage will delve deeper into investigating the model’s decision-making process. By adopting a comprehensive evaluation strategy, encompassing both performance metrics and interpretability measures, we expect to answer the following research question: Does incorporating EHR data into CXR diagnosis for CRD help in improving the ML model’s performance, transparency and trustworthiness in its decision-making processes?

### **Github Overview**
Different documents and resources are at your disposal in this repository to support our project: 
**Jupyter Notebooks: **
-	cohort_and_x_ray_selection.ipynb: This notebook contains code for querying the cohort of patients we are studying and choosing relevant X-ray images.
-	x_ray_data.ipynb: In this notebook, you will find the code for creating a dataset that includes the X-ray features and links them to a specific **subject_id** and **hadm_id** identifiers.
-	Final_data.ipynb: This notebook queries and adds additional features to our cohort of patients and incorporate diagnoses for each disease. 
-	EBM.ipynb: This notebook focuses on training an Explainable Boosting Machine (EBM) model to assess the effect and importance of each feature on our model's predictions. EBM is a machine learning model designed to provide transparency and interpretability.
-	Feature_importance.ipynb: In this notebook, we train an XGBoost Gain Importance model and use eBoruta with SHAP importance measures to help identify the key variables that have the most significant impact on our model's accuracy by evaluating and quantifying the effect of each feature on the model’s predictive power.

**Pdf files:**
-	Project_Proposal.pdf: This document contains our project proposal, outlining the initial plan and objectives.
-	Final report.pdf: The final report can be found in this file. It summarizes the outcomes and findings of our project, providing a comprehensive overview of our work.

### **Data**
The project relies on the MIMIC-IV dataset, which contains a wide range of clinical and image data for analysis. You need a special training to have access to this data. 
