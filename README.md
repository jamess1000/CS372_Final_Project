# CS 372 Final Project: James Sohigian and Andrew Spong. Kaggle Competition: Image2Biomass
## What it does
Our project explores novel (to our knowledge) solutions to the Kaggle competition created by CSIRO titled *Image2Biomass Prediction*. In general, the motivation behind this competition, and by proxy, this project, is simple: farmers often have to estimate the amount of biomass there is in a given pasture to ensure that they properly utilize the land to feed their animals. For this competition, we are given both tabular and image data in the training set, and with that it is quick to see why this competition was chosen by us: it provides a natural application of many techniques we have learned throughout this course, from simple regression models to CNNs to transfer learning to ViTs and even further, while also having the potential for real-world impact if we develop a stronger model than the competition saw. As such, our vision for this project was to build models from the ground-up, progressively increasing complexity along the way to inform our statistical decisions in the latter stages by what we learned in the more interpretable stages. It is worth noting that while we could use the tabular data from the training set, the competition itself only allows access to images at inference time for the test set. As such, many models we create seek to alleviate this problem to align with the competition rules. However, we also believe there is value in the ensemble models with both image and tabular data, since in real world applications farmers would have access to both for prediction.
## Quick Start
Download the Kaggle data, place it in Google Drive (not inside any folder), and the notebooks should run top-to-bottom to reproduce the results seen in them.
## Video Links
Demo video link:
Technical walkthrough video link:
## Evaluation
Results: (Table that includes MSE from each model, R^2 eval from each model, etc) Exposition on which approach worked best
## Individual Contributions
James: Created the Tabular model and ViT model. Andrew: Created the CNN model and the Transfer Learning from a pretrained ResNet model
