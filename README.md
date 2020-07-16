The experiments were carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. The obtained dataset was randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The original dataset included the following statistics:

mean(): Mean value
std(): Standard deviation 
mad(): Median absolute deviation
max(): Largest value in array
min(): Smallest value in array
sma(): Signal magnitude area
energy(): Energy measure. Sum of the squares divided by the number of values.
iqr(): Interquartile range
entropy(): Signal entropy
arCoeff(): Autorregresion coefficients with Burg order equal to 4
correlation(): correlation coefficient between two signals
maxInds(): index of the frequency component with largest magnitude
meanFreq(): Weighted average of the frequency components to obtain a mean frequency
skewness(): skewness of the frequency domain signal
kurtosis(): kurtosis of the frequency domain signal
bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window.


From the original data set a series of steps were followed in order to obtain a tidy data set for further postprocessing. To carry out this process the [run_analysis.R] script was used. A general overview includes:

Merging the training and the test subjects into a single dataset.
Extracting only the measurements corresponding to the mean and standard deviation for each available measurement.
Joining the subjects with the activities performed by the subjects with the measurements from the dataset.
Evaluating the mean per subject and activity of the available meassurements and sorting by subject and activity.
Saving the resulting dataset in a text file.
Saving the dataset column names in a text file.
The resulting dataset [tidytext.txt] contains 66 columns of averaged information (per subject and activity) corresponding to the Mean and std of different meassurements for a total of 180 observations (30 subjects x 6 activities). These observations include meassurements in Time and Frequency of magnitude (Mag) and components in X,Y and Z direction for the linear acceleration (Acc), angular acceleration (Gyro), linear jerk (AccJerk) and angular jerk (GyroJerk) for both Body and Gravity components. Columns 1 and 2 correspond to the Subject and Activity.

