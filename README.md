# SELFI 
SELFI is a framework to predict the future emotion labels from past emotion labels and the current facial image.<br/>
# File Structure
* The code file self_report.ipynb is the implementation of the framework.<br/>
* The Data folder contain two folders: <br/>
1. FacialData contain 3 folders for Amazon, Google and Microsoft image analysis tool. Each of these folders contain a file that stores facial feature values for each image of a particular user.<br/>
2. Self_reports folder contain 2 folders (Valence and Arousal) , where each folder has a file contain the sequence of self-reports for a particuler user. <br/>  
# Input Files
To predict valence/arousal label, 2 files are required.<br/>
1. self-report file located in Valence and Arousal folder to predict valence and arousal label, respectively. It has the following format:<br/>

|old_emo|current_emo|old_img|curr_img|elap_time|
|-------|:-----------:|-------:|--------:|---------|
|1	|1	|user_12/IMG_20210902_150844.jpg|	user_12/IMG_20210902_172538.jpg|	2.28154166666667|
|1	|0	|user_12/IMG_20210902_172538.jpg|	user_12/IMG_20210902_194304.jpg|	2.29043722222222|

old_emo and current_emo represent current emotion and next emotion, respectively. Similarly, old_img and curr_img represents the name of image file corresponding to the current and next emotion label. The elap_time is the elapsed time between current emotion and next emotion label in hour.<br/>
2. Facial feature file located in subfolder within the FacialData folder. <br/>
# Run the code
To run the code, specify
* user_no. 
* input files name.
* run the code block written for a particuler image analysis tool to list facial features it returns.
* In the last code block, comment or uncomment specific lines of the code to select feature reduction tool.
# Pipeline for Data Preparation
Use files in FileProcessing folder to extract features from image using different tool: Amazon Rekognition, Google Vision, Microsoft Azure. 
**Prepare data using Amazon Rekognition** <br/>
* run GetFeatures_AWS.ipynb to extract features from image. <br/>
* run data_preprocessing.ipynb to break the composite features into simple feature.<br/>
* run data_encoding.ipynb to encode the categorical features. <br/>
**Prepare data using Google Vision** <br/>
* run GetFeatures_Vision.ipynb to extract features from image. <br/>
* run BreakingComplexFeatureVision.ipynb to break the composite features into simple feature. <br/>
**Prepare data using Microsoft Azure** <br/>
* run GetFeatures_Azure.ipynb to extract features from image. <br/>
* run BreakingComplexFeaturesAzure.ipynb to break the composite features into simple feature.<br/>

