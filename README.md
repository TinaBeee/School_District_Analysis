## School District Analysis
Cleaned and analyzed students' performance in math and reading for a school district to determine impact of school funding on grades 

### Overview of Project
The analysis consisted of two separate CSV files - one containing information about the schools' financials and style of operation; the other detailed information on nearly 40,000 individual students, their grades, their schools and their scores in reading and math. Initially had to clean the student data and then analyze it to determine the performance of individual schools and quantify performance according to school funding levels, school type and by grade.
After the initial analysis, it turned out that some of the scores at one school were invalid, requiring a repeat of the analysis. The following discusses how removing those scores has impacted the overall analysis.

## Resources 
- Data source: students_complete.csv, schools_complete.csv
- Software: Jupyter Notebook 6.3.0, Pandas library

## Results
- How is the district summary affected after some scores have been removed?
   - In the original summary our results for the entire school district look as follows:
    
     <img src = "https://user-images.githubusercontent.com/90064437/141661420-6b1aab51-d387-42b9-8581-c6e0f2fa4d78.png">
        
   - Once we remove the 9th graders from one of the high schools, we can see that the overall results are slightly repressed.

       <img src="https://user-images.githubusercontent.com/90064437/141661398-260c6ae1-1b46-4137-8dfc-2ca69acc696c.png">

- How is the school summary affected?
   - The school summary, which lists the results of each school individually, is only affected in the line that describes the results of Thomas High School, the 
      school whose results have been altered. In the original analysis, the results for Thomas High School looked as follows:
      
     <img src="https://user-images.githubusercontent.com/90064437/141661621-5b194085-3459-46cf-8058-a47f70b6d957.png">
      
   - After removing the 9th graders' scores, the results looked as seen below, with the only impact a slight change in the average reading score.
      Due to the rounding of the data, the impact is less discernible in the summary table. Without rounding, the impact can be grasped more clearly (included in
      the next bullet point is some not rounded data for comparison)

     <img src="https://user-images.githubusercontent.com/90064437/141661643-fa40671f-a277-49fe-aa24-d9da6295f962.png">
 
 - How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
   - Thomas High School remains the second-best performing school in the district, even after removing ninth graders' scores. But a look at the unrounded data
      shows the difference in scores more clearly. Below, a snap shot of the top-three performing schools in the original analysis:
      
     <img src="https://user-images.githubusercontent.com/90064437/141661775-efc7f4b0-4116-4194-ab14-44e0686dc0d5.png">
      
   - Here the same data after removal of the 9th graders' scores at Thomas High School:
    
     <img src="https://user-images.githubusercontent.com/90064437/141661789-6da83431-249d-401e-aeb4-9e26541321a3.png">
      
 - How does replacing the ninth-grade scores affect the following:
   - Math and reading scores by grade:
    - Grade-level math and reading scores are not impacted at any school other than Thomas High School for the 9th grade. Since we replaced all 9th grade values at
      that particular high school with "null" values, 9th grade scores at Thomas High School are listed as "NaN".
   - Scores by school spending:
    - Results based on schools' per capita spending ranges looked as follows in the original analysis:
      
      <img src="https://user-images.githubusercontent.com/90064437/141662102-91231758-094f-403b-95ab-fdf2ffc84e6f.png">
      
    - After removing 9th grade scores at Thomas High School, the spending range results still look the same as the differences were too small to impact the overall
      result when filtering for schools' per capita spending buckets:
    
      <img src="https://user-images.githubusercontent.com/90064437/141662116-d2b2b8b4-7179-455f-8e6f-cad073e2d2b0.png">
      
  - Scores by school size and school type:
    - Similarly, removing the 9th graders had no impact when filtering the data to display summary results based on the schools' student sizes and the type of 
      school (charter or public)
      
 ## Summary
After removing the scores of 9th graders from Thomas High School, the largest impact is visible on the overall district summary (as detailed above). Specifically, the average score for math dropped by 0.1 points, the percentage of students passing math and reading by 0.2 and 0.3 percentage points, respectively, and the percentage of students passing both subjects dropped by 0.1 percentage point.
 
However, some of the changes on the results with more granular filters exist, but are simply not visible once the numbers have been rounded.







