# Climate EDA
[Data source](https://www.kaggle.com/datasets/goyaladi/climate-insights-dataset)  
Exploratory data analysis over climate change dataset. Columns description can be found inside data folder. The data covers worldwide climate features such as temperature, precipitation, humidity, etc.  
## Methodology
### ETL process 
* First, some simple extracting as I already downloaded the data from Kaggle.
* Perform transformation on data:
  - Adding continent column by mapping countries. I used the library pycountry-convert to get continent names based on the country. I applied functions to get the country codes for each country and then convert the country code to continent code. Using dictionary of continent names, I mapped the continent code to the full name.
  - Deriving timestamp into date, day, month, monthname, year. This is a fairly simple process which I applied `to_datetime` function first to convert the data type into datetime pandas. Pandas made this easy because they provided functions to extract day, month, monthname, and year from datetime object. So, I created columns for each of them to store them. 
* Loading the data into csv after cleaning and transforming. If further transformation process is needed to enrich the features, we could freely add them before loading the data into csv.
### EDA process
Initially I tried to create visualisations on Jupyter notebook using Seaborn and Matplotlib, but I decided to create a dashboard in Power BI to better visualise the complex line plots. In Power BI, I created an interactive dashboard which the 'interactivity' could not be demonstrated in GitHub. So, I uploaded a pdf file to show a sample overview of it. I also uploaded the `.pbix` file for the original file.
## Insights:
* 
