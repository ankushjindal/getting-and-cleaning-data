# CodeBook

This is a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data.

## The data source

* Original data: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
* Original description of the dataset: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

## Data Set Information

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

## The data

The dataset includes the following files:

- 'README.txt'

- 'features_info.txt': Shows information about the variables used on the feature vector.

- 'features.txt': List of all features.

- 'activity_labels.txt': Links the class labels with their activity name.

- 'train/X_train.txt': Training set.

- 'train/y_train.txt': Training labels.

- 'test/X_test.txt': Test set.

- 'test/y_test.txt': Test labels.

The following files are available for the train and test data. Their descriptions are equivalent.

- 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.

- 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis.

- 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration.

- 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second.

## Transformation details

There are 5 parts:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive activity names.
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.


Variables in final tidy data matrix
-----------------------------------
[1] "Subject"
------------
Range: integer from 1 to 30

Unit: None 

Description: Subject is the identifier of the person who carries out the experiments wearing a smartphone (Samsung Galaxy S II) on the waist. 30 volunteers within an age bracket of 19-48 years.

[2] "Activity"
--------------
Range: integer 1 to 6

Unit: None

Description: Six activities are as coded as below. 

1 - WALKING

2 - WALKING_UPSTAIRS

3 - WALKING_DOWNSTAIRS

4 - SITTING

5 - STANDING

6 - LAYING

Variables [3] to [81]
----------------------
Range: Normalized and bounded within [-1,1] and hence have no unit

Unit: None

Description: Features selected for come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern: '-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.
tBodyAcc-XYZ
tGravityAcc-XYZ
tBodyAccJerk-XYZ
tBodyGyro-XYZ
tBodyGyroJerk-XYZ
tBodyAccMag
tGravityAccMag
tBodyAccJerkMag
tBodyGyroMag
tBodyGyroJerkMag
fBodyAcc-XYZ
fBodyAccJerk-XYZ
fBodyGyro-XYZ
fBodyAccMag
fBodyAccJerkMag
fBodyGyroMag
fBodyGyroJerkMag

The set of variables that were estimated from these signals are: 
mean(): Mean value and std(): Standard deviation

[3] "tBodyAcc-mean-X"

[4] "tBodyAcc-mean-Y"

[5] "tBodyAcc-mean-Z"

[6] "tGravityAcc-mean-X"

[7] "tGravityAcc-mean-Y"

[8] "tGravityAcc-mean-Z"

[9] "tBodyAccJerk-mean-X"

[10] "tBodyAccJerk-mean-Y"      

[11] "tBodyAccJerk-mean-Z"

[12] "tBodyGyro-mean-X"         

[13] "tBodyGyro-mean-Y"

[14] "tBodyGyro-mean-Z"         

[15] "tBodyGyroJerk-mean-X"

[16] "tBodyGyroJerk-mean-Y"     

[17] "tBodyGyroJerk-mean-Z"

[18] "tBodyAccMag-mean"

[19] "tGravityAccMag-mean"

[20] "tBodyAccJerkMag-mean"     

[21] "tBodyGyroMag-mean"

[22] "tBodyGyroJerkMag-mean"    

[23] "fBodyAcc-mean-X"

[24] "fBodyAcc-mean-Y"          

[25] "fBodyAcc-mean-Z"           

[26] "fBodyAcc-meanFreq-X"      

[27] "fBodyAcc-meanFreq-Y"

[28] "fBodyAcc-meanFreq-Z"      

[29] "fBodyAccJerk-mean-X"

[30] "fBodyAccJerk-mean-Y"      

[31] "fBodyAccJerk-mean-Z"

[32] "fBodyAccJerk-meanFreq-X"  

[33] "fBodyAccJerk-meanFreq-Y"

[34] "fBodyAccJerk-meanFreq-Z"  

[35] "fBodyGyro-mean-X"

[36] "fBodyGyro-mean-Y"         

[37] "fBodyGyro-mean-Z" 

[38] "fBodyGyro-meanFreq-X"     

[39] "fBodyGyro-meanFreq-Y"

[40] "fBodyGyro-meanFreq-Z"     

[41] "fBodyAccMag-mean"

[42] "fBodyAccMag-meanFreq"     

[43] "fBodyAccJerkMag-mean"

[44] "fBodyAccJerkMag-meanFreq" 

[45] "fBodyGyroMag-mean"

[46] "fBodyGyroMag-meanFreq"    

[47] "fBodyGyroJerkMag-mean"

[48] "fBodyGyroJerkMag-meanFreq"

[49] "tBodyAcc-std-X"           

[50] "tBodyAcc-std-Y"           

[51] "tBodyAcc-std-Z"         

[52] "tGravityAcc-std-X"        

[53] "tGravityAcc-std-Y"        

[54] "tGravityAcc-std-Z"        

[55] "tBodyAccJerk-std-X"

[56] "tBodyAccJerk-std-Y"       

[57] "tBodyAccJerk-std-Z" 

[58] "tBodyGyro-std-X"          

[59] "tBodyGyro-std-Y"

[60] "tBodyGyro-std-Z"          

[61] "tBodyGyroJerk-std-X"    

[62] "tBodyGyroJerk-std-Y"      

[63] "tBodyGyroJerk-std-Z"

[64] "tBodyAccMag-std"          

[65] "tGravityAccMag-std"

[66] "tBodyAccJerkMag-std"      

[67] "tBodyGyroMag-std"

[68] "tBodyGyroJerkMag-std"     

[69] "fBodyAcc-std-X"

[70] "fBodyAcc-std-Y"           

[71] "fBodyAcc-std-Z"

[72] "fBodyAccJerk-std-X"       

[73] "fBodyAccJerk-std-Y" 

[74] "fBodyAccJerk-std-Z"       

[75] "fBodyGyro-std-X"

[76] "fBodyGyro-std-Y"          

[77] "fBodyGyro-std-Z"    

[78] "fBodyAccMag-std"          

[79] "fBodyAccJerkMag-std"

[80] "fBodyGyroMag-std"         

[81] "fBodyGyroJerkMag-std" 


## How ```run_analysis.R``` implements the above steps:

* Require ```reshapre2``` and ```data.table``` librareis.
* Load both test and train data
* Load the features and activity labels.
* Extract the mean and standard deviation column names and data.
* Process the data. There are two parts processing test and train data respectively.
* Merge data set.
