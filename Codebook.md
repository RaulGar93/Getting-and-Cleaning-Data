##This is the code book for the project

The variables in the tidy data:

Tidy data contains 180 rows and 68 columns. Each row has averaged variables for each subject and each activity.

Only all the variables estimated from mean and standard deviation in the tidy set were kept:

mean(): Mean value.

std(): Standard deviation.

The data were averaged based on subject and activity group.

Subject column is numbered sequentially from 1 to 30. Activity column has 6 types as listed below.

WALKING.
WALKING_UPSTAIRS.
WALKING_DOWNSTAIRS.
SITTING.
STANDING.
LAYING.
The tidy data contains 6 rows (averaged based on activity) and 68 columns (66 variables and activity labels).
1-"activitylabel"
2-subject"
3-"tBodyAcc-mean()-X"
4-"tBodyAcc-mean()-Y"
5-"tBodyAcc-mean()-Z"
6-"tBodyAcc-std()-X"
7-"tBodyAcc-std()-Y"
8-"tBodyAcc-std()-Z"
9-"tGravityAcc-mean()-X"
10-"tGravityAcc-mean()-Y"
11-"tGravityAcc-mean()-Z"
12-"tGravityAcc-std()-X"
13-"tGravityAcc-std()-Y"
14-"tGravityAcc-std()-Z"
15-"tBodyAccJerk-mean()-X"
16-"tBodyAccJerk-mean()-Y"
17-"tBodyAccJerk-mean()-Z"
18-"tBodyAccJerk-std()-X"
19-"tBodyAccJerk-std()-Y"
20-"tBodyAccJerk-std()-Z"
21-"tBodyGyro-mean()-X"
22-"tBodyGyro-mean()-Y"
23-"tBodyGyro-mean()-Z"
24-"tBodyGyro-std()-X"
25-"tBodyGyro-std()-Y"
26-"tBodyGyro-std()-Z"
27-"tBodyGyroJerk-mean()-X"
28-"tBodyGyroJerk-mean()-Y"
29-"tBodyGyroJerk-mean()-Z"
30-"tBodyGyroJerk-std()-X"
31-"tBodyGyroJerk-std()-Y"
32-"tBodyGyroJerk-std()-Z"
33-"tBodyAccMag-mean()"
34-"tBodyAccMag-std()"
35-"tGravityAccMag-mean()"
36-"tGravityAccMag-std()"
37-"tBodyAccJerkMag-mean()"
38-"tBodyAccJerkMag-std()"
39-"tBodyGyroMag-mean()"
40-"tBodyGyroMag-std()"
41-"tBodyGyroJerkMag-mean()"
42-"tBodyGyroJerkMag-std()"
43-"fBodyAcc-mean()-X"
44-"fBodyAcc-mean()-Y"
45-"fBodyAcc-mean()-Z"
45-"fBodyAcc-std()-X"
46-"fBodyAcc-std()-Y"
47-"fBodyAcc-std()-Z"
47-"fBodyAccJerk-mean()-X"
48-"fBodyAccJerk-mean()-Y"
49-"fBodyAccJerk-mean()-Z"
50-"fBodyAccJerk-std()-X"
51-"fBodyAccJerk-std()-Y"
52-"fBodyAccJerk-std()-Z"
53-"fBodyGyro-mean()-X"
54-"fBodyGyro-mean()-Y"
55-"fBodyGyro-mean()-Z"
56-"fBodyGyro-std()-X"
57-"fBodyGyro-std()-Y"
58-"fBodyGyro-std()-Z"
59-"fBodyAccMag-mean()"
60-"fBodyAccMag-std()"
61-"fBodyBodyAccJerkMag-mean()"
62-"fBodyBodyAccJerkMag-std()"
63-"fBodyBodyGyroMag-mean()"
64-"fBodyBodyGyroMag-std()"
65-"fBodyBodyGyroJerkMag-mean()"
66-"fBodyBodyGyroJerkMag-std()"

Variable class:
Activity variable is factor type. Subject variable is integer type. All the other variables are numeric type.

##How to get to the output mytinydata.txt:

Download data from the link below and unzip it into working directory of R Studio.
Execute the R script.
About the source data.
The source data are from the Human Activity Recognition Using Smartphones Data Set. A full description is available at the site where the data was obtained: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones Here are the data for the project: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

About R script:
File with R code "run_analysis.R" performs the 5 following steps (in accordance assigned task of course work):

Reading in the files and merging the training and the test sets to create one data set.
1.1 Reading files
  1.1.1 Reading trainings tables
  1.1.2 Reading testing tables
  1.1.3 Reading feature vector
  1.1.4 Reading activity labels
  1.2 Assigning variable names
  1.3 Merging all data in one set

Extracting only the measurements on the mean and standard deviation for each measurement.
2.1 Reading variable names
2.2 Create vector for defining ID, mean and standard deviation
2.3 Making nessesary subset from merged data set

Using descriptive activity names to name the activities in the data set.

Appropriately labeling the data set with descriptive variable names.

Creating a second, independent tidy data set with the average of each variable for each activity and each subject
5.1 Making second tidy data set
5.2 Writing second tidy data set in txt file

The code assumes all the data is present in the same folder, un-compressed and without names altered.

About variables:
x_train, y_train, x_test, y_test, subject_train and subject_test contain the data from the downloaded files.
x_data, y_data and subject_data merge the previous datasets to further analysis.
features contains the correct names for the x_data dataset, which are applied to the column names stored in
