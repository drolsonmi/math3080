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

| Date   | Lecture                       | Reading    |
| :----- | :------                       | :------    |
| Jan 8  | What is Data Science?         |            |
| Jan 10 | Machine Learning Process      |            |
| Jan 12 | Nature of Data                |            |
| Jan 15 | *MLK Jr. Day - No School*     |            |
| Jan 17 | Python Basics                 |            |
| Jan 19 | More Python                   |            |
| Jan 22 | Pandas                        |            |
| Jan 24 | Loading Data from a File      |            |
| Jan 26 | Loading Data from API         |            |
| Jan 29 | Cleaning Data                 |            |
| Jan 31 | Data Wrangling part 1         |            |
| Feb 2  | Data Wrangling part 2         |            |
| Feb 5  | In-class Project              |            |
| Feb 7  | In-class Project              |            |
| Feb 9  | Types of Graphs               |            |
| Feb 12 | Graphing with Matplotlib      |            |
| Feb 14 | Graphing with Seaborn         |            |
| Feb 16 | Graphing with Seaborn         |            |
| Feb 19 | *President's Day - No School* |            |
| Feb 21 |                               |            |
| Feb 23 |                               |            |
| Feb 26 |                               |            |
| Feb 28 |                               |            |
| Mar 1  |                               |            |
| Mar 4  | *Spring Break*                |            |
| Mar 6  | *Spring Break*                |            |
| Mar 8  | *Spring Break*                |            |
| Mar 11 |                               |            |
| Mar 13 |                               |            |
| Mar 15 |                               |            |
| Mar 18 |                               |            |
| Mar 20 |                               |            |
| Mar 22 |                               |            |
| Mar 25 |                               |            |
| Mar 27 |                               |            |
| Mar 19 |                               |            |
| Apr 1  |                               |            |
| Apr 3  |                               |            |
| Apr 5  |                               |            |
| Apr 8  |                               |            |
| Apr 10 |                               |            |
| Apr 12 |                               |            |
| Apr 15 |                               |            |
| Apr 17 |                               |            |
| Apr 19 |                               |            |
| Apr 22 |                               |            |
| Apr 24 | Ethics                        |            |
| Apr 26 |                               |            |
| May 2  | Final Exam opens May 1, 7:00am, due 24 hours after | |

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
