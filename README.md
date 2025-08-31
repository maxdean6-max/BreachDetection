# BreachDetection
The files contained in this repository represent the code used in my dissertation completed August 2025 towards a MSc in Remote Sensing and Environmental Mapping at UCL.
The goal of the dissertation was to investigate / create a model framework for detecting breaching of barrier beaches using land cover classification of times series satellite imagery.

The analysis was conducted in Google Earth Engine using Random Forest models on ten study sites. Training data was extracted from the time series images of each study site and used
to train ten separate models (one per site). These models were used to classify the time series images from each of the other sites and the results were compared. The final result of
the dissertation was a 'composite' model trained using data from five of the sites, which displayed high accuracy when used to classify all ten sites (assessed qualitatively).

The workflow of the analysis is as follows:

1. Image acquisition for each study site
2. Image processing (cloud masking and time series compilation)
3. Training data preparation and extraction
4. Model training and classification

Image acquisition and processing is performed using the ImageProcessing script, although the study dates / parameters set up in the script are set based on manual research to collect
ten images over a specific location.


