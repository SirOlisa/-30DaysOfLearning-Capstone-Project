# 30DaysOfLearning-Capstone-Project
---
An analysis of world airplane crashes from (1908-2009)


![cover](https://user-images.githubusercontent.com/107079747/180192568-9347e59c-746f-4147-ad4b-368e47ae3cdf.JPG)
----

# Introduction
 Flight is cool and planes are awesome. The thought of a giant metal hunk weighing anything from a ton to 240(!) tonnes being thousands of feet in the air and gliding majestically through it is very intriguing and exciting for me (especially being a physcicist lol). However, like they say, what goes up must come down and sometimes planes come down -- crashing violently causing vast amount of damage and more importantly, leading to injuries and loss of lives. This analysis seeks to investigate the recorded cases of these incidents within the timeframe above

----
# Data Sourcing
The data was provided by the #30DaysOfLearning organisers [here](https://github.com/theoyinbooke/30Days-of-Learning-Data-Analysis-Using-Power-BI-for-Students/blob/main/Airline%20Project/Airplane_Crashes_and_Fatalities_Since_1908.csv) although it was originally hosted on [Socrata](https://opendata.socrata.com/Government/Airplane-Crashes-and-Fatalities-Since-1908/q2te-8cvq), its no longer available there

----
# The Problems. What are they?
Data analysts are called to make sense of a lot of information in the clearest and most concise way possible. To do this effectively, one needs to have speciic target questions he/she wants to answer. My questions upon inspecting this data were:
1. What is the fatality rate of these crashes?
2. Was there a period where crashes peaked? What was the reason?
3. Who are the most affected ountries?
4. What time of the year does this happen the most?
5. Is there hope for total air safety in the future? 
----
# Data cleaning/Data Validation
Data rarely ever comes in finished form, you have to clean it and this dataset was no exception. Upon inspecting, the given data were

Date: Date of accident
Time: Local time in 24hr
Location: Location of the accident
Operator: Airline/operator of the aircraft
Flight: flight no assigned by the aircraft operator
Route: complete/ partial route flown prior to the accident
Type: aircraft type
Registration: ICAO registration of the aircraft
Cn/in: construction or serial number/ line or fuselage number
Abroad: total abroad(passengers/crew)
Fatalities: Total fatalities abroad (passengers/crew)
Ground: total killed on ground
Summary: brief description of the accident and the cause if known

Since this is a generic project, I decided to get rid of a few columns I felt were redundant including: Registration, Type(they were too few and far between), CN/IN, Route.

Some locations were more specific than others, hence I split the locations column into 2. One containing cities and another containing the country/region.
A hunderd years of data might be too much to assimilate for moat people so I created a new date table in PowerQuery and created a hierarchy showing dates from decades, to years, to months, to dates

This in addition to numerous changing of datatypes, filling of null or empty values, aggregation of similar data, creating new columns, data modelling etc were the transformations done on the dataset 

----
# Data Visualization
 After cleaning, the data was ready for visualization and I managed to create a highly interactive dashboard to summarize most of it 
 
 ![My dashboard](https://user-images.githubusercontent.com/107079747/180208531-3d4c977a-0863-4def-816b-7cadff9b6d96.JPG)
 
 I also created other sheets for more detailed analysis
 ![dash](https://user-images.githubusercontent.com/107079747/180208402-54af70e0-9a55-4211-a55c-e48147aeb69d.JPG)
 
 
 ![dash1](https://user-images.githubusercontent.com/107079747/180208491-cc7c6d3a-ed2b-43a0-b966-0298d1799a00.JPG)

----
# Insights/Conclusion

Visualizations are cool but their primary aim is to help answer problem questions like the ones listed above and straightaway one can begin to point out the answers 
1. Fatality rate is very high (about 68%)
2. The 70's were the peak of airplane casualties/fatalities with Russia being a major factor (due to the cold war and perennial bad weather amongst other things)
3. Russia is the country with (by far) the most fatalities. Looking at the dashboard, it's easy to see why
4. Lots of crashes tend to happen towards the end of the year with August, November, December and January recording high numbers
5. Looking at the drop in fatalities in the 2000's, coupled with the technology boom that has taken place ever since, its easy to see a future where crashes are extremely minimal. There is hope
