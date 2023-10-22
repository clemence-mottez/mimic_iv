# **Evaluation of transfer learning for enhancing chest x-ray diagnosis using MIMIC-IV dataset**

### **Introduction**
In this project, we aim to use the MIMIC-4 dataset to predict lung disease or dysfunction from X-ray images and other relevant clinical features and measurements. The use of machine learning for chest X-ray analysis has significantly reduced diagnosis time for practitioners in the field of respiratory diagnostics. However, there's still untapped potential, as current approaches often rely solely on imagery data without considering external factors such as policies or intervention procedures.  

This project endeavors to advance CXR diagnostics by combining imagery and non-imagery data. Our approach aims to retain the speed and efficiency of deep learning while improving prediction accuracy through the concept of transfer learning. We intend to maximize the efficiency of ML in aiding healthcare practitioners.  

### **Project Overview**
- Transfer Learning & Fusion  
The core of our system is built on the concept of transfer learning. We utilize a deep learning model pre-trained on common chest X-ray datasets to extract latent representations of the images. This approach allows us to leverage pre-learned information without incurring the cost of extensive training time. By infusing external features with this learned knowledge, we create a holistic diagnostic model.  

- Models: ResNet-CNN & ML Classifier  
Our deep learning procedure incorporates ResNet, one of the most common deep architectures in computer vision. ResNet's ability to analyze features deeply between layers provides the system with a rich understanding of the data, allowing for more informed predictions. The final stage of the project will involve processing these features with a chosen ML classifier model to predict the likelihood of each disease occurring.  

- Outcome Evaluation  
To assess the impact of including non-image features in our predictive models, we will conduct direct comparisons with models that do not include them. We anticipate that models including non-image features will demonstrate improved classification performance.  

- Metrics  
Given the multi-label classification problem, we will evaluate our system using standard metrics such as Precision, Recall, and F1-Score, which provide insights into the system's ability to avoid Type I and Type II errors for each disease. Additionally, we will use AUC-ROC to evaluate the model's distinguishing power through different likelihood thresholds. Interpretability is also a critical aspect of our project, and we will perform exploratory data analysis to identify the main features contributing to the system's decision-making.

### **Data**
The project relies on the MIMIC-4 dataset, which contains a wide range of clinical and image data for analysis. You need a special training to have access to this data. 

