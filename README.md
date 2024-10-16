# Salifort-Motors-Data-Analysis-project-
Skills covered: Python, Data Analysis, visualization, Machine learning , Future Prediction 
## Salifort Motors Data Analysis project 

### 1 Providing data-driven suggestions for HR 
1.1 Description and deliverables 
This project is an opportunity for me to showcase my data analytics skills using Python skills. In this project, I analyzed a dataset and built predictive models that can provide insights to the Human Resources (HR) department of a large consulting firm. 
This project included an executive summary for external stakeholders and completed Python scripts and visuals. In this specific project, I used a regression model and a machine learning model to predict whether or not an employee will leave the company (ethical considerations in place). 

## 2 Project approach 
### 2.1 Plan 

2.1.1 Understand the business scenario and problem 
The HR department at Salifort Motors wants to take some initiatives to improve employee satisfaction levels at the company. They collected data from employees, but now they don’t know what to do with it. The company wants to have data-driven suggestions based on understanding of the data. They have the following question: What’s likely to make the employee leave the company? 

The goals of this project are to analyze the data collected by the HR department and to build a model that predicts whether or not an employee will leave the company. 
If you can predict employees likely to quit, it might be possible to identify factors that contribute to their leaving. Because it is time-consuming and expensive to find, interview, and hire new employees, increasing employee retention will be beneficial to the company. 

2.1.2 Familiarizing with the HR dataset 
In the dataset, there are 14,999 rows, 10 columns, and these variables: 
Variable Description 

2.1.3 Questions to ask in the plan stage. 
*  Who are the stakeholders for this project? 
*  What are problems to solve or accomplish? 
*  What are the initial observations when exploring the data? 
*  What resources are available to complete this stage? 
*  Any ethical considerations at this stage?

### 2.2. Import python packages  
*  Import packages 

*  Load dataset
  
![image](https://github.com/user-attachments/assets/62398072-ed5d-486e-82ee-110cf3730a2f)


2.2.2 Load dataset

![image](https://github.com/user-attachments/assets/538b8cd7-8947-4fe3-923b-2782d58b20aa)

![image](https://github.com/user-attachments/assets/26a2a41a-7988-4d4d-983c-be5956ac4365)

2.3.1 Gather basic information about the data  

![image](https://github.com/user-attachments/assets/9fe055e9-3162-42ff-9bb0-b6d08454ffcb)

### 2.3 Data Exploration (Initial EDA and data cleaning) 


2.3.2 Gather descriptive statistics about the data 
* Descriptiive statistics gives an idea if the data has significant outliers by looking at the min, max and 25%,50% 75% percentile data values.
   
![image](https://github.com/user-attachments/assets/7fc9049a-4014-4241-9c40-980a0b57ba45)

  ### Data cleaning steps are included in the python notebook in the same repository 
      * Detecting dupliates and dropping legitimate duplicates
      * Renaming the columns to readable names
      * Capping outliers
      * Checking and replacing mising value if exist
        
## 3.  Analyze Stage 

* Analyzing relationships between variables
* Analyzing distributions in the data
* Data transformations and ethical consideration

### Let's Explore the data: find the idea why the employees are leaving the company

![image](https://github.com/user-attachments/assets/d61b96fd-8a93-40ee-8524-51b63ac4dc7d)


![image](https://github.com/user-attachments/assets/30f8f9ea-0c91-4a99-a66c-08a55df8dd44)

It might be natural that people who work on more projects would also work longer hours. This appears to be the case here, with the mean hours of each group (stayed and left) increasing with number of projects worked. However, a few things stand out from this plot. 
1. There are two groups of employees who left the company: (A) those who worked considerably less than their peers with the same number of projects, and (B) those who worked much more. Of those in group A, it’s possible that they were fired. It’s also possible that this group includes employees who had already given their notice and were assigned fewer hours because they were already on their way out the door. For those in group B, it’s reasonable to infer that they probably quit. The folks in group B likely contributed a lot to the projects they worked in; they might have been the largest contributors to their projects.
   
3. Everyone with seven projects left the company, and the interquartile ranges of this group and those who left with six projects was ~255–295 hours/month—much more than any other group. 
4. The optimal number of projects for employees to work on seems to be 3–4. The ratio of left/stayed is very small for these cohorts. 
5. If you assume a work week of 40 hours and two weeks of vacation per year, then the average number of working hours per month of employees working Monday–Friday = 50 weeks * 40 hours per week / 12 months = 166.67 hours per month. This means that, aside from the employees who worked on two projects, every group—even those who didn’t leave the company—worked considerably more hours than this. It seems that employees here are overworked. 

### Exploring major factors of employee satifaction: Let's check the average monthly hours versus the satisfaction levels

  ![image](https://github.com/user-attachments/assets/0de3ec20-b2a2-4987-96d5-8bd638f3af10)
  
The scatterplot above shows that there was a sizeable group of employees who worked ~240–315 hours per month.

315 hours per month is over 75 hours per week for a whole year. It’s likely this is related to their satisfaction levels being close to zero. 
The plot also shows another group of people who left, those who had more normal working hours. Even so, their satisfaction was only around 0.4.
It’s difficult to speculate about why they might have left. It’s possible they felt pressured to work more, considering so many of their peers worked more.
And that pressure could have lowered their satisfaction levels. 
Finally, there is a group who worked ~210–280 hours per month, and they had satisfaction levels ranging ~0.7–0.9. 
Note the strange shape of the distributions here. This is indicative of data manipulation or synthetic data. 

###  Let's visualize the satisfaction levels by tenure and get more insights about the data

![image](https://github.com/user-attachments/assets/89ea9f63-9edb-4cd0-a25a-858e5e4a1b5e)

There are many observations we could make from this plot. - Employees who left fall into two general categories: dissatisfied employees with shorter tenures and very satisfied employees with medium-length tenures. 
Four-year employees who left seem to have an unusually low satisfaction level. It’s worth investigating changes to company policy that might have affected people specifically at the four-year mark, if possible. 
The longest-tenured employees didn’t leave. Their satisfaction levels aligned with those of newer employees who stayed. - The histogram shows that there are relatively few longer-tenured employees. It’s possible that they’re the higher-ranking, higher-paid employees. 

### Let's examine salary levels for different tenures
![image](https://github.com/user-attachments/assets/d9535c8e-a094-4b01-87e5-54d61514b7c0)

* The plots above show that long-tenured employees were not disproportionately comprised of higher paid employees.
* It's intersting to see whether there’s a correlation between working long hours and receiv ing high evaluation scores.

  ![image](https://github.com/user-attachments/assets/7b961f95-54b3-4d31-881b-51477a7a70d3)

  The following observations can be made from the scatterplot above:
    * The scatterplot indicates two groups of employees who left: overworked employees who performed very well and employees who worked slightly under the nominal monthly average of 166.67 hours with lower evaluation scores.
    * There seems to be a correlation between hours worked and evaluation score.
    * There isn’t a high percentage of employees in the upper left quadrant of this plot; but working long hours doesn’t guarantee a good evaluation score.
    * Most of the employees in this company work well over 167 hours per month. 







  

