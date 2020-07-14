# Spark MLlib and Stream Data Prediction  

Trained a simple supervised machine learning classification model (offline) that is able to predict the label of a given Wikipedia edit in online streaming.

### Overview of Steps

1.	Gathering historical data 
Streamed and saved historical data from April 15, 2020 through April 21, 2020. (using provided script spark_streaming_example_saving.py.ipynb). Data files are combined using linux commands. 

2.	Data exploration 
I explored the historical dataset and found the dataset to be unbalanced. I notice that many unsafe and vandal edits are made by Unregistered (IP or not logged in) users with names such as "name_user": "190.215.27.232". Though less common, vandal edits are someimies  made by Users with silly names such as "Tylertoney Dude perfect". 

3.	Data preprocessing using MLlib 
For model training purposes, I focus on the three columns: label, text_new, text_old. Train set and test set are preprocessed separately. 

<img src="https://github.com/Finterly/Wiki-Edit-Prediction-PySpark/blob/master/preprocess1.png" width = 400px>


4.	Pipeline: feature engineering, model training, tuning, and selection using MLlib
I proceed with the train data set. 

<img src="https://github.com/Finterly/Wiki-Edit-Prediction-PySpark/blob/master/pipeline1.png" width = 400px>


5.	Streaming and Prediction
<img src="https://github.com/Finterly/Wiki-Edit-Prediction-PySpark/blob/master/prediction.png" width = 400px>


Output : Printed stream predictions

<img src="https://github.com/Finterly/Wiki-Edit-Prediction-PySpark/blob/master/stream.png" width = 400px>

