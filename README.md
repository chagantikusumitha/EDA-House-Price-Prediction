# EDA-House-Price-Prediction
Exploratory data analysis (EDA) is used by data scientists to analyze and investigate data sets and summarize their main characteristics, often employing data visualization methods.      
Here, We are exploring all the features in determining Price of a house in Hyderabad.

# What is the use?

Exploratory Data Analysis (EDA) is an approach to analyze the data using visual techniques. It is used to discover trends, patterns, or to check assumptions with the help of statistical summary and graphical representations.It allows teams within businesses to collaborate and achieve better results. It is useful for businesses to analyse past business performance and optimize future business processes.Hence, it is mainly used in decision making.   

House Price prediction, is important to drive Real Estate efficiency. As earlier, House prices were determined by calculating the acquiring and selling price in a locality. Therefore, the House Price prediction is very essential in filling the information gap and improve Real Estate efficiency. With this, we would be able to better predict the prices.

# Contents :

## Steps Involved for Exploratory Data Analysis are:
Step1 - Data Collection.ipynb    :  ___Data Collection___                       
Step2 - Data Cleaning.ipynb      :  ___Data Cleaning___                    
Step3 - Data Manipulation.ipynb  :  ___Data Manipulation___               
Step4 - Data Analysis.ipynb      :  ___Data Analysis___                                


### 1. Data Collection 
Data collection is a process of gathering information from all the relevant sources and sorting it in a systematic order which is easily understandable.   
Here, We have used a website called https://www.makaan.com/real-estate-hyderabad-property for collecting data.
We have collected data by using Web Scrapping
##### Web Scrapping :
       Web scraping is a software technique of extracting information from the website .
       It  takes the unstructured data into structured data that can be stored and analyzed.
       We have to send a request to the URL of the webpage .  
       If we get the status code as 200 we can scrap the HTML context from webpage.
       BeautifulSoup is a python library for extracting the data from HTML files.

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
By using all these analysis we understood that,        

 - When sft of the house increases Prices also increases                  
![image](https://user-images.githubusercontent.com/92007497/212992798-877f8eef-e397-4125-9380-e0bbd6b6ffce.png)

 - These are the locations where prices are high.        
 - Here Hitech City is frequently repeated which means Hitech City has the more highest Prices among all the Locations
![image](https://user-images.githubusercontent.com/92007497/212996523-9346dffb-287b-4fbe-9d75-3c5b8b09512b.png)


 - These are the locations where prices are low          
 - Here Sadashivpet and Shadnagar is frequently repeated which means these has the lowest Prices among all the Locations           
![image](https://user-images.githubusercontent.com/92007497/212993893-89fdba5e-2b06-4abd-b16c-336f2a2bbd19.png)


## Conclusion

Finally, we can say that exploratory data analysis is a proven methodology that can help Data Scientists to make sense of complex datasets. By using visualizations and other methods, you can uncover patterns and relationships similar to the following relationships.

> _According to the data, 59.7% are 3 BHK properties, 31.2% are 2 BHK properties,8.5% are 4 BHK properties and 0.6% are 1 BHK properties.      
Maximum number of houses are Apartments and Under construction.             
Maximum number of houses are in Kompally ,Hyderabad.             
All the numerical columns have positive correlation                    
As the sqft increases the no. of bhk’s and total price increases                    
Villa has more sft and 4bhks and 5bhk’s compared to apartment and independent houses.                 
In Apartment and Independent houses we have 2 and 3 BHK houses only.                 
Houses which are in the area range 500 sqft to 2000 sqft have the price range 40 lakhs to 2.6Crores               
In Hitech City prices of houses are high where as Sadashivpet has low prices.                   
Buying a house directly from the owner costs less price when compared to buying from agent or builder._
 
We conclude that House price prediction can help the developer determine the selling price of a house and can help the customer to arrange the right time to purchase a house. There are three factors that influence the price of a house which include sft,construction status,type and location. 


## References

These are the reference sites for collecting real estate data apart from the one I used.              
https://www.99acres.com                                              
https://www.commonfloor.com                   
https://www.modibuilders.com               
