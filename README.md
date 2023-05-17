### **Case**

This second project serve as a practice to familiarise with data using Python and to brush up my Python skills. In project 1 the main languages were basic SQL, R and Tableau, project 2 will focus on consolidating data cleaning, analysis and visualisation using Python only.

<br>

### **Ask**

As per the project title I aim to use Python and statistical data packages to perform EDA on this dataset. The goal is to understand the data, identify patterns, relationship using correlation plots, summary statistics or visuals. This will serve as the starting point to gain insights about the data and educate myself the process of EDA.

Our study is exploratory, so instead trying to explain the relationship of weather metrics against a respondent variable, we want to see if the metrics have any relationship between them.

<br>

**The problem I'm trying to answer are:**

- Are there correlation between different weather metrics?
- What trend can I identify by using statistical and visualisation tools?
- Are there significant differences comparing weather data from certain time frame against weather data one decade afterwards?

<br>

I will treat this project as a training and study opportunity dealing with data using Python so that the concept does not feel alien to me, the methods used may or may not have extracted the gist of the data and if it has not, please feel free to comment or give advise on how can I further improve the EDA process.

<br>

### **Preparing**

The dataset is downloaded from Kaggle, a well known site to share data and projects in the data community. The observations within the dataset itself was sourced from an app called 'Dark Sky' via API. Dark sky is an app for weather forecasting and extracts data from the National Meteorological Center.

Our data is organised on a time series basis on an hourly basis over 11 years, with each observations showing us measurements like temperature, wind speed, humidity, visibility and so on.

The dataset size is small to moderate with about 100,000 rows, knowing that data from Kaggle are usually pre-cleaned I am not too worry about any extensive cleaning to be done. But to make sure the data is ready to be manipulated I will import them into a pandas dataframe to do any necessary checks.

<br>

**This dataset will help me to:**

* Most of the observations data are numerical, this allows me to run a predictive model.
* Time frame data allows me to plot trends and compare data between two periods.

<br>

### **Cleaning**

I’m only using Python data wrangling and manipulation packages such as Pandas, Numpy.

To ensure the integrity I look at the observations for each column and decide whether the values makes sense. For example humidity data is usually recorded as a percentage with 100% signifying maximum humidity at certain temperature. The recorded data has a range of 0 to 1 which makes sense. Wind bearing takes a value from 0 to 359 to represent wind direction from North, rotating clockwise and back to north, so the data format is also correct. I do this for all the columns.

<br>

**I have done the following to make sure my data is clean**

* I used Python’s duplicate function to clean duplicates.
* I renamed columns which makes it earlier to refer for the entire project.
* I checked the date with LEN and count() function to make sure date format is consistent, then parse the separated date to another column
* I used the isnull() and isna() function to find null or NA values
* I used the .info() function to make sure that columns data type are in line with the data type of observations.
* No spelling error because the data is number
* Dropped columns not related to the study

Details of cleaning and manipulation are within the uploaded Jupyter notebook.

<br>

### **Analysis**

The analysis process involves model training and testing using Scikit's function to split the data, then building a model using part of the data. After the training I then proceed to test the accuracy of the newly trained model by passing the remaining data from our split, then compare the model's predicted value against the true observed value to judge the prediction power of this model. 

This applies to all regression I run.

In my analysis results I found that the correlation between most of the variables to be extreme low, for example area of lower pressure are usually associated with higher wind speed but in our dataset, the relationship between there two variables is very weak. The full breakdown with summary is documented within the notebook.

<br>

### **Visualisation**

Plots and graphs were made using Python's visualisation packages instead of Tableau, which was what I've used in my first project. Though useful and easier to work with drag and drop interface, using Python to plot is a skill I want to be familiar with and explore what I can do with it.

<br>

### **Thoughts**
Some ideas about this second project were inspired by the community at Kaggle, Medium articles and other websites. This has been a fruitful but extremely frustrating at times learning a new language from a completely different background. I caught myself stuck at the same problem after 3 hours of Google and unable to find an answer. I must admit at times I felt lost whether data analysis is what I would enjoy long run, but on the other hand I tell myself as a complete newbie this is at least something to be proud of. 

I'm writing this here to keep myself accountable: In my next project I am going to use Python with BeautifulSoup to web scrape. Like this project, I have no experience using the tools and unfamiliar with HTML, and this is a big dive into another aspect of Python. I can already see a lot of frustrating hours but I will keep this going until I can confidently say "Yes I am very comfortable using Python to do 'this'"

If you have any suggestions about the findings or any comments at all please don't hesitate to reach out. I'm learning to be a proficient data analyst and appreciate mentorship as well if you're feeling kind.
