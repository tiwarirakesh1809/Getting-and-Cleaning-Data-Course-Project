# This code book of "run_analysis.R" describes the variables, the data, and the transformations or work that I have performed to clean up the data as "secTidySet.txt"

#Identifiers

activityId- The ID of the activity
activityType - The type of activity performed when the corresponding measurements were taken
subjectId - The ID of the subject

# Code Working Flow

     call the working Library
1.   Downloading and unzipping dataset

2.   Merging the training and the test sets to create one data set:
2.1. Read the downloaded unzipped files and Reading trainings tables, testing tables,features.txt and activity labels.
2.2. Assigning column names:
2.3. Merging all data in one set:
3.   Extracting only the measurements on the mean and standard deviation for each measurement
3.1. Reading column names:
3.2. Create vector for defining ID, mean and standard deviation:
3.3. Making nessesary subset from setAllInOne:
4.   Using descriptive activity names to name the activities in the data set:
5.   Creating a second, independent tidy data set with the average of each variable for each activity and each subject:
5.2. Writing second tidy data set in txt file
     Optional Final Step- To Visualize the Output by view() function

# Variables 

x_train, y_train, x_test, y_test, subject_train, subject_test, features and activityLabels contain the data from the downloaded files.

merged_train and merged_test to store mergerd test and train values after applying cbind() function.

setAllInOne by performing rbind on merged_train and merged_test.

mean_and_std by creating vector for defining ID, mean and standard deviation using grepl() function. setForMeanAndStd by setting all columns where mean_and_std was TRUE.

setWithActivityNames stored merged data by applying merge() function on setForMeanAndStd, activityLabels by= "activityId" and setting all.x = TRUE.

secTidySet, by using aggregate() function on data=  setWithActivityNames and FUN= mean and then used order() function and stored the result in secTidySet.

secTidySet.txt- txt file created with write.table() using row.name=FALSE
