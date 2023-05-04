# Cyclistic
## Google Data Analytics Professional Certificate - Case Study


You are a junior data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, 
your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives
must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations.

We will use Ask, Prepare, Process, Analyze, Share, Act phases to answer the questions and implement the data analysis steps that I learned throughout the eight courses.


## Ask
### Business Task
In cyclistic company the director and the marketing team believes that the success of the company depends so much on converting the casual bike riders to annaul membership riders. In this case study we need to analyze the key differences between the casual riders and the annual membership riders. After recognizing the differences in needs between both types of customer, the marketing team can develop a strategy that would be alluring for the casual riders to convert to annual membership. We have many stakeholders with different perspectives and we are supposed to understand their needs to give an effective helpful analysis. Lily Moreno is the director of marketing who had the idea of increasing the annual memeberships so an obvious answer for the key differences between each users is beneficial for her. The marketing team collected the data which we are going to implement in the analysis for gaining useful insights. Finally the executive team who are very details oriented and they are who will decide whether to implement the recommended marketing strategy or not.


## Prepare
### Data Description
All the data is stored in the cloud and it is updated quarterly in CSV format. Every quarter is separate so, we have to combine all quarters in one dataframe to make the analysis possible for the last 12 months. The data was downloaded and organized in a folder at local computer to make it accessible for using in the data analysis tool which is decided to be Rstudio. Also, we need to clean the data and make it more ready for the analysis in RStudio after combining in one dataframe by making changes for inappropriate data types, removing iterated data, changing column names to be identical and sorting it out.


## Process
### Documentation of Data Cleaning and Manipulation
#### In this step I combined the data from the different files into one dataframe to make it easier for the next step of analysis. I dropped null values, checked on all columns before combining the data together so I needed the following: 
* Convert ride_id and rideable_type to character so that they can stack correctly.
* Remove lat, long, birthyear, and gender fields as this data was dropped beginning in 2020.


## Analyze
### Aggregating Data
Data is combined into one big data frame to simplify the analysis process then we needed to inspect the data for futher organization before analysis
### Organizing and Formatting Data
#### After combinig all the data into one big data frame, It is obvious that there are some data needs to be fixed as following:
* In the "member_casual" column, there are two names for members ("member" and "Subscriber") and two names for casual riders ("Customer" and "casual"). We will need to consolidate that from four to two labels.
* The data can only be aggregated at the ride-level, which is too granular. We will want to add some additional columns of data -- such as day, month, year -- that provide additional opportunities to aggregate the data.
* We will want to add a calculated field for length of ride since the 2020Q1 data did not have the "tripduration" column. We will add "ride_length" to the entire dataframe for consistency.
* There are some rides where tripduration shows up as negative, including several hundred rides where Divvy took bikes out of circulation for Quality Control reasons. We will want to delete these rides.
* Add columns that list the date, month, day, and year of each ride because this will allow us to aggregate ride data for each month, day, or year ... before completing these operations we could only aggregate at the ride level.
* Add a "ride_length" calculation to all_trips (in seconds)
* Remove "bad" data as the dataframe includes a few hundred entries when bikes were taken out of docks and checked for quality by Divvy or ride_length was negative.
### Conducting Descriptive Analysis
Firstly, we need to perform our analysis on ride_length (all figures in seconds). Statistics like the average, median, max and minimum ride length would give us a glimpse of the meaning of our data. To answer the question of Moreno, we need to compare members and casual users in average ride time & number by each day. The data analysis findings are interesting and suggests that the casual riders use the bikes more in time while the member are more in the number of rides.


## Share
After Conducting our analysis We have found that the casual user tend to use bikes longer than members while the members tend to use the bikes more in terms of number of times specially during the working days not on the weekends. We exported the data anlysis summary for further analysis and created a visualization of the date would be more effective to convey our message to the stakeholders so, two graphs are created to include in our presentation as following:
* The first graph illustrate the average number of rides against the days of week.
* The second graph illustrates the average duration of rides against the day of the week. 


## Act
Top 3 Recommendations:
* Target casual users who have higher number of rides to convert them to a suitable membership plan.
* Target casual users who use bikes on working days more often.
* Target casual users with low average duration of rides and higher average number of rides would be interested in a membership.
