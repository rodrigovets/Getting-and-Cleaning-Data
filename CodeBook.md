# Getting and Cleaning Data - Course Project
## CodeBook

This file describes step-by-step the comands, variables and data used in run_analysis.R script on how to clean the data. 

A full description of the available were obtained at the site: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

The data used for the project:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Directions:

1. Read X_train.txt, y_train.txt and subject_train.txt from the "./UCI_HAR_Dataset/train" folder.
2. Store train values in trainData, trainLabel and trainSubject variables respectively.
3. Read X_test.txt, y_test.txt and subject_test.txt from the "./UCI_HAR_Dataset/test" folder.
4. Store test values in testData, testLabel and testsubject variables respectively.
5. Concatenate testData to trainData to generate a 10299x561 data frame called joinData.
6. Concatenate testLabel to trainLabel to generate a 10299x1 data frame called joinLabel.
7. Concatenate testSubject to trainSubject to generate a 10299x1 data frame called joinSubject.
8. Read the features.txt file from the "./UCI_HAR_Dataset" folder.
9. Store the data in a variable called features. We only extract the measurements on the mean and standard deviation. Get a subset of joinData with the 66 corresponding columns.
10. Clean the column names of the subset. Remove the "()" and "-" in the names, remove the first letter of mean and std, add the capital letters M and S.
11. Read the activity_labels.txt file from the "./UCI_HAR_Dataset" folder.
12. Store the data in a variable called activity.
13. Clean the activity names in the second column of activity. Firstly, make all names to lower cases. If the name has an underscore remove it and capitalize the letter after the underscore.
14. Transform the values of joinLabel according to the activity data frame.
15. Combine the joinSubject, joinLabel and joinData by column to get a new cleaned 10299x68 data frame called cleanedData. The subject column contains integers that range 1 to 30. The activity column contains 6 kinds of activity names; the last 66 columns contain measurements that range from -1 to 1.
16. Write the cleanedData out to mergeddata.txt file in current working directory.
17. Generate a second tidy data set with the average of each measurement for each activity and each subject. We have 30 unique subjects and 6 unique activities, which result in a 180 combinations of the two. Then, for each combination, we calculate the mean of each measurement with the corresponding combination. So, after initializing the result data frame and performing the two for-loops, we get a 180x68 data frame.
18. Write the result out to tidydataset.txt file in current working directory, without the row names.