# PycitySchools
## Purpose:

The PyCity School Board wants to analyze the reading and math testing results for the district. During the module I created an analysis, however they believe that there may have been scholastic dishonesty in the ninth grade class of Thomas High School. The purpose of this project is to remove those results from the data and preserve the rest of the data to repeat the analysis as well as provide an explanation of how these changes effect the data.


### School Summary:

As a whole, schools with higher budgets, did not yield better test results. By contrast, schools with higher spending per student actually ($645-675) underperformed compared to schools with smaller budgets (<$585 per student).

As a whole, smaller and medium sized schools dramatically out-performed large sized schools on passing math performances (89-91% passing vs 67%).

As a whole, charter schools out-performed the public district schools across all metrics. However, more analysis will be required to glean if the effect is due to school practices or the fact that charter schools tend to serve smaller student populations per school.


## Results Summary:

- For the district summary the THS ninth graders do not make up a significant portion of the total student count so removing them does not have a statistically significant change in the % Passing Math, % Passing Reading, and % Overall Passing results.
- Removing THS ninth graders from the school summary changes the data significantly, because they make up a significant portion of the THS students.
- Removing the NaNs for the by grades summaries is unnecessary because there is little difference between grades from the same school. This report should be used to detect outliers.
- 
- For the school by type, per capita spending and size dataframes if the THS ninth graders make up a significant portion of the total count of the students the % Passing Math, % Passing Reading, and % Overall Passing results will be lower than if they are removed.

## Conclusions:
- Students preform slightly worse in math than reading.
- Students from the same school’s performance is not significantly different from grade to grade.
- Charter schools outperformed the traditional schools. 
- Large schools tend to preform significantly worse than small or medium schools which preform about the same.
- Per capita spending is inversely related to performance.

Charter schools do not typically perform better or worse than traditional public school, but research does seem to suggest that in disadvantaged populations there is performance improvement in charter schools. The PyCity results seem to support this. Charter schools are probably performing better than public schools because of the following:

- Even though traditional schools have a higher per capita budget, the % of the budget they are spending on teachers and educational materials is probably lower than that of charter schools.
- 
    - *Charter school performance had an inverse correlation with per capita spending.* Compared to charter schools, traditional public schools may have higher budgets because they are required to provide students with additional service such as transportation, food, and support services (National Conference of State Legislatures). It would be great to see a breakdown of the budgets to confirm this.
- The traditional public schools are over crowded.
- 
    -  *Medium and small school preform about the same, but large schools tend to preform significantly* 
    -   Large schools tend to be in urban areas with higher percentages of minorities and higher cost of living. They are more likely to be overcrowded which is correlated with poorer facilities and poor performance. 
