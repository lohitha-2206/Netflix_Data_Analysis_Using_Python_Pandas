# 🎬 Netflix Data Analysis using Python Pandas

## 📌 Project Introduction

This project is based on performing data analysis operations on the Netflix Dataset using Python and the Pandas library inside Jupyter Notebook. The dataset contains information related to Netflix Movies and TV Shows such as title, director, cast, country, release year, ratings, duration, and genres.

The main objective of this project is to understand how Python and Pandas are used in real-world streaming platform data analysis for cleaning, filtering, sorting, grouping, and analyzing structured datasets efficiently.

In this project, different data analysis techniques were implemented such as:

- Data Cleaning
- Handling Missing Values
- Removing Duplicate Records
- Filtering Records
- String Operations
- Date-Time Analysis
- GroupBy Operations
- Data Visualization
- Exploratory Data Analysis (EDA)

This project provides practical exposure to working with entertainment datasets and understanding how data analysts use Python for extracting meaningful insights from Movies and TV Shows data.

---

# 📂 Dataset Information

The dataset contains Netflix Movies and TV Shows records available on the streaming platform.

### Dataset Features:

- Show ID
- Category
- Title
- Director
- Cast
- Country
- Release Date
- Release Year
- Rating
- Duration
- Genre/Type
- Description

Each record in the dataset represents a specific Movie or TV Show available on Netflix.

---

# 🛠️ Tools & Technologies Used

## 🐍 Python
Python was used as the programming language for performing data analysis and dataframe operations.

## 📊 Pandas
Pandas library was used for:
- Data Cleaning
- Data Manipulation
- Filtering Data
- Sorting Data
- Date-Time Analysis
- GroupBy Operations

## 📈 Seaborn & Matplotlib
Used for:
- Heatmap Visualization
- Bar Graphs
- Data Visualization

## 📓 Jupyter Notebook
Jupyter Notebook was used to execute Python code interactively and visualize outputs step-by-step.

---

# 🔍 Pandas Functions Implemented

## 🔹 head()
Displays the first 5 rows of the dataset.

### Syntax:
```python
data.head()
```

---

## 🔹 tail()
Displays the last 5 rows of the dataset.

### Syntax:
```python
data.tail()
```

---

## 🔹 shape
Shows the total number of rows and columns.

### Syntax:
```python
data.shape
```

---

## 🔹 size
Displays the total number of elements in the dataset.

### Syntax:
```python
data.size
```

---

## 🔹 columns
Displays all column names.

### Syntax:
```python
data.columns
```

---

## 🔹 dtypes
Displays the datatype of each column.

### Syntax:
```python
data.dtypes
```

---

## 🔹 info()
Displays complete dataset information.

### Syntax:
```python
data.info()
```

---

## 🔹 value_counts()
Displays unique values with their counts.

### Syntax:
```python
data['Category'].value_counts()
```

---

## 🔹 unique()
Displays unique values from a column.

### Syntax:
```python
data['Rating'].unique()
```

---

## 🔹 nunique()
Displays total unique values.

### Syntax:
```python
data['Country'].nunique()
```

---

## 🔹 duplicated()
Checks duplicate records.

### Syntax:
```python
data.duplicated()
```

---

## 🔹 isnull()
Checks null values.

### Syntax:
```python
data.isnull()
```

---

## 🔹 dropna()
Removes rows containing null values.

### Syntax:
```python
data.dropna()
```

---

## 🔹 isin()
Filters records with multiple values.

### Syntax:
```python
data[data['Country'].isin(['India', 'United Kingdom'])]
```

---

## 🔹 str.contains()
Finds records containing specific strings.

### Syntax:
```python
data[data['Cast'].str.contains('Tom Cruise')]
```

---

## 🔹 str.split()
Splits string columns.

### Syntax:
```python
data['Duration'].str.split(' ')
```

---

## 🔹 pd.to_datetime()
Converts date columns into datetime datatype.

### Syntax:
```python
data['Date_N'] = pd.to_datetime(data['Release_Date'].str.strip())
```

---

## 🔹 dt.year.value_counts()
Counts occurrences of years.

### Syntax:
```python
data['Date_N'].dt.year.value_counts()
```

---

## 🔹 groupby()
Groups data based on criteria.

### Syntax:
```python
data.groupby('Category').Category.count()
```

---

## 🔹 sns.countplot()
Displays count plots using Seaborn.

### Syntax:
```python
sns.countplot(data['Category'])
```

