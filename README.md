# Bike-Sharing-Case-Study
Understood how casual riders and annual members use Cyclistic bikes differently. From these insights,  and designed a new marketing strategy to convert casual riders into annual members.


# Section 1- ASK
What is the problem you are trying to solve?


Business Objective: To maximize the number of annual memberships by converting casual riders to annual members.

How can your insights drive buisness decisions?


The effort to find out trends on how the usage of cycles for annual members differ from the casual riders with the help of visualizations and key findings that will help to make recommendations that can be considered by the company in order to increase the annual memberships.

# Section 2: PREPARE
The dataset required for this business objective should be of the past 12 months. Here, we are considering data from July 2020 till June 2021.

The data was made available by Motivate International Inc. under the appropriate license which ensures credibility of the data. This is public data that you can use to explore how different customer types are using Cyclistic bikes.

The data file consisted of different folders for each month of a particular year and also quarterly data year wise was made available.

As we had to consider only the data related to the past 12 months, I downloaded the csv files as per the requirement and stored it in a single folder so they are easier to access and work on.

The data-privacy issues prohibit you from using riders’ personally identifiable information. This means that we won’t be able to connect pass purchases to credit card numbers to determine if casual riders live in the Cyclistic service area or if they have purchased multiple single passes. This ensures data integrity.

# Section 3: PROCESS


I am using Python language for working on data as it is more accessible and easier to use.

The first step while starting any analysis is to import appropriate libraries in the notebook.

Some of the important libraries are:

1) Pandas - Pandas allows importing data from various file formats such as comma-separated values (CSV), JSON, SQL, Excel. Pandas allows various data manipulation operations such as merging, reshaping, selecting, as well as data cleaning, and data wrangling features.
2) Numpy - It can be used to perform a number of mathematical operations like trigonometric, statistical, and algebraic on arrays.
3) Matplotlib and Seaborn - It is used to create graphical analysis of the data.
4) Datetime - These classes provide a number of functions to deal with dates, times and time intervals.

![image](https://user-images.githubusercontent.com/77182591/197330237-a18971e8-861d-42d2-bc33-774f217da72d.png)
Then, the data files are imported in the notebook. As we are working on the dataset of the past 12 months, we have one csv file per month. Therefore we have to import 12 files, convert them into a dataframe and merge them together in a single dataframe using Pandas.
![image](https://user-images.githubusercontent.com/77182591/197330403-9ff1d428-e0bb-4a77-a08e-5263f807bacc.png)

Merged all the data into a single dataset.Then read the dataframe in the Jupyter notebook to understand the data. 
![image](https://user-images.githubusercontent.com/77182591/197330471-36234810-753e-4ecb-9845-e3d7b7d55c0b.png)
We check the data type of all the columns present in the dataframe and convert the data type of columns as per our requirement.

For eg: We can convert the Object data type to Datetime.

Also, we have to add new columns in the dataframe.

For example:

-In order to find the ride length between start and end location, we subtract the values in those columns and create a new column to store values.
![image](https://user-images.githubusercontent.com/77182591/197330549-bb81d458-4bc7-4eaa-9281-5e468af57130.png)
-Create a new column week_day in order to determine the day of the week(Sunday, Monday,...) of the date present in another column.

Also, we convert the values obtained, into weekday values with the help of a python dictionary.
![image](https://user-images.githubusercontent.com/77182591/197330575-379b2edb-07a4-4c7f-bb56-8ae08ed12f29.png)

Note - The next step is to clean the columns, I have listed out the whole cleaning process in detail below. Please check out that section.

-Create a new column for calculating distance between start and end points with the help of Euclidean distance formula.


The most important step of the data cleaning process is to determine all the rows and columns with missing values.

The next step is to check how we can populate the missing cells. But if the percentage of missing data is less than 3%, we can drop them without any major feedback crunch in our analysis.

In this dataset, as the number of rows having missing values was just 0.1% of the total dataset, I dropped all those rows.

If you have a large number of rows with missing values, you can fill in those values by substituting the cells based on exploratory analysis.


![image](https://user-images.githubusercontent.com/77182591/197330627-2d8738ea-84ee-4d06-a33d-0c49c13e4867.png)

# Section 4: Analysis

After cleaning the data, it is important to aggregate, organize and format the data. Here we need to perform calculations(descriptive analysis) and understand the trends present in the data. Following are the analysis I did and the outcomes I observed:

-Calculated the mean ride length of all types of users, annual members and casual riders.

---> Observed that the mean ride length of casual riders was the highest.

![image](https://user-images.githubusercontent.com/77182591/197330698-9a41abf4-97ef-4bb0-b339-5b4a6cb123f5.png)

-Calculated the mode of weekday for all types of users, annual members and casual riders.

---> Observed that the mode weekday for casual riders is “Friday” whereas for annual members it is “Monday”.
![image](https://user-images.githubusercontent.com/77182591/197330813-c74bb2d7-e290-4b11-9494-43e55fbbe237.png)


-Calculate the average ride length for casual riders by weekday.

---> The highest average ride length for casual riders is observed on Saturday which is approximately 47 minutes.

![image](https://user-images.githubusercontent.com/77182591/197330803-100e9675-719b-4c30-b764-99beaa14ce86.png)
![image](https://user-images.githubusercontent.com/77182591/197330832-28a99c09-7204-43b0-8813-11bc5160a654.png)
![image](https://user-images.githubusercontent.com/77182591/197330850-65ba9b37-f78d-4cb2-ab38-e63b12013e84.png)

# Section 5: SHARE
We use python libraries like seaborn and matplotlib to plot visualizations.

Through visualizations, we can observe that the number of casual riders is approximately equal to the number of annual members. The 59.6% of total population are annual membership holders.
![image](https://user-images.githubusercontent.com/77182591/197330894-a68095e9-c94f-49ae-8454-d41b2ea04341.png)
![image](https://user-images.githubusercontent.com/77182591/197330902-126de4b9-7987-4cb4-bca7-f65f9700a0ef.png)

It has been observed that number of casual riders has been increased over the year.
![image](https://user-images.githubusercontent.com/77182591/197330945-928d7c3b-cb68-48dc-b04e-5156984c8d43.png)
The count of people using the services starts dropping from the month of August. 
![image](https://user-images.githubusercontent.com/77182591/197330993-0daca388-5daa-430c-af83-7c66eb950b01.png)
![image](https://user-images.githubusercontent.com/77182591/197330999-6cba163f-0558-448d-9f4f-86dbe0b9c88b.png)

# Section 6: ACT
1) As observed from the analyses, the number of casual riders is more than the number of annual membership holders. We can increase the fare of casual rides (which will help generate more revenue initially) and at the same time, reduce the cost of annual membership. This will pull more riders towards annual membership.

2) As observed, most of the casual riders ride on Fridays. We can hold special weekend discounts on annual membership to attract the customers. At the same time, we can offer a guarantee of bikes being available to annual membership holders on weekends, but the same can’t be guaranteed to casual riders.

3) As we noticed from the graph, on average, casual riders ride for approximately 47 mins. We can have a scheme like “more discounts on more miles” where the riders can get discounts like 10% on 10 more mins of ride, 20% on 20 more mins and so on. These discounts will be used against purchase of annual membership.

4) We can also smoothen the process of acquiring annual membership by making the whole process simple and completing it online too. On the other hand, casual riders should come to bike centers to get their bikes. This might pull some people towards annual membership, but in the long run, this will hurt the company’s image. So we should try not to fall for this dark/anti-pattern.

5) We have observed that approximately more than half of the casual members use Docker bikes for travelling, so we can offer special incentives in order to increase conversion from casual to annual.
