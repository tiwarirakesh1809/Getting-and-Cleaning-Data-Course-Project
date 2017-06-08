# Getting-and-Cleaning-Data-Course-Project
Course Project for Coursera "Getting and Cleaning Data"
The R script in this repository "run_analysis.R" does the below described tasks to achieve the project goal:

1. Download the dataset if it does not already exist in the working directory
2. Load the activity and feature info
3. Loads both the training and test datasets, keeping only those columns which reflect a mean or standard deviation
4. Loads the activity and subject data for each dataset, and merges those columns with the dataset
5. Merges the two datasets, Converts the activity and subject columns into factors
6. Creates a tidy dataset that consists of the average (mean) value of each variable for each subject and activity pair.

# Files Description
CodeBook.md describes the variables, the data, and any transformations or work that was performed to clean up the data.

run_analysis.R contains all the code to perform the analyses described. They can be launched in RStudio by just importing the file.

The output of the 5th step is called "secTidySet.txt".
