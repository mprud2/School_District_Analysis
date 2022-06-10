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
<img width="530" alt="per_school_summary_df_PreUpdate" src="https://user-images.githubusercontent.com/104801614/173038240-93809e47-5bd8-4f7d-bcb9-3d40be3f21b5.png">
This DataFrame classifies each of the 15 schools (charter or district), displays the total student body, the school's budget, the per student spend, and summary statistics of their test scores.  This summary still includes the 461 9th grade students from Thomas High.  When those students were eliminated from the count, the math and reading scores went up.

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
