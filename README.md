# SELFI 
How to use the framework SELFI to predict the future emotion labels.<br/>
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

