# cyclepower2
 Repository for materials in relation to BEng Project
 
Steps to run Baseline and GLM Model
A.	Rider to rider –
1.	Go to rider folder in google drive and copy the folder ID from the URL and paste/replace it in the file_list query and run the code section. This will import the ride files in the /root/data directory.
2.	After importing the files, rename one ride file to ‘ test_’. Make sure all_files and test_files variables are set as ‘rider_*.csv’ and ‘test_*.csv’.
3.	Now change the features_considered and test_features_considered headers to ‘_old’ when running the models for rider 4 and ‘_new’ for other riders. Also change the headers to ‘minimal’ or ‘extended’ to switch between minimal and extended features. 
4.	Make sure to comment out all the variables index1, index2, train1, test, train2, frames2, features, total_tst.
5.	Change the slicing index for X_train and X_test variables to (number of columns – 1) in the header variable. That is *_minimal _* headers contain 4 columns(excluding power) and *_extended _* headers 8 columns (excluding power). You may include weight (when using non-normalized data) and heartrate, however, then you have to change the number of columns again.
6.	Now run the rest of the code sections

B.	All riders –
1.	Go to rider folder in google drive and copy the folder ID from the URL and paste/replace it in the file_list query and run the code section. This will import the ride files in the /root/data directory. Perform this step for all four riders.
2.	Now rename rider 4 files to ‘old_’ and in the code section change the all_files and test_files variables ‘rider_*.csv’ and ‘old_*.csv’ respectively. Run this code section. This will read all the rider files and load the files into DataFrames.
3.	In the next code section change the features_considered and test_features_considered headers to ‘_new’ and ‘_old’ respectively. And also uncomment all the variables index1, index2, train1, test, train2, frames2, features, total_tst. Change the index1 and index2 variable as (total_trn – length of last imported new file) and (total_trn + length of first imported old file)
4.	Change the slicing index for X_train and X_test variables to (number of columns – 1)
5.	Now run the rest of the code sections










Steps to run LSTM Model
A.	Rider to rider –
1.	Go to rider folder in google drive and copy the folder ID from the URL and paste/replace it in the file_list query and run the code section. This will import the ride files in the /root/data directory.
2.	After importing the files, rename one ride file to ‘ test_’. Make sure all_files and test_files variables are set as ‘rider_*.csv’ and ‘test_*.csv’.
3.	Now change the features_considered and test_features_considered headers to ‘_old’ when running the model for rider 4 and ‘_new’ for other riders. Also change the headers to ‘minimal’ or ‘extended’ to switch between minimal and extended features. 
4.	Make sure to comment out all the variables index1, index2, train1, test, train2, frames2, features, total_tst. Also comment out the TRAIN_SPLIT = len(train1)+len(train2).
5.	Now run the rest of the code sections

B.	All riders –
1.	Go to rider folder in google drive and copy the folder ID from the URL and paste/replace it in the file_list query and run the code section. This will import the ride files in the /root/data directory. Perform this step for all four riders.
2.	Now rename rider 4 files to ‘old_’ and in the code section change the all_files and test_files variables ‘rider_*.csv’ and ‘old_*.csv’ respectively. Run this code section. This will read all the rider files and load the files into DataFrames.
3.	In the next code section change the features_considered and test_features_considered headers to ‘_new’ and ‘_old’ respectively. And also uncomment all the variables index1, index2, train1, test, train2, frames2, features, total_tst. Change the index1 and index2 variable as (total_trn – length of last imported new file) and (total_trn + length of first imported old file)
4.	Uncomment out the TRAIN_SPLIT = len(train1)+len(train2).
5.	Now run the rest of the code sections

Both baselines and LSTM can be run with normalized and non-normalized data. Comments accompany normalization blocks of code and may be uncommented or commented depending on how you wish to run the code.
For GLM model, it is preferred that the data is non-normalized since we require the dependent power variable to remain non-negative.

