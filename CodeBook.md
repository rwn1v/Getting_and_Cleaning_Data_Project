## CodeBook

This is a code book that describes the variables, the data, and transformations performed to clean up the data.

The data source of original data:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
 
Description:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

## Data Set Information

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

## Input Data Description

The dataset includes the following files:

-  'README.txt'

-  'features_info.txt': Shows information about the variables used on the feature vector.

-  'features.txt': List of all features.

-  'activity_labels.txt': Links the class labels with their activity name.

-  'test/X_test.txt': Test set.

-  'test/y_test.txt': Test labels.

-  'train/X_train.txt': Training set.

-  'train/y_train.txt': Training labels.


The following files are available for the test and train data. Their descriptions are equivalent.

-   'test/subject_test.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.

-   'test/Inertial Signals/total_acc_x_test.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_test.txt' and 'total_acc_z_test.txt' files for the Y and Z axis.

-   'test/Inertial Signals/body_acc_x_test.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration.

-   'test/Inertial Signals/body_gyro_x_test.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second.

## Transformation Details

-   The training and the test sets were merged to create one data set.
-   Mean and standard deviation were extracted from measurements.
-   Descriptive activity names were used to name the activities in the data set.
-   The data set was labled with descriptive activity names.
-   Tidy data set was created containing the average of each variable for each activity and each subject.

## Workflow of run_analysis.R:

-   Require reshapre2 and data.table.
-   Load both test and train data.
-   Load the features and activity labels.
-   Extract the mean and standard deviation column names and data.
-   Process the data. There are two parts processing test and train data respectively.
-   Merge data set.
