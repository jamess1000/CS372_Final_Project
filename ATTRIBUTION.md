# Kaggle 
In choosing a final project, we looked at competing in a Kaggle competition. While there are several live/ongoing competitions, we found that a past competition -- the CSIRO Image2Biomass Prediction -- was best aligned to apply the architectures and concepts that we learning over the course of this semester. Kaggle provided us with the competition, and the CSIRO Image2Biomass competition provided us with the overview details, evaluation scoring metrics, r-squared calculation, and files/data to run this project.

# Datasets
The CSIRO - Image2Biomass Prediction kaggle competition provided a zip file that contained:
1. test.csv : sample_id — Unique identifier for each prediction row (one row per image–target pair). image_path — Relative path to the image (e.g., test/ID1001187975.jpg). target_name — Name of the biomass component to predict for this row. One of: Dry_Green_g, Dry_Dead_g, Dry_Clover_g, GDM_g, Dry_Total_g. The test set contains over 800 images.
3. train/ : Directory containing training images (JPEG), referenced by image_path.
4. test/ : Directory reserved for test images (hidden at scoring time); paths in test.csv point here.
5. train.csv : sample_id — Unique identifier for each training sample (image). image_path — Relative path to the training image (e.g., images/ID1098771283.jpg). Sampling_Date — Date of sample collection. State — Australian state where sample was collected. Species — Pasture species present, ordered by biomass (underscore-separated). Pre_GSHH_NDVI — Normalized Difference Vegetation Index (GreenSeeker) reading. Height_Ave_cm — Average pasture height measured by falling plate (cm).
target_name — Biomass component name for this row (Dry_Green_g, Dry_Dead_g, Dry_Clover_g, GDM_g, or Dry_Total_g). target — Ground-truth biomass value (grams) corresponding to target_name for this image.
6. sample_submission.csv : sample_id — Copy from test.csv; one row per requested (image, target_name) pair. target — Your predicted biomass value (grams) for that sample_id.

# External Libraries
In each notebook, our first code block is a list of imported external libraries used in the notebook. Some external libraries used include py.torch, pandas, numpy, sklearn, matplotlib, etc. While the first code block in each notebook is not an exhuastive list of imports as some code blocks later in the file might import additional libraries, all used libraries are imported within each notebook.

# Use of generative AI
Generative AI was consulted in the creation of some codeblocks within the notebooks. Within each notebook, generative AI attribution is provided before or below the cell block that it assisted creating. This includes several classes, functions, and graphs throughout all of the notebooks. Each notebook includes specific attributions throughout for transparency. 
