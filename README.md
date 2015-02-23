# Getting-and-Cleaning-Data-Project
##Getting and Cleaning Data Course Project
# run_analysis.R
This file does the following steps on datasets
1- Merges the training and the test sets to create one data set.
2- Extracts only the measurements on the mean and standard deviation for each measurement.
3- Uses descriptive activity names to name the activities in the data set
4- Appropriately labels the data set with descriptive activity names.
5- Creates a second, independent tidy data set with the average of each variable for each activity and each subject.
# How Scripts works
* this scrips needs data.table and reshape2 packages
* datasets must be in a folder named 'UCI HAR Dataset' the working directory
* run the script via command line or gui
* this function makes the tidy data in a file named 'tidy_data.txt' in the working directory 
