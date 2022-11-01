# School_District_Analysis

## Overview
For this challenge, I was tasked with helping the chief data scientist of a city school district with preparing standardized test data for analysis, reporting, and presenting. Our analysis focuses primarily on student funding and overall standardized test scores. 

## Resources
 * Data Source: new_full_student_data.csv
 * Software: Python 3.7.1, Jupyter Notebook 

## Deliverable 1: Collect the Data
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



## Deliverable 2: Prepare the Data
Once the data fram was properly created, I cleaned up the data by checking for and removing any null or duplicated values. 

student_df.isnull()
student_df.isnull().sum()
student_df.dropna()

I continued to clean and organize the data:


And finally, I convered the "grade" column to a 'int' type by using the following code:
student_df['grade'] = student_df['grade'].astype('int64')

## Deliverable 3: Summarize the Data
I used the 'describe' function to generate a list of summary statistics for each column.

The mean math_score for all grades is 64.72 and the min_reading_score was 10.5. The min_reading_score was stored using:

min_reading_score = student_df['reading_score'].min()

## Deliverable 4: Drill Down into the Data
The "loc" and "iloc" functions can be used to display multiple rows and columns. They can also be used to aggregate the data based on certain characteristics. 

## Deliverable 5: Compare the Data







