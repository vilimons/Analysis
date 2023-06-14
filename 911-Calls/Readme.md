# Objective

In this project we aim to understand the main reasons behind the calls to 911 number, the emergency telephone number. The dataset contains almost 100000 entries from the state of Pennsylvania, U.S.

## For this project we will be analyzing some 911 call data from Kaggle. The data contains the following fields:

lat : String variable, Latitude
lng: String variable, Longitude
desc: String variable, Description of the Emergency Call
zip: String variable, Zipcode
title: String variable, Title
timeStamp: String variable, YYYY-MM-DD HH:MM:SS
twp: String variable, Township
addr: String variable, Address
e: String variable, Dummy variable (always 1)

## Basic Questions

This step will allow us to answer basic questions.<br>
For example: What are the top 5 zipcodes for 911 calls?<br>
#### Answer: 19401 (Norristown), 19464 (Pottstown), 19403 (Eagleville), 19446 (Lansdale) and 19406 (King of Prussia).

Another question is: how many unique title codes are there?<br>
#### Answer: 110 unique title codes.

## Creating new features
In the titles column there are "Reasons/Departments" specified before the title code. <br>
These are EMS (emergency medical service), Fire, and Traffic. We can use .apply() with a custom lambda expression to create a new column called "Reason" that contains this string value.<br>
This new feature will be helpful to help us answer new questions, such as: <br>
What is the most common Reason for a 911 call based off of this new column? <br>
#### Answer: The most common reason is EMS, containing a total of 48877 calls. Is followed by traffic, which contains 35695 calls. Finally, the least reason why people call to 911 is Fire, which contains 14920 calls.

## Problems
The dataset contains interesting columns, such as: Day of Week and Months. In the months column we had some problem. It goes to january to august, but it doesn't have the months september, october and november.
Luckly it has December. We solve this problem counting every instance of the columns by the month. 

## Plots
After this step, we begin to create some interesting plots. This will help us to answer even more questions. The first one is a simple one, indicating the count of the columns per month. <br>
Then we create a plot that counts 911 calls. With this plot, we can notice here there are some significant spikes in February and a little bit in March, and then we get some downturns in May and maybe late August.<br>
Now let's move on to creating heatmaps with seaborn and our data. We'll first need to restructure the dataframe so that the columns become the Hours and the Index becomes the Day of the Week.<br>
The heatmap show us that the calls tend to occurs during daytime. What's interesting is that not too many calls occurs on Sundays and Saturdays.

## Conclusion
With this project we could answer some interesting questions that can give us some insights. For example, we could explore more to see why calls tends to occurs less at weekends.
There are more plots in the project, which you can visualize in this [link](https://github.com/vilimons/Analysis/blob/main/911-Calls/911-Calls.ipynb).

