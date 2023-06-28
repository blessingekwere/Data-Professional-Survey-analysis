# Data-Professionals-Survey-analysis

## Project Overview
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Introductory%20pics.jpg)
*Photo Source: Google*

In the vast world of data professionals, a hidden treasure of insights awaits to be uncovered. The journey begins with a dataset collected from a selected group of data professionals who have willingly shared their experiences and perspectives. Despite the modest number of responses, this collection of data holds the power to reveal valuable patterns and trends that can shape the future of the data industry.

The aim of this analysis project is to delve deep into the minds of data professionals and unravel the mysteries surrounding their roles, challenges, and aspirations. By exploring this dataset, we seek to gain an understanding of the current landscape and dynamics of the data industry. 

With each row representing an individual's unique story, let's embark on an adventure through the vast landscape of data. Different skills ranging from analytical techniques, statistical analysis to visualizations, will be used to extract meaningful insights from the dataset. The objective is not only to uncover trends but also to provide actionable recommendations for individuals, organizations, and the industry as a whole.

Despite the modest size of this dataset, we believe that even a small group of voices can ignite a powerful revolution in the world of data. By meticulously documenting our findings, the aim is to inspire data professionals, inform decision-makers, and pave the way for a brighter future in the world of data.

So, let us embark on this exciting expedition, armed with our analytical tools and a thirst for knowledge. Together, we will unravel the untold stories hidden within the data, and unlock the secrets that will shape the future of the data profession. The adventure begins now!

![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/pics%202.jpg)
*Photo Source: Google*
  

## Data Description
The dataset contains 28 columns and 630 rows and contains the following columns:

* Unique ID: An identifier for each survey response.
* Email: The email address of the participant.
* Date Taken (America/New_York): The date the survey was taken in the America/New_York time zone.
* Time Taken (America/New_York): The time the survey was taken in the America/New_York time zone.
* Browser: The web browser used to take the survey.
* OS: The operating system used to take the survey.
* City: The city where the participant is located.
* Country: The country where the participant is located.
* Referrer: The source that referred the participant to the survey.
* Time Spent: The duration of time spent on the survey
* Which Title Best Fits your Current Role?: The participant's current job title.
* Did you switch careers into Data?: Whether the participant switched careers into the field of data.
* Current Yearly Salary (in USD): The participant's current annual salary in USD.
* What Industry do you work in?: The industry in which the participant is employed.
* Favorite Programming Language: The participant's preferred programming language.
* How Happy are you in your Current Position with the following? (Salary): Happiness level with salary in the current position.
* How Happy are you in your Current Position with the following? (Work/Life Balance): Happiness level with work/life balance in the current position.
* How Happy are you in your Current Position with the following? (Coworkers): Happiness level with coworkers in the current position.
* How Happy are you in your Current Position with the following? (Management): Happiness level with management in the current position.
* How Happy are you in your Current Position with the following? (Upward Mobility): Happiness level with upward mobility opportunities in the current position.
* How Happy are you in your Current Position with the following? (Learning New Things): Happiness level with learning new things in the current position.
* How difficult was it for you to break into Data?: The perceived difficulty of entering the field of data.
* If you were to look for a new job today, what would be the most important thing to you?: The most important factor in considering a new job.
* Male/Female?: The gender of the participant.
* Current Age: The age of the participant.
* Which Country do you live in?: The country of residence of the participant.
* Highest Level of Education: The highest level of education attained by the participant.
* Ethnicity: The ethnicity of the participant.
The link to the original dataset can be found [here](https://docs.google.com/spreadsheets/d/1rRqkV4wVbFIxWBdYREqcxPxP8ONTnzTb/edit?usp=sharing&ouid=101168326616437085538&rtpof=true&sd=true)


## Tool Used: 
* Power BI

## Observation with the data
The following observations were made in the data
* 	Null/missing values
* 	Wrong Formatting
* 	Wrong spellings and abbreviations of words


## Data Cleaning and Preprocessing
For the data cleaning and preprocessing step in the data professional dataset, I followed the following steps:

* Firstly, I loaded the data into Power BI and accessed the Power Query Editor by clicking on the transform tab. This allowed me to initiate the data cleaning process.

![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Screenshot%20(123).png)
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Screenshot%20(124).png)
*Loading the excel file into Power BI Desktop*


* I addressed the issue with the "date taken" column by formatting it to the date data type. However, I encountered errors in some rows. To resolve this, I investigated and identified that changing the regional settings for the file from Nigeria to the United States resolved the problem effectively.
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Screenshot%20(129).png)
*Changing the regional setting for the file to resolve the date error*

* To ensure clarity and descriptive labeling, I renamed all the columns appropriately, providing a clear understanding of the values they hold.

* Since the columns for email, browser, OS, city, country, and referrer were all empty and wouldn't contribute to my analysis, I removed them from the dataset.

* Next, I focused on the "current yearly salary" column (in USD). As the values were entered in ranges, I used a delimiter to split the column into minimum and maximum values. Additionally, I replaced the "k" symbol (representing thousand) in those columns with three zeros.
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Screenshot%20(126).png)
*Replacing the "k" in the minimum and maximum salary column after splitting*

* After splitting the column, I noticed that the maximum value column contained null values, indicating that respondents had only provided one value. To address this, I replaced the null values with zero. I then utilized the custom column feature to calculate the average of the maximum and minimum values for each row, adding a new column named "average salary" to the dataset.

![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Screenshot%20(131).png)
*Using custom column command to add another column called "average salary"*

* Moving on, I encountered null values in columns such as "How Happy are you in your Current Position with the following? (Salary)," "How Happy are you in your Current Position with the following? (Work/Life Balance)," "How Happy are you in your Current Position with the following? (Coworkers)," "How Happy are you in your Current Position with the following? (Management)," "How Happy are you in your Current Position with the following? (Upward Mobility)," and "How Happy are you in your Current Position with the following? (Learning New Things)." I replaced these null values with the respective medians of each entire column.

* In the "job role" column, I replaced the value "Other (specify)" with a blank, leaving only the specified values in the column. If no specified value was present, I input "Not Stated" as a replacement.

* To provide a rating for the columns mentioned above, I employed a conditional column approach. For columns like "How Happy are you in your Current Position with the following? (Salary)," "How Happy are you in your Current Position with the following? (Work/Life Balance)," "How Happy are you in your Current Position with the following? (Coworkers)," "How Happy are you in your Current Position with the following? (Management)," "How Happy are you in your Current Position with the following? (Upward Mobility)," and "How Happy are you in your Current Position with the following? (Learning New Things)," I used the following rating scale: If the selected column value is less than or equal to 2, it is considered "Very Dissatisfied." If the value is less than or equal to 4, it is labeled "Dissatisfied." If the value is less than or equal to 6, it is categorized as "Neutral." If the value is less than or equal to 8, it is regarded as "Satisfied." Otherwise, if the value is greater than 8, it is labeled as "Very Satisfied."
  
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Screenshot%20(127).png)
*Using conditional column to add rating columns by using the values in the above listed columns as a condition*

* Lastly, I addressed the "age" column. Observing that the maximum age was 92, I utilized the conditional column approach once again to establish age categories. The age cateogories were defined as follows: Ages 18-34 were categorized as "Young Adults", Ages 18-34 were categorized as "Middle-aged Adults", and Ages 55 and above were categorized as "Older Adults".
  
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Average%20salary%20by%20age%20category.png)
*Using conditional column to add age category column*

* I then went through my ethnicity column to clean it and get rid of all errors. After which I finally went through each column again one after the other.

* By following these steps, I ensured that the data was properly cleaned and preprocessed, setting the stage for meaningful analysis and insights.

* After I completed the data cleaning, I was left with 630 rows and 31 columns.


## Data Analysis Techniques
To gain valuable insights from the dataset. Some of the used data analysis techniques include:

* Descriptive Statistics
* Data Visualization
* Data Aggregation
* Data Cleaning and Preprocessing
* Data Interpretation and Communication
By applying these data analysis techniques, I was able extract valuable insights, make data-driven decisions, and derive actionable recommendations from the dataset at hand.


## Insights

*	The Data Analyst role had the highest number of respondents, totaling 382, followed by the "other" category which includes different unspecified roles which were not indicated at the point of data entry.
  
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Top%205%20job%20industries%20by%20number%20of%20respondents.png)

*Top 5 Job Roles by number of respondents*

* Female respondents accounted for approximately 25.71% of the total population, while male respondents represented 74.29%.
  
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Respondents%20by%20Gender.png)

*Respondents by gender*


* In terms of average salary by job role, the Data Analyst role topped the list with a total average salary of $21.1M followed by the "other" category which includes different unspecified roles which were not indicated at the point of data entry with $2.5M, while Data Engineers, Data Scientists, and Business Analysts earned $2.4M, $2.3M, and $0.5M respectively.
  
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Average%20salary%20based%20on%20top%205%20roles.png)

*Average Salary by Top 5 Job Roles*


* Among the countries in terms of average salary, United States topped the list with a total of $20.3M.
  
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Average%20salary%20based%20on%20Top%205%20Countries.png)

*Average Salary by Top 5 Countries*


* The Tech industry attracted the highest number of respondents, followed by the Finance and Healthcare industries.
  
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Number%20of%20respondents%20based%20on%20Top%205%20job%20Industries.png)

*Number of respondents by Top 5 Job Industry*


* Python programming language emerged as the most preferred language among respondents, followed by R and SQL.
  
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Top%205%20Favorite%20programming%20Languages.png)

*Top 5 favorite programming languages*


* The number of responses steadily decreased each day. The first day recorded the highest number of responses, reaching 347.
  
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Responses%20by%20day.png)

*Responses by day*



*	In terms of age categorization, individuals aged 18-34 who were categorized as "Young Adults" earned the highest average salary, totaling $25.08M. This was followed by individuls aged 35-54 who were categorized as "Middle-aged Adults" with $8.62M and then followed by individuls aged 55 and above who were categorized as "Older Adults" with $0.04M
  
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Average%20Salary%20based%20on%20Age%20Category.png)

*Average Salary based on Age Category*



* Analyzing the count of salary satisfaction ratings, the visual representation shows that the majority of respondents were very dissatisfied, with a count of 176. This was followed by respondents who were dissatisfied, totaling 164. The neutral, satisfied, and very satisfied categories had counts of 133, 119, and 38 respectively.

![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Salary%20satisfaction%20rating.png)

*Salary satisfaction rating*




* When considering key job considerations, a better salary emerged as the top priority for most respondents. Remote work conditions ranked second, followed by a good work/life balance and a positive work culture.
  
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Top%204%20Key%20job%20consideration.png)

*Top four key job consideration*



## Visualization
![](https://github.com/blessingekwere/Data-Professional-Survey-analysis/blob/main/Dashboard%202.jpg)

*Data professionals survey dashboard*


## Limitations

Limitations and assumptions of this project include:

* **Small Sample Size:** The project is based on 630 responses, which does not fully represent the entire population of data professionals. 

* **Response Bias:** The respondents' answers may be influenced by social desirability bias or personal motivations, potentially leading to biases in the data.

* **Subjective Measures:** The project includes subjective ratings such as salary satisfaction, which are based on individual perceptions and may vary among respondents.

* **Missing Data:** The dataset contains missing values or incomplete responses, which could impact the analysis and interpretation of results.


## Recommendation
Based on the insights obtained from the dataset, the following recommendations can be made:
*	**Focus on recruiting and retaining data analysts and other data professionals:** In order to address the growing demand for data analysts and foster a collaborative data team, it is crucial to prioritize the recruitment and retention of these professionals. This includes considering the services of other key members such as data engineers, data scientists and other professionals who play integral roles within the data ecosystem. By offering competitive salaries, ample growth prospects, and a supportive work environment, organizations can effectively attract and retain talented individuals, ensuring the success and synergy of the entire data team.

*	**Address the gender imbalance:** While the majority of respondents were male, it is essential to promote diversity and inclusivity in all fields of data. Companies can take steps to attract and retain more female professionals by implementing diversity initiatives, providing equal opportunities for career growth, and fostering an inclusive work culture.

*	**Explore opportunities in "other" roles:** The "other" category, comprising unspecified roles, had a notable number of respondents. It could indicate a potential area for further exploration and understanding of emerging roles in the data field. Organizations can investigate these roles to identify emerging trends and skill requirements to stay ahead in the industry.

*	**Consider geographic factors:** The dataset highlights that the United States had the highest average salary. Organizations operating in other countries can benchmark their salary structures and benefits to ensure they remain competitive in attracting and retaining top talent. It is important to consider regional salary trends, cost of living, and local market conditions.

*	**Leverage Python, R, and SQL:** Python emerged as the most popular programming language among respondents, followed by R and SQL. Companies can leverage these languages to enhance their data analysis capabilities, invest in training programs for employees, and encourage the adoption of these languages across teams.

*	**Enhance work-life balance and culture:** Respondents ranked better salary, remote work conditions, work-life balance, and a good culture as top key job consideration. Organizations can focus on creating a positive work environment that promotes work-life balance, flexible work arrangements, and a supportive company culture. This can help attract and retain top talent in the data field.


## Conclusion

In conclusion, the analysis of the dataset provided valuable insights into various aspects of the data industry, including job roles, gender distribution, salary trends, geographic factors, programming language preferences, and job considerations. Despite the limitations of a relatively low number of responses, the findings still offer meaningful implications for organizations and professionals in the field.

The dataset revealed that the Data Analyst role had the highest number of respondents, highlighting the increasing demand for individuals skilled in data analysis. It is crucial for organizations to focus on recruiting and retaining data analysts and other data key professionals to meet this demand and leverage their expertise in driving data-driven decision-making.

The gender distribution showed a male-dominated industry, suggesting the need for concerted efforts to promote diversity and inclusivity. Creating an inclusive work environment and providing equal opportunities for career growth can help attract and retain more female professionals in the data field.

Salary analysis indicated variations across different job roles and countries. Organizations can benchmark their salary structures to remain competitive in attracting and retaining top talent. Furthermore, considering geographic factors such as regional salary trends and market conditions is essential for effective talent management.

The popularity of Python, R, and SQL as preferred programming languages highlights their significance in the data analysis field. Investing in training programs and encouraging the adoption of these languages can enhance data analysis capabilities within organizations.

Work-life balance, remote work conditions, and a positive company culture emerged as key considerations for professionals. Organizations should prioritize creating a supportive work environment that promotes work-life balance and fosters a positive culture to attract and retain talent.

Thank you for taking your time to go through this project. Your comments and recommendation will be highly appreciated

Kindly connect with me on [LinkedIn](https://www.linkedin.com/in/blessing-ekwere-857326216) and [Twitter](https://twitter.com/Eddie_Gregs?t=dF3996shVxvPJTePTtxDdw&s=09)

See you next time😙👋
