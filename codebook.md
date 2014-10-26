# Codebook for Course Project

### Repo Info

This Repo has been created for the Course Project of Getting and Cleaning Data Course by Coursera.

### Background

Wearable Computing is the next big wave in computing. UCI Machine Learning Data Set Library has a data set titled [Human Activity Recognition Using Smartphones Data Set] (http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) which lists the data from 30 users who were wearing a wearable computing device. The data includes the readings of various sensors in the device and the activity of the person (walking, standing etc)

### Data

The dataset may be downloaded from [here] (http://archive.ics.uci.edu/ml/machine-learning-databases/00240/) . The explanation regarding the variables are available in the Readme file. 

### Process

The whole process may be divided into 5 steps.

* Merging Testing and Training Data Sets

The components of training and testing data sets were individually read into corresponding data frames, which were integrated using cbind.data.frame() function to provide two data sets. These were then integrated using rbind.data.frame() to produce one data set. This resulted in a data set with 10299 rows and 563 columns.

* Choosing columns about Mean or Standard Deviation

"features.txt" file contains information regarding the columns of the dataset. Using this information, all columns containing mean() or std() in the name were retained. This resulted in a data set with 81 columns. The names from features.txt were attributed to the data frame columns.

* Giving Proper activity names

The files Y_Train.txt and Y_Test.txt contained information regarding the state of the user in a numeric form. The explanation is given in file Activity Labels.txt which explains the state corresponding to each numbers in this column as 1 : WALKING, 2 : WALKING_UPSTAIRS, 3 : WALKING_DOWNSTAIRS, 4 : SITTING, 5 : STANDING and 6 : LAYING. These character values were attributed to the data frame after converting the activity field into a factor.

* Giving Descriptive Variable Names

Proper Variable Names were given by using Regular expressions to expand the existing variable names. The codebook that came with the data set was used to identify how to properly expand the column names. 

* Aggregate data with means

The aggregate function of R was used to aggregate the data grouped by activity per subject. This was then written to a file using the write.table function.










