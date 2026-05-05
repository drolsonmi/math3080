<head>
<title>Writing Reports</title>
<script>
MathJax = {
  tex: {
    inlineMath: [['$', '$'], ['\\(', '\\)']],
    displayMath: [['$$', '$$'], ['\\[', '\\]']]
  }
};
</script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
</head>

1. Introduction / Abstract (Short)
    - Indicate Business Understanding, purpose and goals of the project, and possibly a summary introducing the results of the model
2. Data Handling
    - A summary of the data provided, including how much data
    - A summary of what needed to be done to make the data usable
        - Missing Data
        - Data Wrangling
            - Encoding
            - Joins
            - Feature Engineering
        - Cross Validation
        - Feature Scaling
    - Can be written or summarized in tables
        - Tables may be good to summarize Encoding and Feature Scaling, for example
    - Include graphs
    - Limitations of the data
3. Data Analysis
    - Graphs
    - Calculations (variance, covariance, correlation, and other calculations needed to analyze data)
4. Model
5. Evaluating
    - Display the evaluation metrics
    - Discussion of whether this metric indicates the model is good or not
6. Conclusion
7. Code
    - Included in a file or as an appendix
    - (Generally not included in professional reports)

## EDA
What is the role of EDA in the project?
- Analysis for cleaning data
- Analysis of data
- Analysis to prepare for the model
- Analysis after model is completed

Include *only* figures relevant to the report


## Tips for good writing
Here are some key tips for writing good reports:

### Clarity
We want the reader to easily and quickly get your point. So, 
- Make clear graphs with proper labels
    - Make sure these graphs effectively demonstrate your point
- Good grammar and spelling
    - Make sure the reading is as clear and straightforward as can be

### Don't write in first-person
Remember that we are telling the story of the data, not the other way around. Our report should reflect what the data says, not what we did.

For example look at this sentence:

> I began by looking at the data. I saw it wasn't clean, so I cleaned it by interpolating values for variables A, C, and D. I did this because ... When I looked at variable E, I couldn't get python to load it

Compare that sentence to this one written from the data's perspective:

> The data had some missing values. A simple interpolation worked for variables A, C, and D because... However, variable E was in an unreadable format. Removing the prefix label and a simple conversion to integer format made variable E usable for this model.

The first example focuses on the author and even on the tools more than the data. The second example, on the other hand, focuses more on the data and what the data needed in order to tell a proper story.

### Conclusion
- Don't write "In Conclusion"

## Writing reports in ipython notebooks
The classic way to write a report is to have the code produce and save images to a folder, then insert those images into a document.

An alternative with python is to write the report in an ipython notebook. To write a report in an ipython notebook, you have a few options:
1. Separate code and report files
    - Write the code (in an ipython notebook or a python file)
    - Save the images to the folder
    - Include the images in the report

2. Include the code in the report
    - At the end of the report (an Appendix), include your code
    - Save figures to a variable
    - Display those saved variables above inline with your text
    - __INCLUDE IPYTHON REPORT TEMPLATE__

Either method of ipython notebooks, you will need to learn Markdown coding
- Headers
- Including images
- Type tables