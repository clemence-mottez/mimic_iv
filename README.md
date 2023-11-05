# Enhancing Chest X-ray Diagnosis for Respiratory Diseases using Transfer Learning


## Description
Recently, the use of Deep Learning for Chest X-ray (CXR) has been a common technology in detecting Chronic Respiratory Diseases (CRD) with high or even human-level accuracy. But current techniques only focus on CXR images, they often neglect the potential advantages of incorporating non-imagery information of patients. 

The goal of this project is to combine imagery and non-imagery data in order to advance CXR diagnostics. Our method aims to increase prediction accuracy while maintaining the speed and efficiency of deep learning through the concept of transfer learning. Our goal is to optimize machine learning's effectiveness in supporting medical professionals. 

## **Structure Overview**
The following is an overview of our repository:
```shell
Root
├───Code
│   ├───Cohort Formation
│   └───Evaluation Models
└───Results
    ├───Images
    └───Tables
```

Different scripts are implemented in this repository for this project: 

```shell
├───Code
│   ├───Cohort Formation
│   │       CohortSelection.ipynb           # Filter cohort by existence in MIMIC-CXR
│   │       CXRRetrieval.ipynb              # Selecting 1 CXR for each patient
│   │       FinalisedCohortData.ipynb       # Feature extraction on MIMIC-IV, finalising data (to be run last)
│   │       TranserLearning_Colab.ipynb     # Extract latent features from CXR images (to be run on Colab)
│   │       TransferLearning_Local.ipynb    # Extract latent features from CXR images (to be run locally)
│   │
│   └───Evaluation Models
│           EBM.ipynb                       # Running Explainable Boosting Model to evaluate feature importance (deprecated)
│           EDA.ipynb                       # Exploratory Data Analysis on cohort data
│           Evaluation.ipynb                # Perform data split, model runs and plot out some results
│           FeatureImportance.ipynb         # Extract feature importance metrics
```

### **Data**
The project relies on the MIMIC-IV dataset, which contains a wide range of clinical and image data for analysis. You need a [special training](https://physionet.org/content/mimiciv/view-required-training/2.2/#1) to have access to this data.

## Requirements
This notebook is run on Python 3.10.12, with packages specified in `requirements.txt`. 
- The notebook was originally executed on Google Colab. 
- Minimum 4GB of memory required.
- GPU resource is not required.


### Environment Setup
There are 2 ways of running the notebook: using Colab and running on local.

#### Running on Colab (Recommended)
This is the recommended method. **Hyperlinks that make reference to plots will only work on Colab!**
1. Install [Google Colaboratory](https://workspace.google.com/u/0/marketplace/app/colaboratory/1014160490159) on your [Google Drive](https://drive.google.com).
2. Upload your `.ipynb` notebook file to Google Drive. The notebook should automatically open on Colab.

**Note:** In case of any incompatibilities due to Colab changing package versions, add the following code cell to the start of your notebook and run it:
```
!wget https://github.com/clemence-mottez/mimic_iv/raw/main/requirements.txt
!pip install requirements.txt
``` 

#### Running on local
Note that **hyperlinks that make reference to plots will not work, as local Jupyter notebook does not support HTML!**

In most cases, the notebook can be run locally by just installing the required package versions with the following command (`requirements.txt` is assumed to be in the same directory as your notebook):

```bash
pip install requirements.txt
```

To replicate Colab’s operating system on local computer, this is the specifications of the Colab environment as of October 2023:

```
Python implementation: CPython
Python version       : 3.10.12
IPython version      : 7.34.0

Compiler    : GCC 11.4.0
OS          : Linux
Release     : 5.15.120+
Machine     : x86_64
Processor   : x86_64
CPU cores   : 2
Architecture: 64bit
```

Make sure to do removal/add exception handler for any line in the form of `from google.colab import ...`!