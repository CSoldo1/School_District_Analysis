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

![Student Data](https://github.com/CSoldo1/Photos/blob/main/Deliverable_1.PNG)

## Deliverable 2: Prepare the Data
Once the data fram was properly created, I cleaned up the data by checking for and removing any null or duplicated values. 

student_df.isnull()
student_df.isnull().sum()
student_df.dropna()

![No Missing Values in the Data](https://github.com/CSoldo1/Photos/blob/main/no_null_values.PNG)

I continued to clean and organize the data:

![Cleaned Up and Ready to Analyze](https://github.com/CSoldo1/Photos/blob/main/clean_data.PNG)

![No Duplicated Values](https://github.com/CSoldo1/Photos/blob/main/duplicated_values.PNG)


And finally, I convered the "grade" column to a 'int' type by using the following code:

student_df['grade'] = student_df['grade'].astype('int64')

## Deliverable 3: Summarize the Data
I used the 'describe' function to generate a list of summary statistics for each column.

![Summary Statistics](https://github.com/CSoldo1/Photos/blob/main/summary_statistics.PNG)

The mean math_score for all grades is 64.72 and the min_reading_score was 10.5. The min_reading_score was stored using:

min_reading_score = student_df['reading_score'].min()

## Deliverable 4: Drill Down into the Data
The "loc" and "iloc" functions can be used to display multiple rows and columns. They can also be used to aggregate the data based on certain characteristics. 

![Loc and iLoc Functions](https://github.com/CSoldo1/Photos/blob/main/Deliverable_4_1.PNG)

![Summary Statistics for 9th Graders](https://github.com/CSoldo1/Photos/blob/main/Deliverable_4_2.PNG)

![Minimum Reading Score](https://github.com/CSoldo1/Photos/blob/main/Deliverable_4_3.PNG)

![Reading Scores for Different Grades](https://github.com/CSoldo1/Photos/blob/main/Deliverable_4_4.PNG)








## Deliverable 5: Compare the Data







