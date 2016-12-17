Getting and cleaning data week4 project

purpose

The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 
1. a tidy data set as described below;
2. a link to a Github repository with your script for performing the analysis
3. a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. 
4. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.


Objectives:You should create one R script called run_analysis.R that does the following:

1.Merges the training and the test sets to create one data set.

2.Extracts only the measurements on the mean and standard deviation for each measurement.

3.Uses descriptive activity names to name the activities in the data set

4.Appropriately labels the data set with descriptive variable names.

5.From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.


run_analysis.R

1.It downloads the UCI HAR Dataset data set and puts the zip file working directrory. After it is downloaded, it unzips the file into the UCI HAR Dataset folder.

2.It loads the train and test data sets and appends the two datasets into one data frame. This is done using cbind and rbind function. 

3.It load feature name into R, extract mean and standard deviation of each measurement. This is done using grep function.

4.It load activity data into R, and replace 1 to 6 with activity names.

5.Appropriately labels the data set with descriptive variable names. This is done using gsub function.

6. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject. This is done using dylyr package, and group_by function, and summarise_each function. The mean of activities and subjects are created into a separate tidy data set which is exported into the Project folder as txt file; this is named “MeanData.txt”.


