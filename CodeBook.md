# Code Book

## Study Design
The data used for this project was provided in the zip file below, and was collected from accelerometers from the Samsung Galaxy S smartphone used by the subjects:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
This data was originally obtained from the website:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
This data was untidy with the aim of the assignment being to collect and work with data, and tidy a dataset. To do, I downloaded the zip file and unzipped it, placing all the necessary files into folder in my PC. First, I loaded the necessary packages needed to clean the data, then I set my working directory to that specific folder. I loaded the files into R and gave them unique column names before binding them together to create one dataset. After that, I extracted first two columns along with the columns containing the terms “mean” and “std”, and then I used the activity labels to replace the values in column 2, and thus explain which levels of activity received which values. I then changed the column names by removing the special characters and making them more descriptive. Lastly, I created a tidy data set based on this data set that took the mean of each group of activity per variable and per subject.

## Codebook/Variables
mean = Mean value
std = Standard deviation value

These are the variables using the original names from the features.txt file:
 [1] "Subject"                        	 "Activity"                       
 [3] "tBodyAcc-mean()-X"              "tBodyAcc-mean()-Y"              
 [5] "tBodyAcc-mean()-Z"              "tBodyAcc-std()-X"               
 [7] "tBodyAcc-std()-Y"               	 "tBodyAcc-std()-Z"               
 [9] "tGravityAcc-mean()-X"          "tGravityAcc-mean()-Y"           
[11] "tGravityAcc-mean()-Z"         "tGravityAcc-std()-X"            
[13] "tGravityAcc-std()-Y"              "tGravityAcc-std()-Z"            
[15] "tBodyAccJerk-mean()-X"      "tBodyAccJerk-mean()-Y"          
[17] "tBodyAccJerk-mean()-Z"       "tBodyAccJerk-std()-X"           
[19] "tBodyAccJerk-std()-Y"            "tBodyAccJerk-std()-Z"           
[21] "tBodyGyro-mean()-X"            "tBodyGyro-mean()-Y"             
[23] "tBodyGyro-mean()-Z"             "tBodyGyro-std()-X"              
[25] "tBodyGyro-std()-Y"                  "tBodyGyro-std()-Z"              
[27] "tBodyGyroJerk-mean()-X"      "tBodyGyroJerk-mean()-Y"         
[29] "tBodyGyroJerk-mean()-Z"      "tBodyGyroJerk-std()-X"          
[31] "tBodyGyroJerk-std()-Y"           "tBodyGyroJerk-std()-Z"          
[33] "tBodyAccMag-mean()"           "tBodyAccMag-std()"              
[35] "tGravityAccMag-mean()"       "tGravityAccMag-std()"           
[37] "tBodyAccJerkMag-mean()"    "tBodyAccJerkMag-std()"          
[39] "tBodyGyroMag-mean()"          "tBodyGyroMag-std()"             
[41] "tBodyGyroJerkMag-mean()"   "tBodyGyroJerkMag-std()"         
[43] "fBodyAcc-mean()-X"                 "fBodyAcc-mean()-Y"              
[45] "fBodyAcc-mean()-Z"                 "fBodyAcc-std()-X"               
[47] "fBodyAcc-std()-Y"                      "fBodyAcc-std()-Z"               
[49] "fBodyAcc-meanFreq()-X"         "fBodyAcc-meanFreq()-Y"          
[51] "fBodyAcc-meanFreq()-Z"         "fBodyAccJerk-mean()-X"          
[53] "fBodyAccJerk-mean()-Y"          "fBodyAccJerk-mean()-Z"          
[55] "fBodyAccJerk-std()-X"              "fBodyAccJerk-std()-Y"           
[57] "fBodyAccJerk-std()-Z"              "fBodyAccJerk-meanFreq()-X"      
[59] "fBodyAccJerk-meanFreq()-Y”  "fBodyAccJerk-meanFreq()-Z"      
[61] "fBodyGyro-mean()-X"               "fBodyGyro-mean()-Y"             
[63] "fBodyGyro-mean()-Z"               "fBodyGyro-std()-X"              
[65] "fBodyGyro-std()-Y"                    "fBodyGyro-std()-Z"              
[67] "fBodyGyro-meanFreq()-X"       "fBodyGyro-meanFreq()-Y"         
[69] "fBodyGyro-meanFreq()-Z"       "fBodyAccMag-mean()"             
[71] "fBodyAccMag-std()"                 "fBodyAccMag-meanFreq()"         
[73] "fBodyBodyAccJerkMag-mean()" "fBodyBodyAccJerkMag-std()"      
[75] "fBodyBodyAccJerkMag-meanFreq()"  "fBodyBodyGyroMag-mean()"        
[77] "fBodyBodyGyroMag-std()"          "fBodyBodyGyroMag-meanFreq()"    
[79] "fBodyBodyGyroJerkMag-mean()"     "fBodyBodyGyroJerkMag-std()"     
[81] "fBodyBodyGyroJerkMag-meanFreq()"

These are the variables using the changed names in the new tidy data set:
 [1] "Subject"                                                       
 [2] "Activity"                                                      
 [3] "timeDomainBodyAccelerometerMeanX"                              
 [4] "timeDomainBodyAccelerometerMeanY"                              
 [5] "timeDomainBodyAccelerometerMeanZ"                              
 [6] "timeDomainBodyAccelerometerStandardDeviationX"                 
 [7] "timeDomainBodyAccelerometerStandardDeviationY"                 
 [8] "timeDomainBodyAccelerometerStandardDeviationZ"                 
 [9] "timeDomainGravityAccelerometerMeanX"                           
