# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

### Problem Statement

You are a working as a school counselor in the San Diego Unified School District in California. You are tasked to conduct an information session to a group of top-performing high school students from various schools in the district, to provide them with insights on the SAT scores they should achieve to enter their dream colleges and majors.

---

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|school|object|Ranges of Accepted ACT & SAT Student Scores by Colleges|College|
|number_of_applicants|int|Ranges of Accepted ACT & SAT Student Scores by Colleges|Number of applicants for the college|
|accept_rate|float|Ranges of Accepted ACT & SAT Student Scores by Colleges|Proportion of applicants accepted into the college|
|sat_total_25th_percentile|float|Ranges of Accepted ACT & SAT Student Scores by Colleges|SAT score in which 25% of applicants scored below this score|
|sat_total_75th_percentile|float|Ranges of Accepted ACT & SAT Student Scores by Colleges|SAT score in which 75% of applicants scored below this score|
|top_ten|object|Ranges of Accepted ACT & SAT Student Scores by Colleges|Whether the college belongs to top ten in terms of acceptance rate|
|intendedcollegemajor|object|2019 SAT Scores by Intended College Major|College major in which SAT test takers intend to apply to|
|testtakers|int|2019 SAT Scores by Intended College Major|Number of SAT test takers|
|proportion|float|2019 SAT Scores by Intended College Major|Proportion of SAT test takers, from a total number of 2.2 million test takers|
|total|float|2019 SAT Scores by Intended College Major|Mean total score of SAT test takers by intended college major|
|readingwriting|float|2019 SAT Scores by Intended College Major|Mean score for Evidence-based Reading and Writing score by intended college major|
|math|float|2019 SAT Scores by Intended College Major|Mean score for Math score by intended college major|
|top_five|object|2019 SAT Scores by Intended College Major|Whether the college major belongs to top five in terms of mean total SAT score|

---

### Summary of Analysis

The colleges with less than 10% acceptance rate had 74% more applicants than the other colleges in the dataset. The 25th and 75th percentile of mean total SAT scores of these applicants were also notably higher by 15-24%. This could possibly due to these colleges being more prestigious or having more particular admission criteria, and therefore required higher scores as well for entry consideration.

The top 10 colleges had a mean acceptance rate of 6.5%, and were even more competitive with 110% more applicants than the other colleges. The 25th and 75th percentile mean total SAT score of these applicants were also higher by 16-26%. Again, this is expected as the top 10 colleges are extremely competitive with high number of applications from students hoping to win a spot in the colleges and that these colleges accept only the best of the best students.

The top 5 most popular college majors by SAT test takers had a whopping 327% more test takers than all the college majors. Despite the popularity of these college majors, the SAT scores of test takers applying for them did not have a notable difference (3% higher) compared to the population of all test takers. This could possibly mean that these college majors are in high demand right now and therefore attracted many students to apply for the college major.

The top 5 college majors were popular among test takers, with 101% more test takers than the other college majors. The mean total SAT score for these 5 college majors was also 4% higher than the population of all test takers. While it may come as a shock that the SAT scores required is not as high, it could be due to a high industry demand for students to undertake these college majors and thus were able to accept lower SAT scores to fill the supply gap.

---

### Conclusion and Recommendations

The top 10 colleges expectedly accepted SAT scores that were the highest amongst the other colleges. The data showed that the 25th percentile of mean total SAT score for the top 10 colleges were in the approximate range of 1400-1500, and students vying for a spot in these colleges could use this information as a rough gauge. Aspiring students are recommended to obtain a score of at least 1400 during their revision to have a decent chance of obtaining admission.

The top 5 college majors with test takers of the highest mean total SAT scores were in the approximate range of 1150-1250, and students that are interested to undertake these college majors could gauge their readiness from their scores during revision. However, we recommend students to undertake the college major based on their passion instead of looking at the SAT scores required to enter and that this information was meant for comparison purposes.

---
