**1.Download and unzip the data file under current working directly.** <br />
**2.Set “./UCI HAR Dataset” as working directly by setwd().**<br />
This run_analysis.R script perform the following work about this data file:<br />
  *1).Reformat the test and train data set separately, replace column names with measurement variables information. Two additional columns with subject and activity information are added to each data set.<br />
  *2). Merge two data sets (train and test) into complete data set (completedata)
  *3). Subset data (completedata) from step2 only with column containing activity, subject, mean(), and std(). The columns names with “meanFreq()” is not included.<br />
  *4). Replace column “activity”'s content with 6 activities: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING. It saves into a data file called completedata_sub.<br />
  *5). Use reshape2 library to melt and dcast the completedata_sub file using “subject” and “activity” as ID variable. Calculate mean for the measurement variables.<br /> 
  *6). Run source file (run_analysis.R), it will generate “tidy_data.txt” under folder UCI HAR Dataset.




