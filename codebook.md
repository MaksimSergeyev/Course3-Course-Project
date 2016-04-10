Source of the original data:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Description of data was obtained from:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Process:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names.
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

I began by reading in all of the various files into the variables described below. I then merged each set for the three variables into a single set for each variable. I then extracted the columns containing mean and st. dev values. I then set activity names using activites as a factor. I then added more detailed names to replace the abbreviated names. I then extracted the data using subject as a factor.

Variables:

featurenames = data read in from features file
activityLabels = data read in from activity labels file
subjectTrain = data read in from subject train file
activityTrain = data read in from activity train file
featuresTrain = data read in from features train file
subjectTest = data read in from subject test file
activityTest = data read in from activity test file
featuresTest = data read in from features test file
subject = combined test and train subject data
activity = combined test and train activity data
features = combined test and train features data
columnsWithMeanSTD = extracted column of mean and std values

Output:

The output of this script is a data table called Tidy.txt
The table written in the file, tidyData is a 180 x 88 data frame.
The first column is the subject column. The final column is Angle(Z, GravityMean)