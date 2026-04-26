# Data Download
To download the data, we have the following process:
1. Go to https://www.kaggle.com/competitions/csiro-biomass/overview.
2. Join the competition (Click `Late Submission').
3. From there, navigate to the Data tab of the competition and download the zip file.
4. Upload the Zip file to Google Drive. The notebooks run easiest if it is not in a folder.

# Running the Project
Each notebook works as a stand-alone notebook that explores different possible models using the data downloaded from the competition. In general, it might be easiest to read the Custom_CNN_and_ResNet notebook first, then the VIT notebook, then the tabular notebook, then the Predict_Feature_Plus_Tabular notebook, then the ensemble model notebook, with the model comparison notebook coming last. Each notebook should run top-to-bottom without any changes on your end if it is run in Google Colab.

# Model Comparison Document
Each notebook saves the result to your google drive, which the model comparison document then accesses to generate its plots. Thus, it is best that if this re-run, it should be re-run last to match our results.
