###1.Download and unzip the file under current working directly. 
###2. Create run_analysis.R under folder “UCI HAR Dataset”. Set “./UCI HAR Dataset” as working directly by setwd().
This run_analysis.R script perform the following work about this data file:
  *Reformat the test and train data set separately, using measurement variables as column names. Two separate columns subject  and 6 activities are added to each data set.
  * Merge two data sets (train and test) into complete data set (completedata)
  * Subset completedata from step2 with column names containing activity, subject, mean(), and std(). The columns names with   “meanFreq()” is not considered as mean value calculation since it is weighted average of the frequency components to obtain a mean frequency.
  * Replace column “ activity” with meaning content (6 activities: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING). It creates a data file called completedata_sub.
  * Use reshape2 library to melt and dcast the completedata_sub file using “subject” and “activity” as ID variable. Calculate mean for the measurement variables. 
### 3. Run source(run_analysis.R), it will generate “tidy.data.txt” under folder UCI HAR Dataset.



