# School_District_Analysis
Module 4 Work

## Project Overview
A school district has asked for a comprehensive analysis of the schools in their district. The deliverables should include a high-level snapshot of the district's key metrics and an overview of the key metrics for each school, all presented in a table format. It was also discovered during the analysis that the grades for the 9th graders at Thomas High School were suspect, and were therefore eliminated from the analysis

The School Board asked for the following key metrics:
1. Top 5 and bottom 5 performing schools, based on the overall passing rate
2. The average math score received by students in each grade level at each school
3.  The average reading score received by students in each grade level at each school
4.  School performance based on the budget per student
5.  School performance based on the school size 
6.  School performance based on the type of school

## Results
### District Summary
<img width="506" alt="District_Analysis_Updated" src="https://user-images.githubusercontent.com/104801614/173038023-4f7b55b6-b5f0-4923-a5eb-162e49d6d0d3.png">

The high-level, district summary shows that there are a total of 15 schools with a combined 39,170 students.  Across those schools, ~75% of students are passing their Reading courses, and ~86% are passing their Math courses.  Only about 65% of all students are passing both.  Data analysis identified that of the 39,170 students in the district, 461 were 9th graders from Thomas High School that needed to be eliminated from the statistics until their grades can be reviewed.

### Key Metrics for Each School
#### Original Dataset
<img width="530" alt="per_school_summary_df_PreUpdate" src="https://user-images.githubusercontent.com/104801614/173038240-93809e47-5bd8-4f7d-bcb9-3d40be3f21b5.png">
#### Update Thomas High Dataset
<img width="531" alt="School_Summary_ActuallyUpdated" src="https://user-images.githubusercontent.com/104801614/173047396-1c7698b5-4141-44b1-90e5-d45fcf6dee40.png">

This DataFrame classifies each of the 15 schools (charter or district), displays the total student body, the school's budget, the per student spend, and summary statistics of their test scores.  This summary still includes the 461 9th grade students from Thomas High.  When those students were eliminated from the count, the math and reading scores went up.  We can also see that the Reading and Math scores for Thomas High went up significantly, once the 9th grader scores were nulled out in the dataset.

### Key Metrics By School
#### 1. Top 5 and Bottom 5
<img width="531" alt="Top5SchoolsUpdated" src="https://user-images.githubusercontent.com/104801614/173038877-2200a63c-9e89-4769-9772-5d36908ed672.png">
<img width="530" alt="Bottom5SchoolsUpdated" src="https://user-images.githubusercontent.com/104801614/173038894-4f9b19ca-33e7-4904-91bd-ec24f24ae6b4.png">
These two images show the top 5 performing schools and bottom 5 performing schools.  At first glance, it seems that the Top 5 Schools are generally smaller, charter schools, whereas the Bottom 5 Schools are all district schools with bigger student bodies.  Somewhat counterintuitively, the Bottom 5 Schools also all had higher budget spend per student, which seems to say that the money by itself is not a key determiner of student performance.

#### Average Math Scores by Grade Level
<img width="171" alt="Math_scores_by_grade_Updated" src="https://user-images.githubusercontent.com/104801614/173039752-b71fd6c6-0e06-4e2d-aec5-8703235737bc.png">
This table shows the breakdown of average math scores by grade in each of the 15 schools in the district.  A trend is observable in each school in that scoring averages are roughly similar across all grade levels.  This seems to indicate that schools perform consistently at all grade levels.  You can also see in this chart that the 9th grade scores from Thomas High have been eliminated.  In the image below, where the 9th graders were included in the analysis, we can see that the Math scores are still roughly in line with the performance across the other grade levels at Thomas High.
<img width="235" alt="Math_scores_by_grade_PreUpdated" src="https://user-images.githubusercontent.com/104801614/173040946-508a81b2-b650-4850-935b-d38b39c19cd6.png">

#### Average Reading Score by Grade Level
<img width="172" alt="Reading_scores_by_grade_Updated" src="https://user-images.githubusercontent.com/104801614/173041370-648ab2a6-fe19-4f01-806f-5e9ef161fb1a.png">
Similar to the Math scores above, this table shows the breakdown of Reading scores across the different grade levels at the 15 schools. Again, we see a similar performance across all grade levels at each school, but unlike with the Math scores, we also see that all the schools have very similar Reading scores.  This would indicate that Math might deserve more attention at the underperforming schools in the district, in order to raise student scores.  You can alos see in this table that the 9th graders from Thomas High have been excluded from the analysis.  By comparing to the table below, however, we can see that the Thomas High 9th-grade Reading scores were in the same range as the other grades at Thomas High.
<img width="170" alt="Reading_scores_by_grade_PreUpdated" src="https://user-images.githubusercontent.com/104801614/173042690-c3f2eb01-639f-4c8a-8df1-69ed89941fdd.png">


#### School Performance Based on Budget
<img width="453" alt="School_Spending_df_Updated" src="https://user-images.githubusercontent.com/104801614/173043266-57b7623c-b423-44d6-97a7-655e97ffcaf7.png">
Binning our data to classify schools on their average dollar spent per student shows that, in this school district, the higher spending schools show diminishing returns.  Scores show an inverse relationship with average spend, which requires further analysis to determine why that is the case.

#### Performance Based on School Size
<img width="413" alt="School_Size_df_Updated" src="https://user-images.githubusercontent.com/104801614/173043225-e08c5fef-7cff-4968-b189-957086bbc320.png">
Similarly to our comparison of student scores to average spend, scores also have an inverse relationship with the size of the school.

#### Performance Based on School Type
<img width="389" alt="School_Type_df_Updated" src="https://user-images.githubusercontent.com/104801614/173043312-63926dba-f6d5-4bda-9d84-065b17cbfea1.png">
The final division we used to compare schools was to look at performance between Charter and District schools.  Whereas all schools had similar average scores, the percentages of students passing their courses were significantly higher at charter schools, with ~36% difference in the percentage of students passing all threir courses at a Charter school rather than a district school.

### Summary
After nulling out the grades in question for 9th graders at Thomas High, several things changed.  First, the entire population that we were using to calculate statistics for the district because we eliminated 461 students and their grades from the means and averages.  Secondly, the percentage of student passing Math went up for Thomas High (by nearly 30 percentage points!).  Thirdly, the percentage of students passing Reading went up for Thomas High (again, by nearly 30 percentage points). Fourthly, the percentage of students passing both Math and Reading went up.  Finally, percentages for the district were changed by the elimination of the 9th graders from Thomas High (just not as noticeably because of the larger population).
