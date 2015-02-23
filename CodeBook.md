# Code Book-
this is a code book for getting and cleaning data course project.

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

# tidy data
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
| ---------------------------- | --------------------------- |
|                              | Activity                    |
|                              | Subject                     |
| Time.BodyAcc.Mean.X          | tBodyAcc-mean()-X           |
| Time.BodyAcc.Mean.Y          | tBodyAcc-mean()-Y           |
| Time.BodyAcc.Mean.Z          | tBodyAcc-mean()-Z           |
| Time.BodyAcc.Std.X           | tBodyAcc-std()-X            |
| Time.BodyAcc.Std.Y           | tBodyAcc-std()-Y            |
| Time.BodyAcc.Std.Z           | tBodyAcc-std()-Z            |
| Time.GravityAcc.Mean.X       | tGravityAcc-mean()-X        |
| Time.GravityAcc.Mean.Y       | tGravityAcc-mean()-Y        |
| Time.GravityAcc.Mean.Z       | tGravityAcc-mean()-Z        |
| Time.GravityAcc.Std.X        | tGravityAcc-std()-X         |
| Time.GravityAcc.Std.Y        | tGravityAcc-std()-Y         |
| Time.GravityAcc.Std.Z        | tGravityAcc-std()-Z         |
| Time.BodyAccJerk.Mean.X      | tBodyAccJerk-mean()-X       |
| Time.BodyAccJerk.Mean.Y      | tBodyAccJerk-mean()-Y       |
| Time.BodyAccJerk.Mean.Z      | tBodyAccJerk-mean()-Z       |
| Time.BodyAccJerk.Std.X       | tBodyAccJerk-std()-X        |
| Time.BodyAccJerk.Std.Y       | tBodyAccJerk-std()-Y        |
| Time.BodyAccJerk.Std.Z       | tBodyAccJerk-std()-Z        |
| Time.BodyGyro.Mean.X         | tBodyGyro-mean()-X          |
| Time.BodyGyro.Mean.Y         | tBodyGyro-mean()-Y          |
| Time.BodyGyro.Mean.Z         | tBodyGyro-mean()-Z          |
| Time.BodyGyro.Std.X          | tBodyGyro-std()-X           |
| Time.BodyGyro.Std.Y          | tBodyGyro-std()-Y           |
| Time.BodyGyro.Std.Z          | tBodyGyro-std()-Z           |
| Time.BodyGyroJerk.Mean.X     | tBodyGyroJerk-mean()-X      |
| Time.BodyGyroJerk.Mean.Y     | tBodyGyroJerk-mean()-Y      |
| Time.BodyGyroJerk.Mean.Z     | tBodyGyroJerk-mean()-Z      |
| Time.BodyGyroJerk.Std.X      | tBodyGyroJerk-std()-X       |
| Time.BodyGyroJerk.Std.Y      | tBodyGyroJerk-std()-Y       |
| Time.BodyGyroJerk.Std.Z      | tBodyGyroJerk-std()-Z       |
| Time.BodyAccMag.Mean         | tBodyAccMag-mean()          |
| Time.BodyAccMag.Std          | tBodyAccMag-std()           |
| Time.GravityAccMag.Mean      | tGravityAccMag-mean()       |
| Time.GravityAccMag.Std       | tGravityAccMag-std()        |
| Time.BodyAccJerkMag.Mean     | tBodyAccJerkMag-mean()      |
| Time.BodyAccJerkMag.Std      | tBodyAccJerkMag-std()       |
| Time.BodyGyroMag.Mean        | tBodyGyroMag-mean()         |
| Time.BodyGyroMag.Std         | tBodyGyroMag-std()          |
| Time.BodyGyroJerkMag.Mean    | tBodyGyroJerkMag-mean()     |
| Time.BodyGyroJerkMag.Std     | tBodyGyroJerkMag-std()      |
| FFT.BodyAcc.Mean.X           | fBodyAcc-mean()-X           |
| FFT.BodyAcc.Mean.Y           | fBodyAcc-mean()-Y           |
| FFT.BodyAcc.Mean.Z           | fBodyAcc-mean()-Z           |
| FFT.BodyAcc.Std.X            | fBodyAcc-std()-X            |
| FFT.BodyAcc.Std.Y            | fBodyAcc-std()-Y            |
| FFT.BodyAcc.Std.Z            | fBodyAcc-std()-Z            |
| FFT.BodyAccJerk.Mean.X       | fBodyAccJerk-mean()-X       |
| FFT.BodyAccJerk.Mean.Y       | fBodyAccJerk-mean()-Y       |
| FFT.BodyAccJerk.Mean.Z       | fBodyAccJerk-mean()-Z       |
| FFT.BodyAccJerk.Std.X        | fBodyAccJerk-std()-X        |
| FFT.BodyAccJerk.Std.Y        | fBodyAccJerk-std()-Y        |
| FFT.BodyAccJerk.Std.Z        | fBodyAccJerk-std()-Z        |
| FFT.BodyGyro.Mean.X          | fBodyGyro-mean()-X          |
| FFT.BodyGyro.Mean.Y          | fBodyGyro-mean()-Y          |
| FFT.BodyGyro.Mean.Z          | fBodyGyro-mean()-Z          |
| FFT.BodyGyro.Std.X           | fBodyGyro-std()-X           |
| FFT.BodyGyro.Std.Y           | fBodyGyro-std()-Y           |
| FFT.BodyGyro.Std.Z           | fBodyGyro-std()-Z           |
| FFT.BodyAccMag.Mean          | fBodyAccMag-mean()          |
| FFT.BodyAccMag.Std           | fBodyAccMag-std()           |
| FFT.BodyBodyAccJerkMag.Mean  | fBodyBodyAccJerkMag-mean()  |
| FFT.BodyBodyAccJerkMag.Std   | fBodyBodyAccJerkMag-std()   |
| FFT.BodyBodyGyroMag.Mean     | fBodyBodyGyroMag-mean()     |
| FFT.BodyBodyGyroMag.Std      | fBodyBodyGyroMag-std()      |
| FFT.BodyBodyGyroJerkMag.Mean | fBodyBodyGyroJerkMag-mean() |
| FFT.BodyBodyGyroJerkMag.Std  | fBodyBodyGyroJerkMag-std()  |
