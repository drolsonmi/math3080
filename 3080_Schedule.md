# Math 3080 Course Schedule - Spring 2024
These are the topics that we plan to cover this semester:
* What is Data Science?
  * The Nature of Data
* Basic Python
* Obtaining and Loading Data
  * Web Scraping
  * Regular Expressions
* Graphing Data
* Cleaning Data
* Statistics
  * Bayes Rule
* Intro to Machine Learning
  * Linear Regression
  * Logistic Regression
* Ethics in Data Science

This class has a prerequisite of MATH 2040 or MATH 3040. You are expected to be able to recall/restudy the topics from that class as needed. We will use these principles often, but may not review the material beforehand. If it is needed, we will do a little review in class, but most of the time, you will be responsible to review topics as needed.

Following is my planned schedule for the course. It is incomplete at this point, but will be changed as the semester progresses. The textbooks and videos are found on the [Textbooks](https://github.com/drolsonmi/math3080/blob/main/3080_Textbooks.md) page.

|  Day  | Date   | Lecture                                   | Reading                 |
| :---: | :----- | :------                                   | :-------------------    |
|       |        | __*----- Data Science Overview -----*__   |                         |
|   1   | Jan 8  | What is Data Science?                     |                         |
|   2   | Jan 10 | Machine Learning Process                  |                         |
|   3   | Jan 12 | Nature of Data                            |                         |
|       | Jan 15 | *MLK Jr. Day - No School*                 |                         |
|       |        | __*----- Python Basics -----*__           |                         |
|   4   | Jan 17 | Python Basics                             | McKinney, Chapters 2-4  |
|   5   | Jan 19 | More Python                               | McKinney, Chapters 2-4  |
|   6   | Jan 22 | Pandas                                    | McKinney, Chapter 5     |
|       |        | __*----- Loading Data -----*__            |                         |
|   7   | Jan 24 | Loading Data from a File                  | McKinney, Chapter 6     |
|   8   | Jan 26 | Loading Data from API                     | McKinney, Chapter 6     |
|       |        | __*----- Data Wrangling -----*__          |                         | 
|   9   | Jan 29 | Cleaning Data                             | McKinney, Chapter 7     |
|  10   | Jan 31 | Data Wrangling part 1                     | McKinney, Chapter 8     |
|       | Feb 2  | *Cancelled Class*                         |                         |
|  11   | Feb 5  | Data Wrangling - Joins                    | McKinney, Chapter 8, 10 |
|  12   | Feb 7  | In-class Project: Data Wrangling          |                         |
|       |        | __*----- Graphing -----*__                |                         |
|  13   | Feb 12 | Types of Graphs / Continue Project        |                         |
|       | Feb 14 | *Cancelled Class*                         |                         |
|  14   | Feb 16 | Graphing                                  |                         |
|       | Feb 19 | *President's Day - No School*             |                         |
|  15   | Feb 21 | Exploratory Data Analysis                 |                         |
|  16   | Feb 23 | Interactive Graphs                        |                         |
|  17   | Feb 26 | In-class Project: Stocks & Graphing       |                         |
|  18   | Feb 28 | Scaling                                   |                         |
|  19   | Mar 1  | In-class Project: Stocks & Graphing       |                         |
|       | Mar 4  | *Spring Break*                            |                         |
|       | Mar 6  | *Spring Break*                            |                         |
|       | Mar 8  | *Spring Break*                            |                         |
|  20   | Mar 11 | Ethics - Poor Graphs                      | Irizarry, Chapter 9     |
|  21   | Mar 13 | More work on project                      |                         |
|  22   | Mar 15 | Midterm Review                            |                         |
|  23   | Mar 18 | Midterm Review                            |                         |
|  24   | Mar 20 | __Midterm__                               |                         |
|       |        | __*----- Statistics -----*__              |                         |
|  25   | Mar 22 | Intro to Machine Learning                 |                         |
|  26   | Mar 25 | The ML Process / Cross Validation         |                         |
|  27   | Mar 27 | Classification Evaluation Measures        |                         |
|  28   | Mar 29 | Regression Evaluation Measures            |                         |
|       |        | __*----- Linear Regression -----*__       |                         |
|  29   | Apr 1  | Variance, Covariance, Correlation         |                         |
|  30   | Apr 3  | Linear Regression                         |                         |
|  31   | Apr 5  | Linear Regression Project                 |                         |
|       |        | __*----- Bayes' Theorem -----*__          |                         |
|  32   | Apr 8  | Bayes' Theorem                            |                         |
|  33   | Apr 10 | Naive Bayes Model                         |                         |
|  34   | Apr 12 | Naive Bayes Project                       |                         |
|       |        | __*----- Logistic Regression -----*__     |                         |
|  35   | Apr 15 | Logistic Regression                       |                         |
|  36   | Apr 17 | Logistic Regression Model                 |                         |
|  37   | Apr 19 | Logistic Regression Project               |                         |
|  38   | Apr 22 |                                           |                         |
|  39   | Apr 24 | Ethics                                    |                         |
|  40   | Apr 26 |                                           |                         |
|       | May 2  | __Final Exam__ opens May 1, 7:00am, due 24 hours after |            |

-----
# Lectures
## Day 1: What is Data Science?
* Pi-model

## Day 2: Machine Learning Process
* Demonstrate __3480_00a_Demo.ipynb__
* If there's time, also do __3480_00a_Demo2.ipynb__

## Day 3: Nature of Data

## Day 4: Python Basics
* Why Python?
* Introduce the Jupyter Notebook on Google CoLab
    * Simple Python Calculations
    * Formatting output in Python
    * Markdown cells
* Getting help on functions: `pd.read_csv?`
    * In most IDEs (Google CoLab, VSCode, Jupyter Notebook), type the function and a pop-up window appears showing possible arguments and examples of how the function is used
    * Adding ?? after the function will provide a description of the function and its arguments
* Lists, Tuples, Dictionaries, Arrays, Matrices
    * Lists: a compilation of data (data types can be mixed)
    * Tuple: like a list but restricts the manipulation of data it contains
    * Dictionary: adds labels to the data
        * multiple observations can be entered into the dictionary as lists
        * Preview: we'll use dictionaries to create DataFrames
    * Array: like a list but taylored to make calculations easier and more powerful
        * All elements in the array must have the same data type
        * Calculations like mean `arr.mean()`, sum `arr.sum()`, standard deviation `arr.std(ddof=0), arr.std(ddof=1)`
    * Matrix: a 2-D array
* Strings
    * Splitting a string

## Day 5: More Python
* Virtual Environments
* installing packages through pip
* Array of Random numbers
* If Statements
* For Loops
* Functions
    * Doctrings
    * Loading ftns from a file
* Basic statistical calculations

## Day 6: Pandas
* Series
* DataFrames

## Day 7: Load Data from a File
Using Pandas to load from
* a file on the computer
* a file on the internet
* Web Scraping: extracting files from a webpage or xml file

## Day 8: Load Data from an API

## Day 9: Cleaning Data
* Handling missing data

## Day 10: 

## Day 11: 

## Day 12: Class Project 1
Quick review
* Loading Data
    * from file
    * from API
* Missing Values
    * Remove
    * Fill (ffill, bfill, interpolate, specific value)
* Formatting
    * Datetime
* Data Wrangling
    * Mapping
    * Splitting strings
    * One-hot encoding
    * Ordinal encoding
    * Concatenating / Joins
    * Aggregation
    * Pivot Tables
    * Melting
    * Groupbys

Work on [Group Project 1](https://github.com/drolsonmi/math3080/blob/main/Assignments/3080_GroupProject01.ipynb)

## Day 13: 

## Day 14: Graphing
* Matplotlib Basics
    * Graphing with Matplotlib
    * Graphing with Seaborn
        * Basics (commands, data=, x=, y=)
        * Separating graphs (hue=)

## Day 15: Exploratory Data Analysis
* What is EDA?
* What is involved in EDA?
    * .describe() and .info()
    * Statistics in Python
    * Graphing
* Multi-graphs in Seaborn
    * PairGrids
    * JointGrids

## Day 16: 

## Day 17: Class Project - Stocks
Today, we are going to use stocks in a class project. Topics we'll deal with in this project
* API's
  * Dictionaries and .json
* Datetime Formats
* Scaling
* Graphing

Goal for today:
* Get the stock data loaded from API
  * Specifically, we'll be working with the `4. close` stock values
* Convert data into correct formats
  * Try doing a `sns.lineplot()` with the data to see if it's in the right format

Let the students work until 9:15. Then summarize where everyone should be
* Load API
* Graph data (looks horrible)
* Formatting
  * Convert index to datetime
  * Convert `4. close` to float
* Graph again

## Day 18: Scaling
Load `AMZN` and `T` stocks and plot - very different

Teach about scaling
* Standardization
* Normalization

Do with `AMZN` and `T` data

Give students questions to answer from the data

## Day 19: Finish Stocks Project

## Day 20: Ethics in Graphing

## Day 21: Midterm Review
1. Python
    * a
2. Loading Data
    * a
3. Data Wrangling
    * a
4. Graphing
    * a

## Day 24: Midterm

## Day 25: Intro to Machine Learning
* 