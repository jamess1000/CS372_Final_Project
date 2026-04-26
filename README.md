# CS 372 Final Project: James Sohigian and Andrew Spong. Kaggle Competition: Image2Biomass
## Project Title
*From Landscape to Biomass*. In this project, which explores solutions to the Kaggle competition created by CSIRO titled *Image2Biomass Prediction*, we apply machine learning techniques such as regression, gradient boosting, CNNs, transfer learning, and ViTs to predict 5 biomass features from image and tabular data. 
## What it does
Our project explores novel (to our knowledge) solutions to the Kaggle competition created by CSIRO titled *Image2Biomass Prediction*. In general, the motivation behind this competition, and by proxy, this project, is simple: farmers often have to estimate the amount of biomass there is in a given pasture to ensure that they properly utilize the land to feed their animals. For this competition, we are given both tabular and image data in the training set, and with that it is quick to see why this competition was chosen by us: it provides a natural application of many techniques we have learned throughout this course, from simple regression models to CNNs to transfer learning to ViTs and even further, while also having the potential for real-world impact if we develop a stronger model than the competition saw. As such, our vision for this project was to build models from the ground-up, progressively increasing complexity along the way to inform our statistical decisions in the latter stages by what we learned in the more interpretable stages. It is worth noting that while we could use the tabular data from the training set, the competition itself only allows access to images at inference time for the test set. As such, many models we create seek to alleviate this problem to align with the competition rules. However, we also believe there is value in the ensemble models with both image and tabular data, since in real world applications farmers would have access to both for prediction.
## Quick Start
Download the Kaggle data, place it in Google Drive (not inside any folder), and the notebooks should run top-to-bottom to reproduce the results seen in them. Review SETUP.md for a more detailed walkthrough of the project setup. 
## Video Links
Demo video link:
Technical walkthrough video link:
## Evaluation
**Results:**
| model                     | category                | test_weighted_R2 | can_submit |
|--------------------------|-------------------------|------------------|------------|
| LightGBM                 | Tabular (local only)    | 0.837255         | False      |
| Ridge (alpha=0.01)       | Tabular (local only)    | 0.674643         | False      |
| ViT-B/16 fine-tuned      | ViT                     | 0.589443         | True       |
| ResNet18 fine-tuned      | CNN                     | 0.565345         | True       |
| Custom CNN               | CNN                     | 0.458950         | True       |
| Custom ViT               | ViT                     | 0.436188         | True       |
| Fusion (ViT + Tabular)   | Combined (local only)   | 0.394447         | False      |
| Constant Baseline        | Tabular (local only)    | 0.212215         | False      |
**Comments on results:**
The models that utilize tabular data have the best results on the defined evaluation market, however, they are not usable for submission since the test data only includes an image path (there is no tabular data). Of the strictly vision models that are eligible for submission, we see that the fine tuned ViT performs the best. It is also worth noting that the combined/fushion model performs worse than any of the single modality models. As a result, for this competition, we would recommend submitting the ViT fine-tuned model, but in reality where farmers have access to both tabular and image data, we would recommend the gradient boosting model. For a more detailed analysis on evaluation, see the model_comparison_fin notebook. 
## Individual Contributions
James: Created the tabular models, ViT models, combined/fushion Model, and model comparison notebook. Andrew: Created the CNN model, the Transfer Learning from a pretrained ResNet model, the ensemble model within the predict features plus tabular notebook, and organized the github repo. 
Both individuals collaborated on project ideation, architecture, notebook editing, and final check of all files.
