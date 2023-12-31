# About the Project
This repository showcases my personal project where I analysed data regarding customer credit card defaults from Taiwan in 2005 using PowerBI, as a means to start my learning with the tool. The data was extracted from ![UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients), however, it was altered prior to use. A new column, 'STATE' was added to the data that randomly assigned a state location in USA to customer. <br> <br>
 
# The Data
![raw_data](https://github.com/CalvinJohn99/Credit_Card_Defaults/assets/40469219/6a17b85c-f135-4411-9493-990499c1cea3) <br> <br>

# Data Preparation
We can see from the above data that it needs to be transformed to make sense. For example, the `SEX`, `MARRIAGE`, and `EDUCATION` columns have certain numbers to indicate certain categories. Also, the top row indicating columns as X1, X2, X3, ..., is deleted as this is not descriptive of the data. Now the new top row shows descriptive information about the columns, and is made to be the column header in PowerBI through data transformation. <br> <br>
To transform the column data (in Power BI data view) for `SEX`, `MARRIAGE`, `EDUCATION` and indicate their respective text categories instead of numbers, we first change the data type from 'Whole Number' to 'Text' via 'Transform' group on the 'Home' tab. <br> <br>
For the column `SEX`, the value 2 indicates female, while 1 indicates male. The 'Replace Values' option in the 'Transform' group was used to replace the 1's and 2's with 'Male' and 'Female. <br><br>
For the column `EDUCATION`, the value 1 indicates graduate, 2 indicates undergraduate, 3 indicates highschool, and all other values are unknown.
For the column `MARRIAGE`, the value 1 indicates married, 2 indicates single, and all other values are unknown.
For these columns, we used the 'Condition Column' option in the 'General' group of the 'Add Column' tab to create new columns `MARITAL STATUS` and `EDUCATION LEVEL` that gave the corresponding categorical text description of the number values in those columns. The original columns were then deleted. <br> <br>

# The Data After Transformation
![cleaned_ _transformed_data](https://github.com/CalvinJohn99/Credit_Card_Defaults/assets/40469219/61c86478-8a20-4cbd-8b3f-09a944f8e866)

This data was then used to form the interactive dashboard shown in the next section. <br> <br>

# The Interactive Dashboard
![dashboard](https://github.com/CalvinJohn99/Credit_Card_Defaults/assets/40469219/c57ea836-7b2b-4bcc-ac4a-89ac8be52570) <br> <br>


# Exploratory Data Analysis & Insights
## 1. Defaulted by Age and Sex 
<br>
The distribution of credit card defaults across the ages seems to be fairly similar for both sexes, however, we find that at ages below 30, females default significantly more than males, at the peak we see that females default 201 times, while males default 112 times at age 27. This could be partially influenced by the fact that we have more females than males as customers. <br> <br>

## 2. Defaulted by Education Level and Sex 
<br>
We see that customer with an undergraduate degree defaults most (defaults: 1922 females, 1408 males) while customers that are at high school level defaults the least (defaults: 692 females, 545 males). We also find that females default more at each education level in comparison to males. <br> <br>

## 3. Defaulted by Marital Status and Sex 
<br>
We see that the distribution of credit card defaults appear very similar whether they are married or single. When married, the sum of defaults is 1856 for females, 1485 for males. When single, the sum of defaults is 1860 for females, 1346 for males. Again, males default their credit cards less than females in both the categories.
 <br> <br>
 
## 4. Defaulted by State
<br>
The map we see in the dashboard is a shape map that is color saturated by the number of defaults in the state. The map shows that Florida (156 defaults), and Idaho (160 defaults) are the most saturated states, meaning they have the most credit card defaults. <br> <br>



## 5. Defaulted Ratio
<br>
We find that 22% of all customers have defaulted their credit cards. <br><br>

## 6. Slicers - Education level & Marital Status
### Marital Status
<br>

![married](https://github.com/CalvinJohn99/Credit_Card_Defaults/assets/40469219/1f0e8172-7a67-4289-9c8a-7486a1d173cc)

We see that married customers default more when at ages closer to 35 (for females) and 38 (for males). We also find that the percentage of credit card defaults increases to 23%. <br><br>

![single](https://github.com/CalvinJohn99/Credit_Card_Defaults/assets/40469219/1b0accbe-2bb6-47da-8e44-cc305e9399f1)

We see that most credit card defaults for customer below ages 30 appear to be coming from single individuals, while single customers above age 30 have very few credit card defaults in comparison. We also fine that the percentage of credit card defaults decreases to 21%.

<br><br>

### Education Level
<br>

![graduate](https://github.com/CalvinJohn99/Credit_Card_Defaults/assets/40469219/658a95c1-36f1-4056-9579-ba574509933c)
We find that customers who have a graduate educatio level default more when they are single, while the percentage of total credit card defaults decreases to 19%, i.e., graduates don't default as much.
<br><br>

![highschool](https://github.com/CalvinJohn99/Credit_Card_Defaults/assets/40469219/f48eb6f4-dc0f-4ef8-9e0f-4a29640e09a0)
We see that the majority of credit card defaults for customers above age 30 comes from customers who have a highschool education level. We also find that marrited customers with this highschool level default more, while the percentage of total credit card defaults increases to 25%, i.e., customers at the highschool level default most.
<br><br>

![undergraduate](https://github.com/CalvinJohn99/Credit_Card_Defaults/assets/40469219/f3035455-f73d-4a74-81ca-4eb0669bd982)
We find that the percentage of total credit card defaults increases to 24%, i.e., customers with an undergraduate education level defaults more.


