# MBA-decisions-study
A Study on Factors Influencing MBA Pursuit

Dependencies
-------------
Pandas
```
# Import
import pandas as pd

# Locally 
pip install pandas
```

Matplotlib
```
# Import
import matplotlib.pyplot as plt

# Locally through Anaconda (Note: Requires Python Version 3.7 for all functionality)
conda install matplotlib
```

Jupyter Notebook
```
pip install jupyterlab
```

Installation
-------------
```
# Clone Repo
git clone https://github.com/HGrewal13/MBA-decisions-study.git

# Run in Jupyter Notebook
jupyter notebook MBA_Decisions.ipynb
```

Introduction
-------------

We’ve been tasked with identifying factors that influence the decision of employees to pursue an MBA. In this study we work with 10,000 different participants spanning across 5 different job titles – Analysts, Consultants, Engineers, Entrepreneurs, and Managers. 
In order to analyze and test this dataset we’ve decided to break down our analysis by focusing on 3 main areas pertaining to each participant – their education, employment, as well as their age and gender. 

Our hypothesis we will be trying to prove that the following factors would positively influence the pursuit of an MBA:
1) Undergraduates from top ranking schools
2) Being funded by scholarships or through employment
3) Net salary increases
4) 3-4 years work experience
5) Being an average age of 25

Section 1 – Education
----------------------
Analysis 1.1 – Undergraduate Major vs Pursuing MBA
After first extracting only the participants that pursued an MBA, our next step was to identify the different undergraduate degrees and their impact on this study. The undergraduate degrees used in this dataset were very evenly distributed, allowing us to look at each without worrying about under or over representation. This was a positive sign that we wouldn’t have to worry about bias towards representation of one degree over others.
This dataset was comprised of the following degrees along with their representation of MBA pursuers: 
1)	Arts (19.2%)
2)	Business (19.0%)
3)	Economics (21.3%)
4)	Engineering (19.6%)
5)	Science (20.9%)


[!Pie Chart](https://github.com/HGrewal13/MBA-decisions-study/blob/main/Output/fig_1_undergraduate_distribution.jpg)
[](Output/fig_1_undergraduate_distribution.jpg)

Our first analysis showed that each undergraduate degree had an almost equal number of MBA pursuers. Thus, we can conclude that undergraduate major was not a determining factor when identifying which group is more likely to pursue an MBA. 
This test was inconclusive. 

Analysis 1.2 – University Ranking vs Pursuing MBA
To understand the role university ranking has on pursuing an MBA, we separated rankings into 5 groups:
1)	Top 10
2)	Ranks 11 – 50
3)	Ranks 51 – 100
4)	Ranks 101 – 250
5)	Ranks 251 – 500

We then determined the ratio of MBA pursuers to total participants among these 5 groups to identify if MBA pursuers were more likely to emerge from a specific ranking. 

Insert Bar Chart Here

From our bar chart, we can see that Ranks 11-50 and ranks 251-500 were most likely to pursue an MBA among other groups. Ranks 51-100 were the least likely. 
To further understand this data, we performed a logistical regression analysis and determined the model isn’t statistically significant. Our variable “Undergrad University Ranking” had no specific effect on the MBA decision, with a LLR p-value of 0.603 (p-values greater than 0.05 indicate insignificance). The pseudo R^2 value is very low, indicating that the independent variables are insufficient to explain the MBA decision.

This test was inconclusive.

Analysis 1.3 – Undergraduate GPA vs Pursuing MBA
Undergraduate degree followed a similar trend to our first 2 analyses and showed us that although participants with medium level GPAs (B students) were most likely to pursue an MBA at 60% of all medium participants, all the values were still very similar. We determined undergraduate degree was not a deciding factor for pursuing an MBA.

This test was inconclusive.

Analysis 1.4 – Funding Source vs Pursuing MBA
There were 4 funding sources identified in our study – scholarships, self-funded, employer, and loan. These funding sources were evenly represented in our data and so we performed an ANOVA test and determined that with a p-value of 0.5699 and f-statistic of 0.6707, there was no significant difference when considering funding source as an influence on pursuing an MBA.  
This test was inconclusive.
Multivariable Logistic Regression Analysis
We performed one final logistical regression analysis on our entire education dataframe in order to see if there was any other variable that could be used to influence participants’ decision to pursue an MBA. 

Insert Analysis here

All p-values for our columns were over 0.05, indicating there were no variables within this dataset that could be used to determine the likelihood of participants pursuing an MBA.

Our tests for education were inconclusive.



