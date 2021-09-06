###Sanjoy Kumar Biswas

###Scrape Job portal data

Step 1 :

First go through the problem statement that which domain data I need to collect and which type of columns and information gather by scrape the site.


Step 2 :

Find the bunch of particular URL from where I scrape the information. For the problem statement I will choose indeed.com , monster.com, linkedin.com such type of job portal website.


Step 3 :

Inspect the web page: 
As a lot of information store in webpage, I don’t need all the information. On basis of problem statement I inspect the webpage and highlighted the HTML to get particular information form webpage. And findout the data I want to extract.


Step 4 : 

Extract the data from webpage :
Now extracting data from those website. For extracting data by web scraping I will choose Python library BeautifulSoup.


Step 5 :

After scraping data I will do preprocess every dataset Like , 
Date-Time : May be different dataset have different date time format. I will do make a several format .


Drop unnecessary columns . Drop null and duplicate rows. Scaling all the dataset . 


As every datatsets don not have all the Columns . I will do rescale the columns for all scraping datasets that’s all dataset contain same columns and can merge easily
Like : indeed.com [German] contain columns are company_name, job_title, city, years of experience, salary [Lets say missing columns- Skills]

Monster.com [German] contain columns are company_name, job_title, city, year_of_experience,skills [Lets say missing columns- Salary]

This time I will do which columns are common for those two (any number) datasets. 

For job portal scraping I get must having columns are Job_title & company_name

Now I will make a model data columns after merge which information we need.

Model columns : company_name, job_title, city, year_of_experience, skills,salary

Then I will merge those two dataset by those columns.


Step 6 : 

Fill missing value [skills] for indeed.com:
For fill missing rows I will apply machine learning model here. Like we have dataset of monster.com where I get skills columns. I will take this dataset for train the model and for testing I will apply indeed.com dataset. 
Fill missing value [salary] for monster.com:
For missing columns of salary at monster.com I will use any regression machine learning algorithm to fill those missing rows . And for train dataset I will take indeed.com data as its have salary columns.
