# An Analysis of School District Scores and Spending
Performing anaylsis on school funding and standardized test scores to help Maria advise the school district in its discussions and decision making process.

## Overview of the Project
In this analysis, we helped Maria find the following:
1. A high-level snapshot of the district's key metrics, presented in a table format
2. An overview of the key metrics for each school, presented in a table format
3. Tables presenting each of the following metrics:
    - Top 5 and bottom 5 performing schools, based on the overall passing rate
    - The average math score received by students in each grade level at each school
    - The average reading score received by students in each grade level at each school
    - School performance based on the budget per student
    - School performance based on the school size 
    - School performance based on the type of school

## Results
1. The district summary (below) shows an aggregate view of the district's performance. This data table is largely unchanged from the results we saw in the module. The main difference is added granularity as this dataframe shows data to the tenth of a percent. 

![image](https://user-images.githubusercontent.com/92613639/142089386-c04256a9-be52-4e56-8942-ba02b9a5910e.png)

2. The school summary (below) is also similar to that in the module. It is slightly varied from the earlier dataframe, specifically due to the changes we made to the data relating to Thomas High School (THS). We were alerted of potential academic dishonesty and that THS' ninth grade scores had been altered. Due to this, we helped Maria remove all of these scores from our analysis. This appears to have dropped the average scores at THS by >0.5%.

Data prior to alteration:

![image](https://user-images.githubusercontent.com/92613639/142090475-4ab3076e-b199-437e-8351-50e95590617c.png)

Data post alteration:

![image](https://user-images.githubusercontent.com/92613639/142089726-413377b9-98af-4eb7-a104-a3239b4302dc.png)

3. Replacing the ninth graders' math and reading scores does not have much impact on THS' performance relative to the other schools. As we are looking at averages, the inflated scores did not bring up the overall school's scores by much (adding 100 to a score of 93 doesn't change the average quite as dramatically as say adding 0 to a score of 93). This said, THS remains in the top 5 schools both before and after removing the faulty scores, ranking second overall.

![image](https://user-images.githubusercontent.com/92613639/142091178-a5bc3632-c3f4-4eb6-ae4d-4ba20146b0c8.png)

4. Replacing the ninth-grade scores impacts the following minimally:
    - Math and reading scores by grade were largely unimpacted other than THS having no score showing for ninth graders in either data frame. The new dataframes are formated to a single decimal point, making them cleaner and easier to read.
    
    Math Scores by Grade:
    
    ![image](https://user-images.githubusercontent.com/92613639/142091560-9f55af6b-1700-4a72-8032-7f782663bc44.png)
    
    Reading Scores by Grade:
    
    ![image](https://user-images.githubusercontent.com/92613639/142091648-797f38d1-02e8-4b53-b267-b5b643362a8e.png)

    - THS spends $638/student. By dropping the ninth grade scores, their bin ($630-644) had no detectable change - the missing scores may have been nothing more than a rounding error.
    
    ![image](https://user-images.githubusercontent.com/92613639/142091906-dec43415-0da6-4e36-8c3d-6299356d9173.png)

    - THS has 1635 students and is therefore characterized as a Medium sized school. By dropping the ninth grade scores, their bin (1000-2000 students) again had no detectable change.
    
    ![image](https://user-images.githubusercontent.com/92613639/142092145-50e9f931-56b2-418b-9616-aa26e77a0c7e.png)

    - THS is a charter school. By dropping the ninth grade scores, their grouping (Charter Schools) again had no detectable change.
    
    ![image](https://user-images.githubusercontent.com/92613639/142092279-7015d68e-865e-4ad4-aa27-471890d7a010.png)

## Summary
- When we simply removed the ninth grade scores from THS, the scores dropped dramatically (see below). This is because we were now averaging 3 years of scores over 4 years of students, essentially giving all ninth graders zeroes for their scores. When we rectified that by omitting ninth graders from both the numerator and denomenator, we realized the scores went back up to essentially where they were prior to removing the ninth graders at all.

![image](https://user-images.githubusercontent.com/92613639/142093555-eeecf8f5-d3f7-45fa-bad7-c31877b838bf.png)

- 
