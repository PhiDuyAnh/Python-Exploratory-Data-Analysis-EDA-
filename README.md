# Python Exploratory Data Analysis (EDA) Project
This project uses a big dataset to do data cleaning and perform Exploratory Data Analysis (EDA) entirely with Python.

## Disclaimer
This project was inspired by a Youtube video made by Ryan & Matt Data Science which you can find [here](https://www.youtube.com/watch?v=4sZFkPw87ng&t=2781s).<br/>
However, please bear in mind that all the codes in the Jupyter Notebook uploaded above and the summary of findings in this README file were written by me!

## Dataset Overview
The dataset contains more than **7M race records** registered between 1798 and 2022. More specifically, it contains **7,461,226 ultra-marathon race records from 1,641,168 unique athletes** in CSV format. The dataset can be downloaded on Kaggle [here](https://www.kaggle.com/datasets/aiaiaidavid/the-big-dataset-of-ultra-marathon-running/data).

![image](https://github.com/user-attachments/assets/df78235e-06f5-4abc-a759-39177b64a296)


### Data Structure & Types
- Using a simple line of code on Python, we can take a peek at the structure of dataset: **7,461,195 rows** and **13 columns**!

![image](https://github.com/user-attachments/assets/63d8af28-aef7-4c49-ac54-9c95a925546b)<br/>


- Regarding the data types, most columns are **object-type** with the exception of: Year of event **(int)**, Event number of finishers **(int)**, Athlete ID **(int)** and Athlete year of birth **(float)**.

![image](https://github.com/user-attachments/assets/36233c1c-3495-47a8-b2bd-70ea40da302a)

## Data Cleaning

### Filtering Data
- Because of the sheer size, time period and scope of the dataset, we are going to filter it down to only showing **50km and 50 miles USA races in 2020**.

![image](https://github.com/user-attachments/assets/9ca0cb7d-fb14-42a7-ae42-8d5884257505)<br/>

- Following this, we remove 'USA' from Event names, remove 'h' from Athlete performance column, create a new column calculating an athlete's age and finally drop some columns. This is what the data frame looks like now:

![image](https://github.com/user-attachments/assets/539f1b70-f3a2-4bd6-9e8f-88a7699a423b)<br/>

### Null & Duplicated Values

- Checking for null and duplicated values are also important parts of the process. Although **no duplicated value** is present, **233 null values** are found in the Athlete age column.

![image](https://github.com/user-attachments/assets/8115b620-70f5-4d54-95b3-d120ed0abf08)

- After dropping all the null values, the dataset now contains **25857 rows and 10 columns**!

![image](https://github.com/user-attachments/assets/9cd3bb1d-50dd-4ea2-a433-a58b1b1369ff)

### Final DataFrame

- Next, we **reset the dataframe index**, **change data types** of some columns, **rename and reorder** all the columns. This is the final result:

![image](https://github.com/user-attachments/assets/f679d405-820a-41ac-8020-9f08db76ebdd)






