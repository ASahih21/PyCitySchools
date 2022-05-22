# PycitySchools
## Purpose:

The PyCity School Board wants to analyze the reading and math testing results for the district. During the module I created an analysis, however they believe that there may have been scholastic dishonesty in the ninth grade class of Thomas High School. The purpose of this project is to remove those results from the data and preserve the rest of the data to repeat the analysis as well as provide an explanation of how these changes effect the data.

## Deliverable 1: Replacing the 9th grade reading and math scores at Thomas High School with NaN:

Just dropping the ninth grade THS students would make the total students incorrect. I don’t want to replace the data with a different value, because it will throw off my averages. Instead I converted all the test results for THS 9th graders to NaNs so that they would be ignored in my .mean functions.


#### District Summary: Results

There is not a significant difference in the percent of students who passed math and reading or who passed over all when we drop the THS 9th graders from the student count. This makes sense they make up about 1% of the overall population of students. 

|	| % Passing Math | % Passing Reading |% Overall Passing|
| --- | --- | --- | ---- |
| w/THS 9th | 75.0 | 85.8 | 65.2 |
| w/o THS 9th | 74.8 |	85.7 | 64.9 |
|Difference|0.18  | 0.11 | 0.27 |


### School Summary:

Even though removing the ninth graders from our count didn’t have a large effect on the overall data for the district, once we look deeper into the data it may have a larger effect. For example, although the THS freshmen only made up 1% of the district they make up 28% of THS students, so we can assume it influence the conclusions we can make from the data in our school summary. To combat this I removed the THS 9th graders from the THS total students and then calculated new percentages to make the per_school_summary_df which will be used to analyze the per capita spending, size and type.

            
The reading_scores_by_grade and math_scores_by_grade use the school_data_complete_df. They are not affected by replacing the ninth grader scores for THS, because they are grouped by both the ninth graders and the schools. There is little difference between grades from the same school. This means any outliers might indicate a problem with the data. 

If you wanted to look at the average grades for all the students in the district by grade, the code would have to be modified, because it may be somewhat affected by the missing values. This also probably wouldn’t be very useful as all the values would probably be very close to the averages from the district summary.

### Scores by School Spending:

To create a dataframe of school data based on spending I created bins  that would have a relatively equal number of schools in each bin and named them. Then I used the .cut method to divide the per capita spending by my bins. I used the group by method to get the averages for each variable. Then I created and formatted the spending ranges per student dataframe.
```

#### Scores by School Spending: Results

THS is in the middle of per capita spending so the scores very greatly. If they make up a significant portion of the total count the THS ninth graders would lower the percentage results.

### Scores by School Size

To create a dataframe of school data based on size I created bins  that would have a relatively equal number of schools in each bin and named them. Then I used the .cut method to divide total students for my bins. I used the group by method to get the averages for each variable. Then I created and formatted the dataframe.

#### Scores by School Type: Results


If they make up a significant portion of the total count the THS ninth graders in the data have lowered the passing percentage for charter schools.

## Results Summary:
- For the district summary the THS ninth graders do not make up a significant portion of the total student count so removing them does not have a statistically significant change in the % Passing Math, % Passing Reading, and % Overall Passing results.
- Removing THS ninth graders from the school summary changes the data significantly, because they make up a significant portion of the THS students.
- Removing the NaNs for the by grades summaries is unnecessary because there is little difference between grades from the same school. This report should be used to detect outliers.
- For the school by type, per capita spending and size dataframes if the THS ninth graders make up a significant portion of the total count of the students the % Passing Math, % Passing Reading, and % Overall Passing results will be lower than if they are removed.

## Conclusions:
- Students preform slightly worse in math than reading.
- Students from the same school’s performance is not significantly different from grade to grade.
- Charter schools outperformed the traditional schools. 
- Large schools tend to preform significantly worse than small or medium schools which preform about the same.
- Per capita spending is inversely related to performance.

Charter schools do not typically perform better or worse than traditional public school, but research does seem to suggest that in disadvantaged populations there is performance improvement in charter schools. The PyCity results seem to support this. Charter schools are probably performing better than public schools because of the following:

- Even though traditional schools have a higher per capita budget, the % of the budget they are spending on teachers and educational materials is probably lower than that of charter schools.
    - *Charter school performance had an inverse correlation with per capita spending.* Compared to charter schools, traditional public schools may have higher budgets because they are required to provide students with additional service such as transportation, food, and support services (National Conference of State Legislatures). It would be great to see a breakdown of the budgets to confirm this.
- The traditional public schools are over crowded.
    -  *Medium and small school preform about the same, but large schools tend to preform significantly* (Condition of America's Public School Facilities: 1999). Large schools tend to be in urban areas with higher percentages of minorities and higher cost of living. They are more likely to be overcrowded which is correlated with poorer facilities and poor performance. *Only one Charter school is a large school.* This is probably the, because charter school are not forced to take students once they are at capacity; enrollment is either first come first serve or by lottery. So their infrastructure is built to handle the large number of students. Public schools, however, must take students even if they are over crowded.
