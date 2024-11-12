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

## Exploratory Data Analysis

### Plots and Graphs
- Using **Seaborn**, we can see the number of 50km races is more than **triple** the number of 50 miles races from the **histogram** below. This is understandable because of the big difference in length between the two types of races.
- It is also interesting that the number of male athletes is **higher** than female athletes in 50 miles races while they are **almost the same** in 50km races. 

![image](https://github.com/user-attachments/assets/25fddb05-e3f3-4c2e-8aa5-0529bf316e0b)

- The **distribution plot** below shows that most athletes have **average speed between 6-8km/h**.

![image](https://github.com/user-attachments/assets/3bcae348-4246-4ca8-b840-37aa9690a9f0)

- The **violin plot** shows the **distribution** of athlete average speed by gender in 50km and 50 miles races.
- In the 50km plot, the male athlete distribution plot **slightly shifts upward** compared to female athlete indicating that in **shorter race**, male athletes have higher average speed. However, in **longer races** such as 50 miles, the average speed distribution plots of two genders are **almost identical**.

![image](https://github.com/user-attachments/assets/fe39a501-116d-47c2-8c0b-365f86dfa601)

### Using Groups
- We can take a **closer look** at the **difference in speed** between males and females in these two types of race.
- The difference in mean of athlete average speed between 2 genders is around **0.65km/h** in 50km races while the gap is smaller at **0.42km/h** in 50 miles races.

![image](https://github.com/user-attachments/assets/df9031e2-e9d9-4a5e-9954-bcc60ad95d27)

- **29-year-old athletes** perform the **best** in 50 miles races with the **highest** mean of athlete average speed at **7.9km/h**, taking into consideration the condition that each age must appear more than **20 times**.

![image](https://github.com/user-attachments/assets/be181193-30ec-420b-ad72-8ae19bea5617)

- After creating 2 new columns which are **race_month** and **race_season** from **race_day**, we can **compare** the mean of athlete average speed between each **seasons**.
- We can clearly see the **big difference** in speed in **Summer** compared to other seasons. This is because it is much more difficult to run ultra-marathons in Summer due to the **heat** and **dehydration**.

![image](https://github.com/user-attachments/assets/a3006679-fa7e-46f9-b281-743233c9ec9a)












