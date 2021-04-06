# School District Analysis
Module 4 Project

## Overview

This project is to satisfy the requirements for the fourth module challenge in the Data Analysis Bootcamp. 
In this project we are asked to help Maria, a Data Scientist, analyze and review the data from a school district.
The analysis includes results showing performance trends, spending per student, average and overall grades per school, and a comparison of the size school.
During this analysis, Maria was notified of potential grade tampering with Thomas High School's (THS) 9th grader's scores. 
Those math and reading scores will be changed to NaN (not a number); with all other data maintained until further investigation of the tampering can be completed.
The difference between before and after of the removal of the suspect grades will be reviewed.
* Note:  To maintain the Family Educational Rights and Privacy Act (FERPA) rules, results will not show the student's name with their individual grades. 


## Results
The results for the district show the following:

 * How is the district summary affected by the Thomas High School adjustment? 
In the original analysis of the district, which kept the grades intact for the 9th graders at THS, the average scores and overall passing percentages were slightly higher. 
The largest change being the Percentage Overall Passing, which changed from 65.2% to 64.9%. The calculation included the change of total student count, which reduced approximately by 460.
#### District Original Summary
![District Original Summary](https://github.com/summerstime/School_District_Analysis/blob/main/Resources/District_Summary_1st.png) 
#### District Summary
![District Summary](https://github.com/summerstime/School_District_Analysis/blob/main/Resources/District_Summary_Challenge.png)

 * How is the school summary affected?
The Thomas High School percentage summary changed dramatically when the suspect values were removed and the students who had those values were also removed from the calculations.
To include them in the overall count would shift the percentages to a much lower number.
The original totals for THS were 66.9%, 69.7%, and 65.1% for math, reading and overall, respectively.
After the suspect grades were removed the percentages changed to 93.1%, 97.0%, and 90.6%, respectively. 
#### Thomas School Original Data Summary
![Thomas School Original Summary](https://github.com/summerstime/School_District_Analysis/blob/main/Resources/THS_B4_NaN_School_Summary.png) 
#### Thomas School Summary
![Thomas School Summary](https://github.com/summerstime/School_District_Analysis/blob/main/Resources/THS_School_Summary.png) 

 * How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
Originally, THS was 8th out of 15 schools with an overall percentage of 65.1%. After the adjustment, THS moved to the top 5.
#### Top 5 Schools
![Top 5 Schools](https://github.com/summerstime/School_District_Analysis/blob/main/Resources/Top_5_Schools.png) 

 * How does replacing the ninth-grade scores affect the following:
   - Math and reading scores by grade
     - THS's average scores appear to be consistent before and after the removal of the 9th grader's scores.
     - These screenshots show how THS compares to other shools across each grade level. Comparing THS's grade levels, they appear to also be consistent to each other.
#### Average Math Scores for All Schools
![Average Math](https://github.com/summerstime/School_District_Analysis/blob/main/Resources/Average_Math.png)
#### Average Reading Scores for All Schools
![Average Reading](https://github.com/summerstime/School_District_Analysis/blob/main/Resources/Average_Reading.png)

   - Scores by school spending
     - The overall school scores would be a little lower, if the adjustment to THS was not made. THS's spending group is approximately $638 per student. That spending group would be affected.
#### Scores by School Spending
![Scores by School Spending](https://github.com/summerstime/School_District_Analysis/blob/main/Resources/Scores_Spending.png)

   - Scores by school size
     - The total number of THS 9th graders taken out of the totals would affect their overall student total by 461 students. (38709 total students after removal)
#### School Size Scores
![Scores by School Size](https://github.com/summerstime/School_District_Analysis/blob/main/Resources/School_size.png)
    
   - Scores by school type
     - The adjusted scores helped bring the Charter schools up in overall percentages. The average scores were very similar.
#### School Type Scores
![Scores by School Type](https://github.com/summerstime/School_District_Analysis/blob/main/Resources/School_type.png)

 

## Summary
In summary, the most dramatic change to the results was found in the three percentages for Thomas High School, Passing Math Scores, Passing Reading Scores, and Overall Passing. 
Once the 9th graders were removed from the total student count, the percentages reflected a great improvement, from 65% to 90% overall. This moved them to the top 5 of schools.
Another evaluation is the spending per student. The overall district would be affected by the reduction of 461 students; but the total number of students for the district is sufficient enough that the change would be minor; but the change for THS would be much more noticable. 

## Analysis Details
The data was delivered in two separate files, schools_complete.csv and students_complete.csv. The two files were merged by a join function that matched up the school name in both files. 
Since the student file has more data, it was used as the left side of the join. The school file joined only that information that matched the student file.
To maintain the rules for the Family Educational Rights and Privacy Act (FERPA), the dataframes/displays of data does not show the individual student names with their grades.
This would be sharing the student's educational record and would violate FERPA. 
Python, Numpy, Pandas, and Jupyter Notebook were utilized to analysis the merged data to deliever the above results.
Example of the data showing how NaN is listed in the data.
#### THS NaN Example
![THS NaN Examplee](https://github.com/summerstime/School_District_Analysis/blob/main/Resources/Thomas_NaN_Example.png)