[10] "timeDomainGravityAccelerometerMeanY"                           
[11] "timeDomainGravityAccelerometerMeanZ"                           
[12] "timeDomainGravityAccelerometerStandardDeviationX"              
[13] "timeDomainGravityAccelerometerStandardDeviationY"              
[14] "timeDomainGravityAccelerometerStandardDeviationZ"              
[15] "timeDomainBodyAccelerometerJerkMeanX"                          
[16] "timeDomainBodyAccelerometerJerkMeanY"                          
[17] "timeDomainBodyAccelerometerJerkMeanZ"                          
[18] "timeDomainBodyAccelerometerJerkStandardDeviationX"             
[19] "timeDomainBodyAccelerometerJerkStandardDeviationY"             
[20] "timeDomainBodyAccelerometerJerkStandardDeviationZ"             
[21] "timeDomainBodyGyroscopeMeanX"                                  
[22] "timeDomainBodyGyroscopeMeanY"                                  
[23] "timeDomainBodyGyroscopeMeanZ"                                  
[24] "timeDomainBodyGyroscopeStandardDeviationX"                     
[25] "timeDomainBodyGyroscopeStandardDeviationY"                     
[26] "timeDomainBodyGyroscopeStandardDeviationZ"                     
[27] "timeDomainBodyGyroscopeJerkMeanX"                              
[28] "timeDomainBodyGyroscopeJerkMeanY"                              
[29] "timeDomainBodyGyroscopeJerkMeanZ"                              
[30] "timeDomainBodyGyroscopeJerkStandardDeviationX"                 
[31] "timeDomainBodyGyroscopeJerkStandardDeviationY"                 
[32] "timeDomainBodyGyroscopeJerkStandardDeviationZ"                 
[33] "timeDomainBodyAccelerometerMagnitudeMean"                      
[34] "timeDomainBodyAccelerometerMagnitudeStandardDeviation"         
[35] "timeDomainGravityAccelerometerMagnitudeMean"                   
[36] "timeDomainGravityAccelerometerMagnitudeStandardDeviation"      
[37] "timeDomainBodyAccelerometerJerkMagnitudeMean"                  
[38] "timeDomainBodyAccelerometerJerkMagnitudeStandardDeviation"     
[39] "timeDomainBodyGyroscopeMagnitudeMean"                          
[40] "timeDomainBodyGyroscopeMagnitudeStandardDeviation"             
[41] "timeDomainBodyGyroscopeJerkMagnitudeMean"                      
[42] "timeDomainBodyGyroscopeJerkMagnitudeStandardDeviation"         
[43] "frequencyDomainBodyAccelerometerMeanX"                         
[44] "frequencyDomainBodyAccelerometerMeanY"                         
[45] "frequencyDomainBodyAccelerometerMeanZ"                         
[46] "frequencyDomainBodyAccelerometerStandardDeviationX"            
[47] "frequencyDomainBodyAccelerometerStandardDeviationY"            
[48] "frequencyDomainBodyAccelerometerStandardDeviationZ"            
[49] "frequencyDomainBodyAccelerometerMeanFrequencyX"                
[50] "frequencyDomainBodyAccelerometerMeanFrequencyY"                
[51] "frequencyDomainBodyAccelerometerMeanFrequencyZ"                
[52] "frequencyDomainBodyAccelerometerJerkMeanX"                     
[53] "frequencyDomainBodyAccelerometerJerkMeanY"                     
[54] "frequencyDomainBodyAccelerometerJerkMeanZ"                     
[55] "frequencyDomainBodyAccelerometerJerkStandardDeviationX"        
[56] "frequencyDomainBodyAccelerometerJerkStandardDeviationY"        
[57] "frequencyDomainBodyAccelerometerJerkStandardDeviationZ"        
[58] "frequencyDomainBodyAccelerometerJerkMeanFrequencyX"            
[59] "frequencyDomainBodyAccelerometerJerkMeanFrequencyY"            
[60] "frequencyDomainBodyAccelerometerJerkMeanFrequencyZ"            
[61] "frequencyDomainBodyGyroscopeMeanX"                             
[62] "frequencyDomainBodyGyroscopeMeanY"                             
[63] "frequencyDomainBodyGyroscopeMeanZ"                             
[64] "frequencyDomainBodyGyroscopeStandardDeviationX"                
[65] "frequencyDomainBodyGyroscopeStandardDeviationY"                
[66] "frequencyDomainBodyGyroscopeStandardDeviationZ"                
[67] "frequencyDomainBodyGyroscopeMeanFrequencyX"                    
[68] "frequencyDomainBodyGyroscopeMeanFrequencyY"                    
[69] "frequencyDomainBodyGyroscopeMeanFrequencyZ"                    
[70] "frequencyDomainBodyAccelerometerMagnitudeMean"                 
[71] "frequencyDomainBodyAccelerometerMagnitudeStandardDeviation"    
[72] "frequencyDomainBodyAccelerometerMagnitudeMeanFrequency"        
[73] "frequencyDomainBodyAccelerometerJerkMagnitudeMean"             
[74] "frequencyDomainBodyAccelerometerJerkMagnitudeStandardDeviation"
[75] "frequencyDomainBodyAccelerometerJerkMagnitudeMeanFrequency"    
[76] "frequencyDomainBodyGyroscopeMagnitudeMean"                     
[77] "frequencyDomainBodyGyroscopeMagnitudeStandardDeviation"        
[78] "frequencyDomainBodyGyroscopeMagnitudeMeanFrequency"            
[79] "frequencyDomainBodyGyroscopeJerkMagnitudeMean"                 
[80] "frequencyDomainBodyGyroscopeJerkMagnitudeStandardDeviation"    
[81] "frequencyDomainBodyGyroscopeJerkMagnitudeMeanFrequency"
