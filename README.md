# School_District_Analysis


## Overview of Project

An analysis is carried out to find patterns in a database about the development of schools and their students in order to make the best decisions that improve their development.

But we have a problem, we are informed that we have a case of dishonesty in one of the schools. We have been told that the information for the ninth graders at "Thomas High School" was possibly tampered with. To avoid problems while this case is being solved, we are asked to override the information of the ninth grade students of this school when conducting the study.

Then we need to know how much impact is had by discarding this information from the ninth grade and how the databases are developed at the end, in order to be able to answer the questions that are asked to us, such as the following:

- How is the district summary affected?
- How is the school summary affected?
- How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
- How does replacing the ninth-grade scores affect the following:
  - Math and reading scores by grade
  - Scores by school spending
  - Scores by school size
  - Scores by school type




## Resources
- Data source: schools_complete.csv , students_complete.csv
- Software: Python 3.7.0 , Anaconda , Jupyter


## Results

### How is the district summary affected?
- As we can see, the effect of not having the information of the ninth graders of Thomas High School was that almost all the statistics were slightly reduced except for the "Average Reading Score", it was the only one that remained intact, all the others slightly decreased


Modified 
![image](https://user-images.githubusercontent.com/66183125/137639242-2feb1ee2-febc-414b-9f4b-4f5bdd4ec628.png)

Original 
![image](https://user-images.githubusercontent.com/66183125/137645131-ae0ac1e9-86c8-4ffb-82a5-ed0d47dd535f.png)

### How is the school summary affected?
- There is really no dataframe modification, only Thomas High School is affected.

Modified (It is the result of revoming the ninth graders of Thomas School and replacing the data with nan)
![image](https://user-images.githubusercontent.com/66183125/137642368-e143c796-cf31-461e-9eeb-4a499f5ddb00.png)


Original 

![image](https://user-images.githubusercontent.com/66183125/137642375-569c99ce-10b9-414b-93e4-0a3d61a06e46.png)

### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
- Thomas High School is significantly affected in all areas except the Average Reading Score, removing the 9th grade student's score from the overall percentage results in a reduction from 90.94 to 65.07. But if we work with the data of the 10th, 11th and 12th students, as if the information of the ninth grade students had never existed, we would see that they would still be affected, but not in the same proportion, as we can see in the general percentage, it just goes down from 90.94 to 90.63

Modified(It is the result of working with the data of 10th, 11th and 12th of thomas high school and averaging them without taking in terms of those of ninth)

![image](https://user-images.githubusercontent.com/66183125/137643223-cc2bdf01-2240-4b78-840b-1e6f046c90e0.png)


### Math and reading scores by grade
- The only difference that they have in these dataframes is that in the 9th column, Thomas High School, its value is represented as nan, everything else compared to the original analysis has not changed

![image](https://user-images.githubusercontent.com/66183125/137643494-72afeca2-f5ec-48a8-8107-929ccc21ead1.png) ![image](https://user-images.githubusercontent.com/66183125/137643502-54bfd8f0-d424-497d-aeab-f175b9015fbd.png)


### Scores by school spending
- The purpose of this dataframe is to know with how much money should be assigned to each student and therefore how much budget should be assigned to each school, surprisingly the students who were assigned a lower amount of budget performed better in the school . There was no difference with the original analysis
![image](https://user-images.githubusercontent.com/66183125/137643865-59d248c4-671b-49e9-9587-ff78ac54fe88.png)





### Scores by school size
- It was necessary to know the number of students in each school and for the same reason to know if this influenced the development of the students, this database shows us that at an average level of students between a range of 1000 to 2000 they perform better , so we can think that they are given greater attention as there are not so many, since in the range of 2000 to 5000, their performance is much worse. There were no differences with the original analysis
![image](https://user-images.githubusercontent.com/66183125/137644079-cee2a372-229d-4420-aa9c-b7c993e928ab.png)




### Scores by school type
- It was also necessary to know what type of school could make its students perform better, in this case without a doubt the Charter schools have a higher score, so more attention should be paid to the district schools, there were no changes with the original analysis
![image](https://user-images.githubusercontent.com/66183125/137644108-b92b24a1-df7b-4ac1-a2ff-b1dbc5dc6343.png)


## Summary

- Basically the main effects after modifying the databases by removing the ninth grade results from Thomas High School, were in the district summary dataframe , where they decreased a few tenths in general. Changes were also seen in the Dataframe of "school summary" since by only removing the results of ninth grade , the result that they had compared to the other schools were very low, also if we do not take them into account (9th) and we just use the averages with the remaining students from the same school, we can  alse see that the statistics decrease but to a much lesser extent. The last analysis where the results were also affected was in the "Math and Reading scores by grade" dataframes, since nan values appeared in the ninth-grade rows of Thomas High School.













