# Code Book-
This is a code book for getting and cleaning data course project.

# About the dataset
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

For each record it is provided:
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

# Dataset files
The dataset includes the following files:

- 'README.txt'

- 'features_info.txt': Shows information about the variables used on the feature vector.

- 'features.txt': List of all features.

- 'activity_labels.txt': Links the class labels with their activity name.

- 'train/X_train.txt': Training set.

- 'train/y_train.txt': Training labels.

- 'test/X_test.txt': Test set.

- 'test/y_test.txt': Test labels.

# Steps to tidy data
the goal is to make tidy data via the following steps
1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive activity names.
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.


# tidy data


| column       | description                                              | type    |
| ------------ | -------------------------------------------------------- | ------- |
| Subject      | Identifier of the subject                                | integer |
| Activity     | Label of the activity                                    | factor  |
| MeanSamples  | Mean of variables by Subject + Activity provided in tidy | numeric |

tidy data contains the following columns

|  Original Name               | Column                      |
| ----------------------------| --------------------------- |
|                             | Activity                    |
|                             | Subject                     |
| tBodyAcc-mean()-X           | tBodyAcc-mean()-X           |
| tBodyAcc-mean()-Y           | tBodyAcc-mean()-Y           |
| tBodyAcc-mean()-Z           | tBodyAcc-mean()-Z           |
| tBodyAcc-std()-X            | tBodyAcc-std()-X            |
| tBodyAcc-std()-Y            | tBodyAcc-std()-Y            |
| tBodyAcc-std()-Z            | tBodyAcc-std()-Z            |
| tGravityAcc-mean()-X        | tGravityAcc-mean()-X        |
| tGravityAcc-mean()-Y        | tGravityAcc-mean()-Y        |
| tGravityAcc-mean()-Z        | tGravityAcc-mean()-Z        |
| tGravityAcc-std()-X         | tGravityAcc-std()-X         |
| tGravityAcc-std()-Y         | tGravityAcc-std()-Y         |
| tGravityAcc-std()-Z         | tGravityAcc-std()-Z         |
| tBodyAccJerk-mean()-X       | tBodyAccJerk-mean()-X       |
| tBodyAccJerk-mean()-Y       | tBodyAccJerk-mean()-Y       |
| tBodyAccJerk-mean()-Z       | tBodyAccJerk-mean()-Z       |
| tBodyAccJerk-std()-X        | tBodyAccJerk-std()-X        |
| tBodyAccJerk-std()-Y        | tBodyAccJerk-std()-Y        |
| tBodyAccJerk-std()-Z        | tBodyAccJerk-std()-Z        |
| tBodyGyro-mean()-X          | tBodyGyro-mean()-X          |
| tBodyGyro-mean()-Y          | tBodyGyro-mean()-Y          |
| tBodyGyro-mean()-Z          | tBodyGyro-mean()-Z          |
| tBodyGyro-std()-X           | tBodyGyro-std()-X           |
| tBodyGyro-std()-Y           | tBodyGyro-std()-Y           |
| tBodyGyro-std()-Z           | tBodyGyro-std()-Z           |
| tBodyGyroJerk-mean()-X      | tBodyGyroJerk-mean()-X      |
| tBodyGyroJerk-mean()-Y      | tBodyGyroJerk-mean()-Y      |
| tBodyGyroJerk-mean()-Z      | tBodyGyroJerk-mean()-Z      |
| tBodyGyroJerk-std()-X       | tBodyGyroJerk-std()-X       |
| tBodyGyroJerk-std()-Y       | tBodyGyroJerk-std()-Y       |
| tBodyGyroJerk-std()-Z       | tBodyGyroJerk-std()-Z       |
| tBodyAccMag-mean()          | tBodyAccMag-mean()          |
| tBodyAccMag-std()           | tBodyAccMag-std()           |
| tGravityAccMag-mean()       | tGravityAccMag-mean()       |
| tGravityAccMag-std()        | tGravityAccMag-std()        |
| tBodyAccJerkMag-mean()      | tBodyAccJerkMag-mean()      |
| tBodyAccJerkMag-std()       | tBodyAccJerkMag-std()       |
| tBodyGyroMag-mean()         | tBodyGyroMag-mean()         |
| tBodyGyroMag-std()          | tBodyGyroMag-std()          |
| tBodyGyroJerkMag-mean()     | tBodyGyroJerkMag-mean()     |
| tBodyGyroJerkMag-std()      | tBodyGyroJerkMag-std()      |
| fBodyAcc-mean()-X           | fBodyAcc-mean()-X           |
| fBodyAcc-mean()-Y           | fBodyAcc-mean()-Y           |
| fBodyAcc-mean()-Z           | fBodyAcc-mean()-Z           |
| fBodyAcc-std()-X            | fBodyAcc-std()-X            |
| fBodyAcc-std()-Y            | fBodyAcc-std()-Y            |
| fBodyAcc-std()-Z            | fBodyAcc-std()-Z            |
| fBodyAccJerk-mean()-X       | fBodyAccJerk-mean()-X       |
| fBodyAccJerk-mean()-Y       | fBodyAccJerk-mean()-Y       |
| fBodyAccJerk-mean()-Z       | fBodyAccJerk-mean()-Z       |
| fBodyAccJerk-std()-X        | fBodyAccJerk-std()-X        |
| fBodyAccJerk-std()-Y        | fBodyAccJerk-std()-Y        |
| fBodyAccJerk-std()-Z        | fBodyAccJerk-std()-Z        |
| fBodyGyro-mean()-X          | fBodyGyro-mean()-X          |
| fBodyGyro-mean()-Y          | fBodyGyro-mean()-Y          |
| fBodyGyro-mean()-Z          | fBodyGyro-mean()-Z          |
| fBodyGyro-std()-X           | fBodyGyro-std()-X           |
| fBodyGyro-std()-Y           | fBodyGyro-std()-Y           |
| fBodyGyro-std()-Z           | fBodyGyro-std()-Z           |
| fBodyAccMag-mean()          | fBodyAccMag-mean()          |
| fBodyAccMag-std()           | fBodyAccMag-std()           |
| fBodyBodyAccJerkMag-mean()  | fBodyBodyAccJerkMag-mean()  |
| fBodyBodyAccJerkMag-std()   | fBodyBodyAccJerkMag-std()   |
| fBodyBodyGyroMag-mean()     | fBodyBodyGyroMag-mean()     |
| fBodyBodyGyroMag-std()      | fBodyBodyGyroMag-std()      |
| fBodyBodyGyroJerkMag-mean() | fBodyBodyGyroJerkMag-mean() |
| fBodyBodyGyroJerkMag-std()  | fBodyBodyGyroJerkMag-std()  |
