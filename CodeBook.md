**INTRODUCTION**

The script run_analysis will
   1/- Merge the train and test set which down load from this file
	d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 
   2/- Extract only the measurement on the mean and standard deviation for each measurement from file features.txt	
   3/- Use descriptive activity names to name the activities in the data set activity_labels.txt.
   4/- Appropriately label the data set with descriptive variable names from merged data set train and test.
   5/- Create a second, independent tidy data set with the average of each variable for each activity and each subject ((30 subjects * 6 activities = 180 rows)).
        The output file is called averages_data.txt, and uploaded to github repository.	

**VARIABLES**

   1/-Download file:
	x_train, y_train, x_test, y_test, subject_train and subject_test. 

   2/-Merger data set:
	x_data, y_data and subject_data.

   3/- Features contains the correct names for the x_data dataset, which are applied to the column names stored in mean_and_std_features, a numeric vector used to extract the desired data.

   4/-  A similar approach for y_data dataset is taken with activity names through the activities variable.

   5/- Final modified merge dataset:
	all_data

   6/- Tidy dataset which contains the relevant averages which will be later stored in a .txt file. ddply() from the plyr package is used to apply colMeans() and ease the development.
	averages_data 