Getting and Cleaning Data Course Project - CodeBook

This file describes the variables, the data, and the work performed for cleaning up the data.

    The site where the data was obtained:
  
    http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 

    The data for the project:
    
    https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

    The run_analysis.R script is written to perform the following tasks for the cleaning of the data:
       
	1. Read X_train.txt, y_train.txt and subject_train.txt from the "./UCI HAR Dataset/train" folder and store them in trainData, trainLabel and trainSubject variables respectively.

        2. Read X_test.txt, y_test.txt and subject_test.txt from the "./UCI HAR Dataset/test" folder and store them in testData, testLabel and testSubject variables respectively.

        3. Join trainData and testData together into a dataframe called joinedData; trainLabel and testLabel into dataframe, joinedLabel; trainSubject and testSubject into dataframe, joinedSubject.
       
	4. Combined all the three dataframes - joinedSubject, joinedLabel and joinedData into one dataset called mergedData.
 	
	5. Generate first 6 rows of mergedData for viewing/checking.
	
	6. Read the features.txt file from the "./UCI HAR Dataset" folder and store the data in a variable called features. 
        
	7. Extract only the measurements on the mean and standard deviation. There are 66 results. 
        
	8. Subset the joinedData with the 66 corresponding columns and store as extractedData.
	
	9. Generate first 6 rows of extractedData for viewing/checking.
 
        10.Read the activity_labels.txt file from the "./UCI HAR Dataset" folder and store the data in a variable called activity.
        
	11.Clean the activity names in the second column of activity.  This includes making all the names to lower cases and if the name has an underscore between letters, replace it with empty space.
        
	12.Change the values of joinedLabel according to the activity dataframe.

	13.Generate first 6 rows of joinedLabel to show changes made.

	14.Name the first two columns, "Subject" and "Activity". 

	15.Label the name of the columns in the dataframe, extractedData.
        
	16.Combine the joinedSubject, joinedLabel and extractedData by column to get the cleaned dataset and store as firstData. 

	17.Generate first 6 rows of firstData to show labels changed and the combination of data.
	
	18.Write the firstData out to "first_dataset.txt" file in current working directory.

        19.Generate a second independent tidy dataset with the average of each measurement for each activity and each subject, then store as secondData.

        20.Write the secondData out to "tidy_dataset.txt" file in current working directory.
