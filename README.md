## Overview of the school district analysis

Our group is fortunate to have been selected by the local school board to perform an audit of the district and the schools within it. The board provided us with two CSV files, the first containing data on every district school, the second containing data on every student in the district. Our primary analysis tool was Jupyter Notebook, initialized in an Acaconda PythonData developer environment. We used this tool to process, clean and analyze the data in the CSV files. 

After completing the first iteration of our analysis, the school board alerted us to some academic dishonesty at one of the local high schools. This prompted us to alter our findings by removing the 9th Grade reading and math test results from Thomas High School. Below you will see an in depth report of our new findings and how they differ from our initial analysis.

## Results

- Outlined in the charts below, we can see that removing Thomas High School's 9th grade test scores reduced the overall passing percentage of in the district, but the effect was minimal. Surprisingly, there wasn't a difference in Average Reading Score, and a slight reduction in Average Math Score.
  - Below is the new District Summary
![new_district_summary](https://github.com/rivas-j/School_District_Analysis/blob/d5c769384fe0f5a82a989f4624969d2dc8d54e9d/Resources/new_district_summary.png)  
  - Below is the previous District Summary
![old_district_summary](https://github.com/rivas-j/School_District_Analysis/blob/d5c769384fe0f5a82a989f4624969d2dc8d54e9d/Resources/old_district_summary.png)


- Comparing the two School Summaries below, we can see reduction across the board for Thomas High School after eliminating the erroneous grades. The only exception we see is a slight increase in the overall Reading Score, however this did not prevent the passing percentage of reading test takers from decreasing.
  - Below is the new School Sumary
![new_school_summary](https://github.com/rivas-j/School_District_Analysis/blob/d5c769384fe0f5a82a989f4624969d2dc8d54e9d/Resources/new_school_summary.png)
  - Below is the previous School Summary
![old_school_summary](https://github.com/rivas-j/School_District_Analysis/blob/d5c769384fe0f5a82a989f4624969d2dc8d54e9d/Resources/old_school_summary.png)
- The good news for Thomas High School is that, while their passing percentages were down slightly, it maintained it's spot as the second best performing school in the district.
  - Below is the new Ranking of Top Performing Schools
![new_top_performing](https://github.com/rivas-j/School_District_Analysis/blob/d5c769384fe0f5a82a989f4624969d2dc8d54e9d/Resources/new_top_performing.png)
  - Below is the previous Ranking of Top Performing Schools
![old_top_performing](https://github.com/rivas-j/School_District_Analysis/blob/d5c769384fe0f5a82a989f4624969d2dc8d54e9d/Resources/old_top_performing.png)
- How does replacing the ninth-grade scores affect the following:

  - Math and reading scores by grade
    - Below are the new Math scores by grade
    
    ![new_math_scores_by_grade](https://github.com/rivas-j/School_District_Analysis/blob/d5c769384fe0f5a82a989f4624969d2dc8d54e9d/Resources/new_math_scores_by_grade.png)
    - Below are the new Reading scores by grade

    ![new_reading_scores_by_grade](https://github.com/rivas-j/School_District_Analysis/blob/d5c769384fe0f5a82a989f4624969d2dc8d54e9d/Resources/new_reading_scores_by_grade.png)
  - Scores by school spending
    - Below are the new Scores by School Spending
    
    ![new_scores_by_school_spending](https://github.com/rivas-j/School_District_Analysis/blob/d5c769384fe0f5a82a989f4624969d2dc8d54e9d/Resources/new_scores_by_school_spending.png)
    - Below are the previous Scores by School Spending
    
    ![old_scores_by_school_spending](https://github.com/rivas-j/School_District_Analysis/blob/d5c769384fe0f5a82a989f4624969d2dc8d54e9d/Resources/old_scores_by_school_spending.png)
  - Scores by school size
    - Below are the new Scores by School Size  
    
    ![new_scores_by_school_size](https://github.com/rivas-j/School_District_Analysis/blob/d5c769384fe0f5a82a989f4624969d2dc8d54e9d/Resources/new_scores_by_school_size.png)
    - Below are the previous Scores by School Size
    
    ![old_scores_by_school_size](https://github.com/rivas-j/School_District_Analysis/blob/d5c769384fe0f5a82a989f4624969d2dc8d54e9d/Resources/old_scores_by_school_size.png)
  - Scores by school type
    - Below are the new Scores by School Type
    
    ![new_scores_by_school_type](https://github.com/rivas-j/School_District_Analysis/blob/d5c769384fe0f5a82a989f4624969d2dc8d54e9d/Resources/new_scores_by_school_type.png)
    - Below are the previous Scores by School Type
    
    ![old_scores_by_school_type](https://github.com/rivas-j/School_District_Analysis/blob/d5c769384fe0f5a82a989f4624969d2dc8d54e9d/Resources/old_scores_by_school_type.png)
    
## Summary: Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.
