# School District Analysis with Python

![School](images/school.jpg)

## <div align="center">Perform school district audit by building a python solution in jupyter notebook</div>

<p align="center">
<a href="#goals">Goals</a> &nbsp;&bull;&nbsp;
<a href="#dataset">Dataset</a> &nbsp;&bull;&nbsp;
<a href="#tools-used">Tools Used</a> &nbsp;&bull;&nbsp;
<a href="#analysis-and-challenges">Analysis and Challenges</a> &nbsp;&bull;&nbsp;
<a href="#results">Results</a> &nbsp;&bull;&nbsp;
<a href="#summary">Summary</a>
</p>

# <div align="center">Goals</div>
Analyze student data across a local school district to confirm evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. This analysis will allow the school district to uphold state-testing standards.

# <div align="center">Dataset</div>
This analysis will utilize two CSV files, retrieved from an Amazon S3 host, to conduct the district level audit.

- [Students_Complete:](data/students_complete.csv) 39,170 rows of student data used for our analysis, in CSV format
- [Schools_Complete:](data/schools_complete.csv) 14 rows of data, containing data for all schools in the district in CSV format

# <div align="center">Tools Used</div>
- **Python:** Programming language used to build automated auditing solution
  - **Pandas:** Open source Python library providing high performance analysis tools
- **Jupyter Notebook:** Open source web based application used to run our python code


# <div align="center">Analysis and Challenges</div>
We performed an audit of the local district and the schools within it. The board provided two CSV files: the first containing data on every district school, the second containing data on every student in the district. The primary analysis tool was Jupyter Notebook, initialized in an Anaconda PythonData developer environment. We used this tool to process, clean and analyze the data in the CSV files. 

After completing the first iteration of our analysis, the school board alerted us to some academic dishonesty at one of the local high schools. This prompted us to alter our findings by removing the 9th Grade reading and math test results from Thomas High School. 

We accommplished this by using the Pandas loc method with conditional statements and comparison and logical operators, selecting the ninth-grade reading and math scores for Thomas High School. Then, using the Pandas NumPy module to change the reading and math scores to NaN. You'll see how we executed this in the code snippets below:

```python
# Use the loc method on the student_data_df to select all the reading scores from the 9th grade at Thomas High School and replace them with NaN.
student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"),["reading_score"]] = np.nan
```
```python
#  Refactor the code for the reading scores to replace the math scores with NaN.
student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"),["math_score"]] = np.nan
```
Below is an in-depth report of our new findings and how they differ from our initial analysis.

# <div align="center">Results</div>
- Outlined in the charts below, we can see that removing Thomas High School's 9th grade test scores reduced the overall passing percentage of school in the district, but the effect was minimal. Surprisingly, there wasn't a difference in Average Reading Score, and a slight reduction in Average Math Score.
 
  ### New District Summary
    ![new_district_summary](images/new_district_summary.png)  
  ### Previous District Summary
    ![old_district_summary](images/old_district_summary.png)


- Comparing the two School Summaries below, we can see reduction across the board for Thomas High School after eliminating the erroneous grades. The only exception we see is a slight increase in the overall Reading Score, however this did not prevent the passing percentage of reading test takers from decreasing.

### New School Summary
![new_school_summary](images/new_school_summary.png)
  
### Previous School Summary
![old_school_summary](images/old_school_summary.png)
- The good news for Thomas High School is that, while their passing percentages were down slightly, it maintained its spot as the second-best performing school in the district.

  ### New Ranking of Top Performing Schools
    ![new_top_performing](images/new_top_performing.png)

  ### Previous Ranking of Top Performing Schools
    ![old_top_performing](images/old_top_performing.png)

- These last few summaries depict the effect removing all 9th Grade test scores from Thomas High School had in our analysis.

  - Below you will see a comparison of all the test scores by school grade. Notice that we've nullified the 9th grade scores for Thomas High School. Eliminating these scores did not influence the other grade scores for Thomas High School.

    ### New Math Scores by Grade
    
    ![new_math_scores_by_grade](images/new_math_scores_by_grade.png)
    
    ### New Reading Scores by Grade
    ![new_reading_scores_by_grade](images/new_reading_scores_by_grade.png)
  
  - There was not a big change in test scores by school spending. We only saw a slight difference in the $631-645 tier, but not enough to shift the overall numbers. 
    
    ### New Scores by School Spending    
    ![new_scores_by_school_spending](images/new_scores_by_school_spending.png)

    ### Previous Scores by School Spending
    ![old_scores_by_school_spending](images/old_scores_by_school_spending.png)

- Removing Thomas High School 9th graders did not affect our school size summary. We saw some slight variations in the Medium (1000-1999) student tier, but not enough to shift the results.
    ### New Scores by School Size  
    ![new_scores_by_school_size](images/new_scores_by_school_size.png)
    
    ### Previous Scores by School Size
    ![old_scores_by_school_size](images/old_scores_by_school_size.png)

- For our school type breakdown, we saw slight variations within the Charter School test results. These changes did not cause a big enough shift in the overall numbers, as outlined in the charts below.
    
    ### New Scores by School Type
    ![new_scores_by_school_type](images/new_scores_by_school_type.png)
    
    ### Previous Scores by School Type
    ![old_scores_by_school_type](images/old_scores_by_school_type.png)

# <div align="center">Summary</div>
We'd like to share the good news that our results didn't change too drastically after removing the 9th grade scores for Thomas High School. Here are more of our findings from our analysis:

- Predictably, removing artificially inflated scores reduced the overall passing percentage in our school and district wide summaries.
- Surprisingly, there wasn't a big change in the overall reading scores, despite a reduction in passing percentage across the board.
- Based on our reading of the difference in scores, we conclude that eliminating the 9th Grade Thomas High School grades affected the average Math Scores the most.
- After reviewing our findings, it is safe to assume that the majority of the erroneous test scores in the district were the Math Scores for the 9th Graders in Thomas High School.

[Back to top](#school-district-analysis-with-python)






