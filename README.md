# Employee Retention Dataset

* Employee turn-over is a very costly problem for companies.
* The cost of replacing an employee if often larger than 100K USD, taking into account the time spent to interview and find a replacement, placement fees, sign-on bonuses and the loss of productivity for several months.
* It is only natural then that data science has started being applied to this area.
* Understanding why and when employees are most likely to leave can lead to actions to improve employee retention as well as planning new hiring in advance. This application of DS is sometimes called people analytics or people data science
* We got employee data from a few companies. We have data about all employees who joined from 2011/01/24 to 2015/12/13. For each employee, we also know if they are still at the company as of 2015/12/13 or they have quit.
* Beside that, we have general info about the employee, such as avg salary during her tenure, dept, and yrs of experience.

**Goal:**

In this challenge, you have a data set with info about the employees and have to predict when employees are going to quit by understanding the main drivers of employee churn.
* Assume, for each company, that the headcount starts from zero on 2011/01/23. Estimate employee headcount, for each company, on each day, from 2011/01/24 to 2015/12/13. That is, if by 2012/03/02 2000 people have joined company 1 and 1000 of them have already quit, then company headcount on 2012/03/02 for company 1 would be 1000.
* You should create a table with 3 columns: day, employee_headcount, company_id. What are the main factors that drive employee churn? Do they make sense? Explain your findings.
* If you could add to this data set just one variable that could help explain employee churn, what would that be?

**Data:** (data/employee_retention_data.csv)

Columns:

* employee_id : id of the employee. Unique by employee per company
* company_id : company id.
* dept : employee dept
* seniority : number of yrs of work experience when hired
* salary: avg yearly salary of the employee during her tenure within the company
* join_date: when the employee joined the company, it can only be between 2011/01/24 and 2015/12/13
* quit_date: when the employee left her job (if she is still employed as of 2015/12/13, this field is NA)

### Question 1

#### Write a function to convert given CSV file to Dataframe

* Define function with name `csv_to_dataframe` which should accept `filepath` as a parameter.
* Function should return a dataframe.
* As we require a dataframe, type of return variable should be pandas dataframe.
* In case if we pass `filepath` which does not exist, function should raise FileNotFoundError.

### Question 2

#### Write a function to convert datatype of given variables to "category"

* Define function with name `dtype_category` which should accept `dataframe` and `list of columns` as parameters.
* Function should return a dataframe with type of given columns changed to "category".
* As we require a dataframe, type of return variable should be `pandas dataframe`.
* In case if we pass column name which does not exist, function should raise KeyError

### Question 3

#### Write a function to to center and scale numerical variables.

* Define function with name `centre_and_scale` which should accept `dataframe` and `column_list` as parameters.
* Function should return a dataframe given columns of numerical variables being centred and scaled.
* As we require a dataframe, type of return variable should be `pandas dataframe`.
* In case if we pass column name which does not exist, function should raise KeyError

### Question 4

#### Write a function to encode all nominal categorical variables using label encoding

* Define function with name `label_encoder` which should accept `dataframe`, `column_list` (of variables to be encoded) as parameters.
* Function should return dataframe with encoded variables.
* As we require dataframe, type of return variable should be pandas dataframe.
* In case if we pass column name which does not exist or is not categorical type, function should raise KeyError

### Question 5

#### Write a function to encode nominal categorical variables using one hot encoding

* Define function with name `one_hot_encoder` which should accept `dataframe`, `column_list` (of variables to be encoded) as parameters.
* Function should return dataframe with encoded variables.
* As we require dataframe, type of return variable should be pandas dataframe.
* In case if we pass column name which does not exist or is not categorical type, function should raise KeyError

### Question 6

#### Write a function to return skewness of numerical variables:

* Define function with name `skewness` which should accept `dataframe`, `column_list` (of variables whose skewness is to be determined) as parameters.
* Function should return list of skewness of given columns
* As we require list of values, type of return variable should be list
* In case if we pass column name which does not exist or is categorical type, function should raise KeyError

### Question 7

#### Write a function to return sqrt transform of numerical variables

* Define function with name `sqrt_transform` which should accept `dataframe`, `column_list` (of variables which are to be sqrt transformed) as parameters.
* Function should return dataframe of sqrt transformed columns of given columns
* As we require list of values, type of return variable should be list
* In case if we pass column name which does not exist or is categorical type, function should raise KeyError

### Question 8

#### Write a function to plot  histogram and box plot of transformed  vs original numerical variables:

* Define function with name `plots` which should accept `dataframe`, `column_list` (of variables to be plotted) as parameters.
* Function should return subplots of histogram and boxplots for the numeric variables.
* As we require plot, type of return variable should be matplotlib object.
* In case if we pass column name which does not exist, function should raise KeyError