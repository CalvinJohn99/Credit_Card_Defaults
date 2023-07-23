# About the Project
This repository showcases my personal project where I analysed data regarding customer credit card defaults from Taiwan in 2005 using PowerBI, as a means to start my learning with the tool. The data was extracted from UCI Machine Learning Repository, however, it was altered prior to use. A new column, 'STATE' was added to the data that randomly assigned a state location in USA to customer.

# The Data
![raw_data](https://github.com/CalvinJohn99/Credit_Card_Defaults/assets/40469219/6a17b85c-f135-4411-9493-990499c1cea3)

# Data Preparation
We can see from the above data that it needs to be transformed to make sense. For example, the `SEX`, `MARRIAGE`, and `EDUCATION` columns have certain numbers to indicate certain categories. Also, the top row indicating columns as X1, X2, X3, ..., is deleted as this is not descriptive of the data. Now the new top row shows descriptive information about the columns, and is made to be the column header in PowerBI through data transformation. <br> <br>
To transform the column data (in Power BI data view) for `SEX`, `MARRIAGE`, `EDUCATION` and indicate their respective text categories instead of numbers, we first change the data type from 'Whole Number' to 'Text' via 'Transform' group on the 'Home' tab. <br> <br>
For the column `SEX`, the value 2 indicates female, while 1 indicates male. The 'Replace Values' option in the 'Transform' group was used to replace the 1's and 2's with 'Male' and 'Female. <br><br>
For the column `EDUCATION`, the value 1 indicates graduate, 2 indicates undergraduate, 3 indicates highschool, and all other values are unknown.
For the column `MARRIAGE`, the value 1 indicates married, 2 indicates single, and all other values are unknown.
For these columns, we used the 'Condition Column' option in the 'General' group of the 'Add Column' tab to create new columns `MARITAL STATUS` and `EDUCATION LEVEL` that gave the corresponding categorical text description of the number values in those columns. The original columns were then deleted.

# The Data After Transformation
![cleaned_ _transformed_data](https://github.com/CalvinJohn99/Credit_Card_Defaults/assets/40469219/61c86478-8a20-4cbd-8b3f-09a944f8e866)

This data was then used to form the interactive dashboard shown in the next section.

# The Interactive Dashboard
![dashboard](https://github.com/CalvinJohn99/Credit_Card_Defaults/assets/40469219/fb7f272a-cb03-4d6a-be0d-c54e664c4e3d)
