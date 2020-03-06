# Which Company is Worth Working for?

A study concerning employee reviews for Google, Amazon, Apple, Facebook, Microsoft, and Netflix. 

The Medium Post can be find at: [Which Tech Company is Worth Working for?](https://medium.com/@ls3583/which-tech-company-is-worth-working-for-c21c10f6f1f1)


## Part 1: Project Motivations

**Business Objectives:**     

It is an important question to ask when you try to find a new position on your career path: which company within the industry best aligns with your professional goals? In other words, where to send your resume and apply for a job? To facilitate the answer to this question, many candidates reach for the opinions of employees of these companies. Employee reviews give useful insights into the firms and provide valuable suggestions about whether to work for and grow together with the companies. Through employee reviews, we can compare the similarities between these companies, have a better understanding on which company is worth working for, and conduct the common attributes for each company based on their employee reviews.  

This study aims to help comapnies understand what area to improve while try to bring insights for job hunters to help them know better about their dream companies. 

I am specially interested to find answers for the following questions with this project: 

1. Waht are the similarities and differences from these companies based on employee reviews?  
2. Which company stands out the most from various aspects and is worth working for?  
3. What are the aspects that firms need to improve?  

## Part 2: Data Description  

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


## Part 3: Data Analysis  

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

![alt text](https://github.com/lisu1222/which-company-worth-working-for/blob/master/images/cons_pros.png)
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


## Part 4: Conclusion

### Recommendations:

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


