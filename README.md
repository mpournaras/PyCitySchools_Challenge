# PyCitySchools Challenge:

## Overview:

On a tip from the schoolboard that 9th graders at Thomas High School had cheated on math and reading exams, our team was instructed to perform an analysis. This analysis was to be done by removing their scores without altering the other data. We want to see how it affects various metrics at a school and district level.

## Results:

### The first thing we wanted to look at was how the district summary was affected. 

By removing the 461 9th-grade test scores we are able to see that quite a few metrics change, if only by a few 1/10ths of a percent. all changed metrics go down!

Top: Original District Summary:
![file](https://github.com/mpournaras/PyCitySchools_Challenge/blob/main/Resources/District.png)

Bottom: New District Summary:
![file](https://github.com/mpournaras/PyCitySchools_Challenge/blob/main/Resources/District_New.png)

### The second thing we wanted to look at was how the school summary was affected. 

By removing the 461 9th-grade test scores we are able to see that quite a few metrics change once again. The passing rate for math, reading, and overall scores all go down. This is because the total student count was not adjusted (2nd pic.). When we adjust the student count to remove the 9th graders scores seem to normalize quite a bit (3rd pic.)

Top: Original School Summary:
![file](https://github.com/mpournaras/PyCitySchools_Challenge/blob/main/Resources/SchoolSummary_Orig.png)

Middle: New District Summary (with cheating scores replaced by NaNs):
![file](https://github.com/mpournaras/PyCitySchools_Challenge/blob/main/Resources/SchoolSummary_NaN.png)

Bottom: New District Summary (with just counting 10-12th graders):
![file](https://github.com/mpournaras/PyCitySchools_Challenge/blob/main/Resources/SchoolSummary_10_12.png)

### The third thing we wanted to look at was how Thomas High School's performance vs other schools was affected. 

Referencing the top picture, we can see that Thomas High School is performing in the top half of district schools. However, when adjusting for the ninth-grader's replaced scores in the second picture, we see they are still in the top half... in the same position even. The percentages have changed a little bit but we can see those changes are inconsequential when compared to the schools above and below it. the 2nd and 5th overall-performing schools are only separated by .05%!

Top: Original Position:
![file](https://github.com/mpournaras/PyCitySchools_Challenge/blob/main/Resources/Top.png)

Bottom: New Position (with just counting 10-12th graders):
![file](https://github.com/mpournaras/PyCitySchools_Challenge/blob/main/Resources/Top_New.png)

### The fourth thing we want to address are the school's scores grouped various ways.

#### We can begin by addressing how the average math and reading scores are grouped by grade and school. There was no change with the exception of "NaN" for Thomas High School. This makes sense because those were the only scores we altered in the new analysis. 10th, 11th, and 12th grade scores were unchanged across all schools. The first image is "math scores" and the second image to the right of it will be "reading scores". I have only included the updated scores here as they are the only ones that are of interest to this particular metric.

Left: Math Scores by Grade and School, Right: Reading Scores by Grade and School:


![file](https://github.com/mpournaras/PyCitySchools_Challenge/blob/main/Resources/MathByGrade_New.png)![file](https://github.com/mpournaras/PyCitySchools_Challenge/blob/main/Resources/ReadingByGrade_New.png)


### The fourth thing we want to address are the school's scores grouped various ways.

#### Following the grouping by grade, we can take a look at how the scores change based on funding levels.

We binned funding into 4 groups to get relatively even spread among the 4 groups. There was no meaningful change after altering the cheating data, however we are able to tell that as funding increases... overall passing grades decrease. That is an interesting statistic!

Scores by Funding Level:
![file](https://github.com/mpournaras/PyCitySchools_Challenge/blob/main/Resources/ScoresByFunding.png)

#### Following the grouping by funding buckets, we can take a look at how the scores change based on school size.

We binned school size into 3 groups to get relatively even spread among the 3 groups and to address the obvious fact that no school is going to have less than 50 students or a similar statistic. There was no meaningful change after altering the cheating data, however we are able to tell that as school size increase... overall passing grades decrease. Just like the funding analysis it is an interesting statistic!

Scores by School Size:
![file](https://github.com/mpournaras/PyCitySchools_Challenge/blob/main/Resources/ScoresBySize.png)

#### Finally, we analysized grouping by school type, we can take a look at how the scores change based on school type.

We grouped them by school type. Our values were "District" and "Charter". Once again there was no meaningful change post grade adjustment... but we can see a few things pretty clearly. Charter schools have a pretty substantial advantage over district schools in regards to passing grades, and test scores in all categories.

Scores by School Type:
![file](https://github.com/mpournaras/PyCitySchools_Challenge/blob/main/Resources/ScoresByType.png)


## Summary:

There are a few changes we can see after reading and math scores have been replaced by NaNs at Thomas High School.

1) The district scores decreased just about across the board. It was only a .1 drop on Average Math Scores, .1% and .2% decreses in Passing Math Score and Reading scores, and .3% drop in Overall Passing Percentage. This could be explained by cheateing scores generally being higher than hinest scores. They are small changes but it is importnat to remeber the district scores are spread over almost 40,000 students! IT will be hard to substantially change a population of that size. Praise statistics!

2) The percent passing reading, math, and overall dropped dramatically in the School Summary when we did not adjust student size for the NaN scores. Thomas High School is relatively small at 1635 students so having some 1/4 of the scores calculate at 0 when adding to the average is detrimental.

3) In the very same summary, we were able to normalize the data by removing that NaN scores from the average. All metrics were able to bounce back to within roughly 1% of their original levels. This shows that cheating aside, the Thomas High School students perform very well as evidenced by their immobile postion in the top 5 schools list.

4) School performace appears to drop dramatically with an increase in school size and funding. It is clear that larger district schools are able to pay less attentino to students and based on that, among other factors, students are performing worse across the board. This is the first thing I would addresss as a school board.

  - 36% variation in overall passing % based on funding
  - 32% variation in overall passing % based on size
  - 36% variation in overall passing % based on school type.


