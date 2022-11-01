# School_District_Analysis

## Overview


## Source
Data new_full_student_data.csv
Python




## Deliverable 1
I imported the data from the .csv file into a data frame using the following code:

import pandas as pd
import os

os.getcwd()
os.chdir(r"C:\Users\chris\Desktop\Data_Analytics_Class\Module 4\School_District_Analysis\Module 4 Challenge\Student_Data_Challenge_Starter_Code")
path = "/Student_Data_Challenge_Starter_Code"
full_student_data = os.path.join('Resources/new_full_student_data.csv')
student_df = pd.read_csv(full_student_data)

To confirm that Pandas imported the data correctly, I used the "head" function. 

student_df.head()



## Deliverable 2
Once the data fram was properly created, I cleaned up the data by checking for and removing any null or duplicated values. 

student_df.isnull()
student_df.isnull().sum()
student_df.dropna()

I continued to clean and organize the data:


And finally, I convered the "grade" column to a 'int' type by using the following code:
student_df['grade'] = student_df['grade'].astype('int64')





