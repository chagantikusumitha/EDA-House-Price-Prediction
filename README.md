# EDA-House-Price-Prediction
Exploratory data analysis (EDA) is used by data scientists to analyze and investigate data sets and summarize their main characteristics, often employing data visualization methods.      
Here, We are exploring all the features in determining Price of a house in Hyderabad.

## Steps Involved for Exploratory Data Analysis are:

___1. Data Collection___      
___2. Data Cleaning___          
___3. Data Manipulation___        
___4. Data Analysis___            


### 1. Data Collection 
Data collection is a process of gathering information from all the relevant sources and sorting it in a systematic order which is easily understandable.   
Here, We have used a website called https://www.makaan.com/real-estate-hyderabad-property for collecting data.
We have collected data by using Web Scrapping
##### Web Scrapping :
       Web scraping is a software technique of extracting information from the website .
       It  takes the unstructured data into structured data that can be stored and analyzed.
       We have to send a request to the URL of the webpage we want to access .  
       If we get the status code as 200 we can scrap the HTML  context  from webpage.
       BeautifulSoup is a python library for extracting  the data from HTML files.

In this way after collecting the data we have stored it systematically in a Data Frame
Now the data collected looks in this way
![image](https://user-images.githubusercontent.com/92007497/212983576-ea7a1f53-3e53-4357-bfbd-2077dcff50a7.png)


### 2. Data Cleaning
Data Cleaning is a process of Removing duplicate or irrelevant data, Fix structural errors, Handle missing data, Validate the quality of data.
The cleaned data looks in this way
![image](https://user-images.githubusercontent.com/92007497/212987795-e0ffd00b-86a3-46d5-adb8-21c9f1feeda1.png)
Data cleaning is done in the following steps:
 -  Dropped Titles column after extracting Type , Colony and BHK from it.   
 -  Dropped colony column as there are many null values in it.    
 -  Got all the inaccurate values for BHK of residential plot columns, so filled it with mode based on sft.    
 -  Filled null values for Handover column based on construction_status of the house.   
 -  Dropped duplicate rows.   
 -  Extracted type of seller data from seller_info column.   


### 3. Data Manipulation
Data Manipulation is done to sort Outliers of the data because Outliers are those which are extremely high or low values compared to the whole data. If outliers are not sorted it effects the whole data analysis results

Sorting outliers is done for all the numerical columns of the data which include BHK,sft,Costpersft,Prices columns by using the following steps :
 - Sorting values from low to high and checking minimum and maximum values.
 - Visualizing data with a box plot and looking for outliers.
 - Using the interquartile range to create fences for your data.
 - Using statistical procedures to identify extreme values.
 - Replacing the outliers with median values of the data

### 4. Data Analysis
Data analysis can be classified as Univariate, Bivariate, and Multivariate analysis.   
Univariate analysis looks at one variable, Bivariate analysis looks at two variables and their relationship. Multivariate analysis looks at more than two variables and their relationship.