Section 2.1 – Employment
-------------------------
Analysis 1 – Current Job Title vs Pursuing MBA
Our list of participants were among 5 different job titles – Analysts, Consultants, Engineers, Entrepreneurs, and Managers. We calculated the percentage of participants from each job that decided to pursue an MBA, and found that each job title was almost equally as likely to pursue an MBA. 
Insert bar chart here
1)	Analysts: 58%
2)	Consultants: 60%
3)	Engineers: 60%
4)	Entrepreneurs: 60%
5)	Managers: 59%

This test was inconclusive.

Analysis 2.2 – Post MBA Role vs Pursuing MBA
We performed a very similar analysis among the 5 desired post MBA roles identified in our study – Executives, Marketing Directors, Consultants, Startup Founders, and Finance Managers. Again, each role showed essentially no difference in level of impact to pursuing an MBA.

Insert Bar Chart

1)	Consultant: 60% 
2)	Executive: 59% 
3)	Finance Manager: 59% 
4)	Marketing Director: 59% 
5)	Startup Founder: 59%


This test was inconclusive.

Analysis 2.3 – Expected Net Salary Increase/Decrease as a Factor for MBA Pursuers
For this analysis, we first calculated the expected net salary increase/decrease for each participant post MBA, and determined the mean value for each desired post MBA role. The values ranged from $54,000 - $58,000, but this wasn’t sufficient for our tests. 
Next, we decided to segregate the data based on MBA pursuers that expected a salary increase, and MBA pursuers that expected a pay decrease. Among 5,907 participants who pursued an MBA, 5,045 expected a net salary increase, while 862 expected a pay decrease. 

Insert Pie Chart here

This test identified that 85.4% of MBA pursuers were likely motivated by earnings potential as a key factor when making their decision. 14.6% of MBA pursuers expected a net salary decrease, but followed through with their decision. These participants were likely motivated to pursue an MBA for factors relating to career changes, or future career success after a few years of experience.

Thus, we can conclude that a net salary increase has a strong correlation to pursuing an MBA.

Analysis 2.4 – Which Reasons Motivated More Participants to Pursue an MBA
In this dataset, we were given 4 main reasons participants decided to pursue an MBA – entrepreneurship, skill enhancement, career growth, and networking. We split these reasons among MBA pursuers and MBA non-pursuers based on their current job titles. 
For MBA Pursuers:

Insert chart here

Although most of these values were very close, we discovered that networking was the most influential reason for pursuing an MBA for Analysts, Consultants, and Entrepreneurs. It was also the second most influential reason for Engineers. Skill enhancement was also a large driving force for all participants with the exception of managers. Career growth, also had a smaller impact. 

For MBA Non-Pursuers:

Insert Chart here

With the exception of analysts, most MBA non-pursuers considered an MBA but were least likely to do so for entrepreneurship. We found these participants did not value entrepreneurship as a strong enough reason to follow through with pursuing an MBA. Each job title had specific reasons they valued more than others, and there was usually a reason they valued far less, but no other factor of great significance was identified.

Thus we can conclude that for participants that decided to pursue an MBA, networking was the most influential factor. For participants that decided to not pursue an MBA, entrepreneurship was the factor least likely to influence their decision. 

Section 3 – Age and Gender’s Impact on Pursuing an MBA
-------------------------------------------------------
Analysis 3.1 – Gender 

Among all MBA pursuers in this study, we found that the breakdown in terms of gender were as follows:
Male: 50.5%
Female: 44.7%
Other: 4.8%

We can conclude that males are more likely to pursue an MBA, however, females are not far behind with only a 5.8% difference. 

Analysis 3.2 - Age and Gender 

When conducting this analysis, we investigated age as a complimentary factor to gender. Our participants ranged from ages 21 - 34 across all 3 genders. We identified the mean age to pursue an MBA for participants regardless of their gender was 27% across all 3. We were unable to identify a key influence for pursuing an MBA based on the combination of age and gender.

Insert chart here

This test was inconclusive.

Analysis 3.5 - Years of Work Experience by Gender

Among all MBA pursuers, all 3 genders averaged about 4.5 years of work experience. There was no sufficient data to determine work experience based on gender when pursuing an MBA.

This test was inconclusive.

Final Conclusion
-----------------
Although this study was able to determine 2 conclusions: salary increase post-MBA has a strong correlation to pursuing an MBA (see Analysis 2.3), and males are more likely to pursue an MBA (see Analysis 3.1), most of our tests were inconclusive.
We were only able to prove Hypothesis 3: A net salary increase would positively correlate to pursuing an MBA. 
This is largely due to the fact that data across all columns of this dataset are too evenly distributed. We worked with nearly equal values across every portion of the study to the point that almost every analysis yielded similar results no matter how to data was divided.

We can conclude that more diverse data is needed before coming to an accurate conclusion as this is an inaccurate representation of real life.


