# BreachDetection
The files contained in this repository represent the code used in my dissertation completed August 2025 towards a MSc in Remote Sensing and Environmental Mapping at UCL. The analysis was conducted in Google Earth Engine using Random Forest models. The scripts in this repository are appropriately commented and can be copied into GEE to run the analysis workflow; full instructions are at the end of this document.

The goal of the dissertation was to investigate a model framework for detecting breaching of barrier beaches using land cover classification of times series satellite imagery. Training data was extracted from the time series images of ten study sites and used to train separate models (one per site). These models were used to classify the time series images from each of the other sites and the results were compared. The final result of the dissertation was a 'composite' model trained using data from five of the sites, which displayed high accuracy when used to classify all ten sites (assessed qualitatively).

The workflow of the analysis is as follows:

1. Image acquisition for each study site
2. Image processing (cloud masking and time series compilation)
3. Training data preparation and extraction
4. Model training and classification

Manual research was conducted to select appropriate images for each study site. The image processing was performed using the 'ImageProcessing' script in this repository. The ImageProcessing script is fully functioning and set up to show the process using the Bossington Beach study site. 

Training data preparation was also done manually by digitising point features based on eight land cover classes. Training data extraction, model training, and site classification was performed using the 'TrainingClassification' script in this repository. This script requires the training points and image stacks for each site, which can be downloaded here: https://drive.google.com/file/d/1_MvZXh1Q_JIB4iUjyyNyv5wbixArCA5N/view?usp=sharing (WARNING: Large file, ~230mb)

The training points and image stacks can be uploaded to GEE as assets, and then imported IN ALPHABETICAL ORDER for use with the 'TrainingClassification' script. The script only provides the means to create individually trained models (models trained on one specific site). The composite model can be created by combining training data from multiple sites.

Please reach out with any questions to ucfamd1@ucl.ac.uk or max.dean6@gmail.com
