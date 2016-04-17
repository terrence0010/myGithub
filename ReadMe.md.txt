DataSet Description
-------------------
The Human Activity Recognition(HAR) using Smartphones Dataset created from experiments conducted with a group of 30 people in the age group (19-48) years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy) on the waist. Using its embedded accelerometer and gyroscope, 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz data were captured. The experiments were video-recorded to label the data manually. The obtained dataset was randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

R Program Name: run_analysis.R

Program Description
--------------------
The run_analysis.R script reads data from the "Human Activity Recognition(HAR) Using Smartphones Dataset and produces tidy dataset which may be used for further analysis.

The run_analysis.R script merges data from a number of .txt files and produces a tidy data set which may be used for further analysis. High level overview is as follows

1) Loads "reshape2" package (if required)  and reads all required .txt files and labels the datasets

2) Appropriate Column Names "activity_id"'s and "subject_id"'s are appended to the "test" and the "training" data, which are then combined into one single data frame

3) Using the "grep" function, all the columns with mean() and std() values are extracted and then a new data frame, including only the "activity_id", the "subject_id" and the mean() and std() columns, is created

4) Using the "merge" function, descriptive activity names are merged with the mean/std values dataset, to get one dataset with descriptive activity names

5) Use "melt" and "dcast" functions to convert data into a table containing mean values of features, ordered by the activity name and the subject id, and the data is written to the "tidy_movement_data.txt" file.

6) Pl refer to description of the "tidy_movement_data.txt" file in the "CodeBook.md" file.

Pre-requisite for executing run_analysis.R
------------------------------------------
Download Human Activity Recognition - Smartphone data zip file from the following URL into your local HDD and extract it 

URL: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip


