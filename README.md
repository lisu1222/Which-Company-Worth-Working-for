# Which Company is Worth Working for?

A study concerning employee reviews for Google, Amazon, Apple, Facebook, Microsoft, and Netflix. 

The Medium Post can be find at: [Which Tech Company is Worth Working for?](https://medium.com/@ls3583/which-tech-company-is-worth-working-for-c21c10f6f1f1)


## Part 1: Business Understanding

**Business Objectives:**     

It is an important question to ask when you try to find a new position on your career path: which company within the industry best aligns with your professional goals? In other words, where to send your resume and apply for a job? To facilitate the answer to this question, many candidates reach for the opinions of employees of these companies. Employee reviews give useful insights into the firms and provide valuable suggestions about whether to work for and grow together with the companies. Through employee reviews, we can compare the similarities between these companies, have a better understanding on which company is worth working for, and conduct the common attributes for each company based on their employee reviews.  

This study aims to help comapnies understand what area to improve meanwhile trying to bring usaful insights for job hunters to help them gain knowledge about how to chooose their dream company. 

This project is specially interested to find answers for the following business questions: 

1. Waht are the similarities and differences from these companies based on employee reviews?  
2. Which company stands out the most from various aspects and is worth working for?  
3. What are the aspects that firms need to improve?  

**Project Plan:**

This project will include the following steps:
1. Data Preprocessing
- Deal with duplicates, missing values, messey data types and formats
2. Data Analysis
- Exploratory Analysis 
- Text Mining and Sentimental Analysis
- Trend Analysis to reveal patterns over time
3. Predictive Modeling with Text
- Use combined text from *pros* and *cons* to predict *overall.ratings* . A document term matrix using tfidf will be created as new predictors.
- regression tree and linear regression will be used to build two models
- predicting performance will be measured using rmse



## Part 2: Data Understanding  

**Source:**   
	The initial cvs file was downloaded from [Kaggle](www.kaggle.com). The original employee reviews’ dataset was scraped from [Glassdoor](www.glassdoor.com), a website where current and former employees anonymously review companies and their management. 


**Size:**  
	The cvs contains over 67k rows and 17 columns.
    
**Columns Details:**    
- 'x': integar, works as row index
- 'company': character, company names including 'Amazon', 'Apple', 'Facebook', 'Google', 'Microsoft' and 'Netflix' 
- 'location': character, where the employee works/worked
- 'dates': character, the date this review was created
- 'job.title', character, the position and employee status
- 'summary', character, brief summary given by the employee who made the review
- 'pros', character, listing pros given by the employee
- 'cons', character, listing cons given by the employee
- 'advice.to.mgt', character, advice to the management levels given by the emoloyee   
-'overall.rating', int, an overall star rating in range between 1 to 5 given by the employee
- 'work-balance.stars', numeric, a star rating specifically for work and life balance situation in this company given by the employee
- 'career.opportunities.stars', numeric, a star rating specifically for career opportunities in this company given by the employee
- 'culture.values.stars', numeric, a star rating specifically for company culture and values given by the employee
- 'senior.management.stars, numeric, a star rating specifically for senior management situation in this company given by the employee
- 'comp.benefits.stars', numeric, a star rating specifically for the compensations and benefits in this company given by the employee
- 'helpful.count', integar, how many 'helpful' did this review received from audience
- 'link', character, website link to this review
      
**Time Range:**     
	2008 - 2018  

**Data Quality**
    Initial data inspection shows that there exist duplicated and missing values in this dataset. Variables' data types are not unified. Some columns should be transformed to usable formats. Multiple steps of data cleaning and preprocessing will be in need before analysis.
    
    
## Part 3: Data Preparation

**Data Selection:** 
Among the 17 columns, we will use 15 of them - 'helful.count' and 'link' will not be the focus of this project. Rows that are related to reviews of the following companies will be used: Google, Amazon, Facebook, Microsoft, Apple and Netflix. 

**Data Cleaning:**
Detailed data cleaning work can be found within the notebook. Here list methods used in this part of work:
- drop duplicated records
- deal with missing values: drop records/replace with mean or mode or 'none' 
- convert to correct data types
- split columns: 'job.title' is split into two columns: 'position' and 'status'
- clean text data: convert to lower case, remove punctuation, remove whitespace from 'pros', 'cons', 'summary' and 'advice.to.mgt'


## Part 4: Exploratory Data Analysis  

**Which company has the most reviews?**  

![](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/count_reviews.png)

Amazon has the largest amount of reviews — over 25,000, and Microsoft follows as the second with less than 20,000. Then comes Apple. Netflix only has 810个reviews in this dataset.

**What are the top 10 job positions that contributed to the reviews?**  

![](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/positions.png)

‘Anonymous Employee’ accounts for the majority，then comes ‘Software Engineer’ and ‘Software Development Engineer’. Apparently employees tend not to reveal their identities when post a company review.

**What are the top 10 locations for employees who made reviews?**  

![](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/locations.png)

Among those who reveal their locations information, Seattle ranks the top location, two cities — Redmond and Seattle are on the list. The second state is California and the third is New York. Outside of U.S., there are also two India locations. This list show worldwide popular places that are concentrated with big technology companies.

**What is the time range of the reviews in this dataset?**  

![](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/time_range.png)


**How differently are those tech companies being rated?**  

![alt text](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/ratings.png)

![Boxplot](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/boxplots.png)


**Which words are used most frequently in the reviews for each company?**

![Google](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/google.png)

Google is praised for its good and smart people, nice food, culture and environment, and blamed for management and pressure from hard projects and long work time.

![Amazon](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/amazon.png)

Amazon is praised for its pay and benefits, it’s learn opportunities, culture and environment, while blamed for poor work-life balance and management.

![Apple](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/apple.png)

Apple has great benefits, amazing people and generous pay. Employee discounts for its product is also well-mentioned as special benefits. And it’s blamed for management, retail and customer issues as well as work-life balance.

![Microsoft](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/microsoft.png)

Microsoft is known for its smart and great people, great opportunities, work-life balance and pay, while blamed for POLITICS and management.

![Facebook](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/facebook.png)

Facebook also bring together smart people and share a great culture. Employees don’t like its work-life balance status, and describing work as ‘hard’ and ‘fast’.

![Netflix](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/netflix.png)

Netflix’s employees are satisfied with its good pay, culture of ‘freedom’ and working environment. But they showed grudge about people getting ‘fired’ and not happy with the team, culture and management. It is the only company here that is blamed for its culture.


**What do employee like and dislike about a company in general?**

![summary](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/summary.png)

**Do current employees review the companies higher than the former ones?**

![trend](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/trend_status.png)

We can tell from the above graph that:
- Current employees rated their firms higher than former employee
- Google has the most satisfied current employee
- Netflix has the biggest gap for company rating between current and former employee

**How did ratings change over time for each company?**

![over years](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/over_years.png)

 - Google: the overall ratings is on stable increase, but other break-down variables show slow decrease over years, especially in culture values
 - Facebook and Netflix share very fluctuant trends over years, it’s the only company whose overall ratings drop in the recent years, but Facebook has the most satisfied senior management over years and its performance in other aspects also stay higher compared to others
 - Amazon: showed steady improvements in every aspect since 2015
 - Microsoft: company benefit stars have decreased the most over years
 - Netflix apparently made a lot efforts in improving employees’ satisfactions, however over years made less-satisfactory progress


## Part 5: Data Modeling: 

We want to use text to predict an employee's overall rating for a company. First of all, we need to prepare the dataset for modeling.  
The initial plan was to use *summary*, however the values contained in this column have very limited value for audience. Only several words were used and mostly are just 'good company' or similar.
Instead, we append *pros* and *cons* to a new single column, and create a document term matrix using Term Frequency - Inverse Document Frequency Weighting.  This term matrix, after transformed to a dataframe, will be used as predictors to predict overall rating.
The data then split to train and test sets. Two machine learning methods were applied in building models: regression tree and linear regression.


## Part 6: Evaluating

Root Mean Square Error (RMSE) is the standard deviation of the residuals (prediction errors). Residuals are a measure of how far from the regression line data points are; RMSE is a measure of how spread out these residuals are. In other words, it tells how concentrated the data is around the line of best fit.

Linear Regression has outperformed with a smaller RMSE, which showing better predictive capability.
RMSE for linear regression: 1.02768442536384
RMSE for regression tree:   1.10288808043191


## Part 7: Recommendations:

We have found some useful insights for both companies and job hunters:
**For companies**

1. Facebook, Netflix, Microsoft and Google to improve working environments
2. Companies should learn from Facebook's senior management strategy to motivate their employees
3. Apple and Netflix need urgent measures to improve work-life balance
4. Netflix should improve their proceess in firing an employee  
5. Microsoft should pay attention to its politics issue

**For Job Seekers**

1. To gain a clear understanding of the company's culture, values, benefits and environment
2. To match the most suitable company based on different personal goals
3. Tips to choose the company:
	- Environment-oriented: Apple and Amazon
	- Higher payment: Facebook and Netflix
	- More career opportunities: Facebook
	- Educational environment: Google & Microsoft
	- Long-term stable development: Amazon
	- Lots of smart employees: Google & Microsoft
	- Be careful of POLITICS: Microsoft


