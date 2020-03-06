# Which Company is Worth Working for?

A study concerning employee reviews for Google, Amazon, Apple, Facebook, Microsoft, and Netflix. 

## Overview

- Part 1: Project Motivations
- Part 2: Methodology       
	2.1 Data Preprocessing  
	2.2 Text Mining & Sentimental Analysis  
	2.3 Trend Analysis  
- Part 3: Conclusion  

## Part 1: Project Motivations

Business Objectives:     

It is an important question to ask when you try to find a new position on your career path: which company within the industry best aligns with your professional goals? In other words, where to send your resume and apply for a job? To facilitate the answer to this question, many candidates reach for the opinions of employees of these companies. Employee reviews give useful insights into the firms and provide valuable suggestions about whether to work for and grow together with the companies. Through employee reviews, we can compare the similarities between these companies, have a better understanding on which company is worth working for, and conduct the common attributes for each company based on their employee reviews.   

We are specially interested to find answers for the following questions with this project:  
1. Waht are the similarities and differences from these companies based on employee reviews?  
2. Which company stands out the most from various aspects and is worth working for?  
3. What are the aspects that firms need to improve?  

### Data Description  

**Topic:**  
	Tech company reviews of employees  
**Companies:**  
	Amazon, Apple, Facebook, Google, Microsoft and Netflix  
**Size:**  
	over 67k records and 15 variables        
**Time Range:**     
	2008 - 2018        
**Source:**   
	The initial dataset was downloaded from [Kaggle](www.kaggle.com). The original employee reviews’ dataset was scraped from [Glassdoor](www.glassdoor.com), a website where current and former employees anonymously review companies and their management.    
**Variables:**   
	15 variables in total   
	- Character: company name, location, position, summary, pros, cons, advice to management   
	- Numeric: overall rating, work-balance rating, career opportunities rating, culture values rating, senior management rating, comp& benefits rating

## Part 2: Methodology

![Methodology](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/methodology.png)
![Boxplot](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/boxplots.png)
![alt text](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/cons_pros.png)
![Google](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/google.png)
![Amazon](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/amazon.png)
![Apple](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/apple.png)
![Microsoft](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/microsoft.png)
![Netflix](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/netfliix.png)
![sentimental analysis - emotions](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/senti_emotion.png)
![summary](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/summary.png)
![trend](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/trend_status.png)
![over years](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/over_years.png)

 - Google: the overall ratings is on stable increase, but other break-down variables show slow decrease over years, especially in culture values
 - Facebook: Facebook and Netflix share very fluctuant trend over years, but Facebook has the most satisfied senior management generally and its performance in other aspects stay higher compared to others
 - Amazon: showed steady improvements in every aspect since 2015
 - Microsoft: company benefit stars have decreased the most over years
 - Netflix: had the most fluctuant trends 

## Part 3: Conclusion

#### Recommendations:

**For companies**

1. Facebook, Netflix, Microsoft and Google to improve working environments
2. Companies should learn from Facebook's senior management strategy to motivate their employees
3. Apple and Netflix need urgent measures to improve work-life balance
4. Netflix should improve their proceess in firing an employee  

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