---

# 📊 Tasks Performed in the Project

## ✅ Task 1) Removing Duplicate Records

### Task:
Check whether duplicate records are present and remove them.

### Code Used:
```python
data.drop_duplicates()
```

### Explanation:
- Removes duplicate rows
- Improves data quality

---

# 📊 Task 2) Handling Null Values

### Task:
Show null values using Heatmap.

### Code Used:
```python
sns.heatmap(data.isnull())
```

### Explanation:
- Visualizes missing values
- Helps identify incomplete records

---

# 📊 Q1) House of Cards Analysis

### Task:
Find Show ID and Director of "House of Cards".

### Code Used:
```python
data[data['Title'] == 'House of Cards']
```

### Explanation:
- Filters records of the given title
- Displays show details

---

# 📊 Q2) Year-wise Release Analysis

### Task:
Find the year with highest number of Movies & TV Shows released.

### Code Used:
```python
data['Date_N'].dt.year.value_counts()
```

### Explanation:
- Counts yearly releases
- Helps analyze Netflix content trends

---

# 📊 Q3) Movies & TV Shows Count

### Task:
Find total number of Movies and TV Shows.

### Code Used:
```python
data.groupby('Category').Category.count()
```

### Explanation:
- Groups records by category
- Displays category-wise totals

---

# 📊 Q4) Movies Released in 2000

### Task:
Show all movies released in year 2000.

### Code Used:
```python
data[(data['Category'] == 'Movie') & (data['Release_Year'] == 2000)]
```

### Explanation:
- Filters movies released in 2000
- Useful for historical content analysis

---

# 📊 Q5) TV Shows Released in India

### Task:
Show titles of TV Shows released in India.

### Code Used:
```python
data[(data['Category'] == 'TV Show') & (data['Country'] == 'India')]
```

### Explanation:
- Filters Indian TV Shows
- Displays country-specific content

---

# 📊 Q6) Top Directors Analysis

### Task:
Find Top 10 Directors with highest number of Movies & TV Shows.

### Code Used:
```python
data['Director'].value_counts().head(10)
```

### Explanation:
- Counts director appearances
- Displays top content creators

---

# 📊 Q7) Multi-Level Filtering

### Task:
Show records where:
- Category is Movie and Type is Comedies
- or Country is United Kingdom

### Code Used:
```python
data[(data['Category'] == 'Movie') & (data['Listed_In'] == 'Comedies') | (data['Country'] == 'United Kingdom')]
```

### Explanation:
- Uses AND & OR filtering
- Displays targeted records

---

# 📊 Q8) Tom Cruise Movies/Shows

### Task:
Find how many Movies/Shows Tom Cruise was cast in.

### Code Used:
```python
data[data['Cast'].str.contains('Tom Cruise', na=False)]
```

### Explanation:
- Searches actor name in cast column
- Displays related records

---

# 📊 Q9) Netflix Ratings Analysis

### Task:
Find different ratings available on Netflix.

### Code Used:
```python
data['Rating'].unique()
```

### Explanation:
- Displays all unique ratings
- Helps analyze content categories

---

# 📊 Q10) Maximum Duration Analysis

### Task:
Find maximum duration of Movies/Shows.

### Code Used:
```python
data['Minutes'].max()
```

### Explanation:
- Finds longest content duration
- Useful for duration analysis

---

# 📌 Important Insights

✔️ Pandas makes entertainment data analysis simple and efficient.

✔️ Filtering operations help analyze Movies and TV Shows separately.

✔️ String operations help search actors, genres, and titles.

✔️ Date-Time analysis helps identify content release trends.

✔️ Visualization techniques help understand missing values and category distributions.

✔️ Real-world streaming datasets can be analyzed efficiently using Python.

---

# 📁 Project Structure

```text
├── Netflix_Data_Analysis.ipynb
├── Netflix_Dataset.csv
├── README.md
```

---

# 🎯 Final Conclusion

This project demonstrates how Python and Pandas can be used for real-world Netflix data analysis tasks. Different operations such as handling missing values, removing duplicates, filtering records, grouping data, string operations, visualization, and extracting meaningful insights were successfully implemented.

Through this project, practical understanding was gained in:

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Manipulation using Pandas
- String Operations
- Date-Time Analysis
- GroupBy Operations
- Data Visualization
- Python-based Data Analytics

Overall, this project serves as a strong beginner-friendly foundation for learning Data Analysis and Data Science using Python.
