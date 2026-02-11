One of the goals of this class is to help you earn a Data Analysis certificate. To earn this certificate, you must demonstrate that you understand the principles and can use programming to create and analyze data. Because of this, projects and exams in this class will be geared toward that certificate.

To demonstrate your understanding of Data Analysis principles, you will have 2 projects and 2 exams:

## Midterm Project
The project will be your opportunity to demonstrate your ability to load, wrangle, and analyze data.
* Loading data
* Missing data
* Encoding data
* Statistics
* Graphing
* Analyzing data

The project will be presented to you as a request from an employer. Your submission will be a report that thoroughly investigates the employer's questions. You will be expected to write a full report with good writing techniques. Use code to produce figures, inserting only the relevant figures into your report. For your submission, you will be required to give me:
* Your code
    * Any necessary documentation
* Your report
    * 5-7 pages
    * Figures cannot take up more than 1/4 of the page (that's a maximum - if figures can be smaller than that, they should be)

You may submit your report as a PDF, a Markdown file, or as a Jupyter Notebook. 
* If you use a Jupyter Notebook, you can use the first part of the notebook as your report with all supporting code at the end as an Appendix to your report. There is a way to create figures in the code, save them to a variable in memory, then display them earlier in the report.
    * Put this code in an upper cell within the report
        ```python
        # Figure 1: Relationship between petal length and petal width
        display(figure1)
        ```
    * Adapt this code and run it with your calculations in the Appendix at the bottom of your notebook. RUN THIS BEFORE YOU RUN THE PREVIOUS CODE.
        ```python
        # Creating Figure 1: Relationship between petal length and petal width
        import seaborn as sns
        import matplotlib.pyplot as plt
        iris = sns.load_dataset('iris')

        figure1 = plt.figure(figsize=(7,5))
        sns.scatterplot(data=iris, x='petal_length', y='petal_width', hue='species')
        ```

## Midterm Exam
The exam will cover concepts discussed in class
* The Nature of Data
* What is Data Science?
* What is a Data Scientist?
* What is CRISP-DM?
* Ethics
    * Ethics of Graphing

## Final Project
* Basic Machine Learning
    * Linear Regression
    * Logistic Regression

## Final Exam
* Ethics
    * Responsible AI