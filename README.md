# Getting-and-Cleaning-Data-Course-Project

**README

Dataset:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 

Files:
1. README.md: 
- README description and code book describing the variables, the data, and transformations to clean up the data

2. run_analysis.R: 
- includes data preparation and 5 steps from course project’s definition:
-- Merges the training and the test sets to create one data set.
-- Extracts only the measurements on the mean and standard deviation for each measurement.
-- Uses descriptive activity names to name the activities in the data set
-- Appropriately labels the data set with descriptive variable names.
-- From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

**Code Book

1. Extract UCI HAR Dataset for the project

2. Appropriately set variable from the data set
- features <- features.txt
- activities <- activity_labels.txt 
- subject_test <- test/subject_test.txt 
- x_test <- test/X_test.txt
- y_test <- test/y_test.txt
- subject_train <- test/subject_train.txt 
- x_train <- test/X_train.txt 
- y_train <- test/y_train.txt 

3. Merges the training and the test sets to create one data set using:
- X with the rbind() function
- Y with the rbind() function
- Subject with the rbind() function
- Merged_Data with the cbind() function

4. Extracts only the measurements on the mean and standard deviation for each measurement using:
- TidyData subsetted by Merged_Data using the mean and standard deviation (std) for each measurement

5. Uses descriptive activity names to name the activities in the data set
- Numbers in code column of the TidyData are replaced with corresponding activity from the second column of activities variable

6. Appropriately labels the data set with descriptive variable names
- code column in TidyData renamed into activities
- All Acc in column’s name replaced by Accelerometer
- All Gyro in column’s name replaced by Gyroscope
- All BodyBody in column’s name replaced by Body
- All Mag in column’s name replaced by Magnitude
- All start with character f in column’s name replaced by Frequency
- All start with character t in column’s name replaced by Time

7. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject
FinalData made from sumarizing TidyData by taking the means of each variable from each activity and each subject, after groupped by subject and activity.
