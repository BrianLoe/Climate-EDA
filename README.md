# Climate EDA
[Data source](https://www.kaggle.com/datasets/goyaladi/climate-insights-dataset)  
Exploratory data analysis over climate change dataset. Columns description can be found inside data folder. The data covers worldwide climate features such as temperature, precipitation, humidity, etc and it is collected from 2000-2022. I discovered that the data was not accurate and not consistent. **The data is assumed to be generated and therefore is not a real data.**
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
Since this is not real data, the weather metrics are misleading for some countries.
* The average temperature over years (14.94°C) worlwide fluctuates which peaks in 2005.
Based on continent:
* South America:
  - The continent with most significant changes in climate.
  - In 2009, the temperature reached the lowest of almost 13°C and peaks in 2016 with around 18°C.
    * February is the highest and starts to decrease until December.
  - Produced the lowest CO2 emission during 2013, 2015, 2022.
    * Lowest in July and peaks in December. 
  - Experienced the highest and lowest sea level rise in 2004 and 2016 respectively.
    * Fluctuates and peaks in October. 
  - Has the lowest rainfall in 2002, 2017 and highest in 2019.
    * Significanly dropped in February, starts to rise until June where it dropped again in October and increases until December. 
  - Has the highest humidity in 2003 and 2016
    * Fluctuates, hits rock bottom in July and peaks in August. 
  - Has the highest wind speed in 2007, 2012, 2014 and lowest in 2018.
    * Fluctuates, with significant drops in April, August, and December. Significant increase in May and July.
* Europe:
  - Has a stable trend overall for temperature, with a major drop in 2002 and a major increase in 2003.
    * Monthly overall trend starts to increase in February and slightly decreases until June and then fluctuates steadily.
  - CO2 emissions over year fluctuates with minor changes in some years and a major drop in 2008.
    * Slightly decreases until April and starts to slighly increases until October.
  - Sea level rise fluctuates steadily with no major changes over the years.
    * Monthly trend also stable with fluctuations.
  - Rainfall fluctuates steadily with no major changes over the years.
    * Monthly trend also stable with minor fluctuations.
  - Experienced a significant increase in 2007 for humidity and significant drop in 2011.
    * Monthly trend shows that there is a slight increase over the months.
  - Has the highest windspeed in 2006, 2009, and 2021. Lowest in 2008.
    * Starts to drop from February to the lowest in July. After that, it starts to increas until December with some minor drops.
* Africa:
  - Experienced lower temperature during 2009-2013.
    * It reached the lowest temperature in April, overall the trend shows fluctuation.
  - Stable changes over the years for C02 Emissions.
    * C02 emissions were the highest in July and starts to decrease until December.
  - Stable changes over the years for Sea level rise.
    * Starts to drop from March-June then slighlt increases until December.
  - Average rainfall over the years is fluctuating.
    * It reached the lowest rainfall in June, overall it shows fluctuating trend.
  - Overall, the trend shows fluctuation for average humidity until 2020 where it reached rock bottome and significantly increases in 2021 then dropped again.
    * Trend shows fluctuation over the months.
  - Stable change over the years for wind speed.
    * Stable fluctuations over the months.
* Asia:
  - Average temperature shows that there is an indication of declining from 2010-2022.
    * Peaks in April and starts to slighly declining until December.
  - Fluctuates a lot over the years for C02 emissions, however no major changes.
    * There is a trend of higher C02 emissions during second half of the year compared to the first half.
  - Stable changes over the years for Sea level rise.
    * Stable changes over the months.
  - Stable changes over the years for rainfall amount.
    * Slightly decreases until July and starts to increase until December.
  - Stable changes over the years for humidity.
    * Stable changes over the months.
  - Stable change over the years for wind speed.
    * Experienced lower wind speed during March-June, overall fluctuates.
* Australia/Oceania:
  - Has significant climate changes notably after 2015.
  - Fluctuates a lot, experienced some significant change in temperature in several years (drop/increase)
    * Overall, stable with minor changes.
  - Has the lowest CO2 emissions in 2005, 2009 and highest in 2018.
    * Higher emissions in May and November.
  - Highest sea level rise in 2007, 2014 and the lowest in 2017.
    * Significantly drops in February and starts to increase where it peaks in May and then experienced some fluctuation until it peaks again in December.
  - Stable fluctuation of rainfall amount until 2013 and starts to drop in 2014 and starts to increase until it peaks in 2019.
    * Declined in February then slighlty increases until June where it peaks.
  - Stable changes of humidity until 2017 where it starts to drop and increases again in 2019.
    * Experienced drop in March and October, overall steady fluctuations.
  - Experienced significant increases of wind speed during 2003, 2006, 2008, and 2013.
    * Significant increase in March (peak) and dropped significantly in April then starts to increase again until December.
* North America:
  - Major drop of average temperature in 2006 and major increase in 2021.
    * Slightly decreases from April until July and peaks in August.
  - Peaks in 2004 and then trend indicates that there is a slight decline afterwards in CO2 emissions.
    * Higher emissions during March-May, July, and November.
  - Sea level rise fluctuates a lot with lowest in 2002, 2008, and 2020, highest in 2003, 2011, and 2013.
    * Highest during March and August.
  - Rainfall amount were the highest in 2002 and 2007, lowest in 2010, 2015, and 2022.
    * Fluctuations over the months.
  - Has the lowest humidity among the continent in 2004 and 2022. Significantly increases during 2004-2006.
    * Stable changes until October where it peaks and then dropped significantly until December.
  - Stable changes of wind speed over the years.
    * Stable changes over the months.
  
