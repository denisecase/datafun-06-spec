# Specification for Project 6 EDA Notebook

## Overview

Project 6 is an opportunity to create a compelling data story using
exploratory data analysis (EDA) in a Jupyter Notebook,
focusing on pandas and seaborn skills to analyze data and create visualizations.

## Deliverable Names

- GitHub Repository:  datafun-06-eda
- Documentation:      README.md
- Notebook:           yourname_eda.ipynb

Create a new GitHub repository with a README.md.
Create a new Jupyter Notebook with the specified name.

## Version Control with Git

Use Git for version control.
In your README.md, document the steps of  initializing a new project in GitHub, creating a Jupyter Notebook, and managing notebook versions with Git.

## Objective

Develop a Jupyter Notebook that demonstrates advanced skills in
exploratory data analysis using pandas and seaborn.
The notebook should tell a data story and visually present findings
in a clear and engaging manner.

## Requirements 

### 1. Environment Setup

1. Create and activate a project virtual environment.
1. Install all required packages into your local project virtual environment.
1. After installing the required dependencies, generate a requirements.txt file.
1. Document the process and commands you used in your README.md.
1. Add a .gitignore file to your project with useful entries.

### 2. Project Start

Make sure Jupyter is installed and working in your project virtual environment.
Document the process and commands you used in your README.md.

Then create, open, and start a new notebook:

1. Create the Notebook: In the VS Code Explorer, create a new file e.g., yourname_eda.ipynb. Ensure it has a .ipynb extension.
2. Open the Notebook: Double-click the notebook file to open it in the notebook editor.
3. Add a Markdown cell at the top of your notebook with a title, author, date and the purpose of the project.

### 3. Import Dependencies

Add a Python cell next with the import statements for the libraries you will use in the project.
Organize your project imports following conventions.

### 4. Add Logging

Logging is recommended for all script and notebook projects.
Implement logging to enhance debugging and maintain a record of program execution.

1. Configure logging to write to a file named log.txt.
1. Log the start of the program using logging.info().
1. Log the end of the program using logging.info().
1. Log exceptions using logging.exception().
1. Log other major events using logging.info().
1. Log the start and end of major functions using logging.debug().

### 5.  Data Acquisition

Choose a dataset for analysis.
Due to issues with unreliable data sources,
it is strongly recommended to select from one of the pre-installed datasets in Seaborn.
You can view a list of the datasets at the link below:

- [List of Seaborn Datasets Installed](https://github.com/mwaskom/seaborn-data)

Load one of these datasets into your notebook with the following code.
Change from iris to the dataset name (without the .csv extension).

```python
import seaborn as sns
import pandas as pd

# Load the Iris dataset into DataFrame
df = sns.load_dataset('iris')

# Inspect first rows of the DataFrame
print(df.head())
```

### 6. Basic Data Exploration

First, use pandas to perform the basic data exploration tasks as the initial steps of
any data analysis project:

1. Load Data into DataFrame
2. Inspect Data w/head(), shape, and dtypes
3. Describe Summary Statistics
4. Display Histograms for Numeric Columns

For example:

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load data into DataFrame
df = sns.load_dataset('iris')

# Inspect data with head(), shape, and dtypes
print(df.head(10))
print(df.shape)
print(df.dtypes)

# Describe summary statistics
print(df.describe())

# Display histograms for numeric columns
df.hist(figsize=(10, 8))
plt.show()
```

### 7. Data Transformation

Use pandas and other tools to perform transformations as needed.
Transformation may include renaming columns, adding new columns,
or transforming existing data for more in-depth analysis.
For example:

```python
# Renaming a column
df.rename(columns={'sepal_length': 'Sepal Length'}, inplace=True)

# Adding a new column
df['Sepal Area'] = df['Sepal Length'] * df['sepal_width']
```

### 8. Data Visualization

Create a variety of chart types using seaborn and matplotlib to showcase different aspects of the data.
For example:
  
```python
sns.pairplot(df, hue='species')
plt.show()
```

### 9. Storytelling and Presentation

Interpret the visualizations and statistics to craft a narrative around your findings.
Present your findings in a logical and engaging manner.

## Notebook Design

- Begin your notebook with a project summary including the title, author, date, and project's purpose. This provides an immediate understanding of the notebook's objective.
- Ensure your code and presentation are neat, well-organized, and follow good coding practices. This includes proper variable naming, consistent code style, and logical organization of code cells.
- Use Markdown features effectively for formatting, such as section headings, bullet points, and emphasis (bold/italic), to enhance readability.

## Notebook Structure and Documentation

Once the notebook runs without errors, focus on how the notebook content is structured and documented.
Organize your notebook into well-defined sections, each with a clear purpose and header.
Use Markdown cells to provide context, explain your analysis, and share findings. This makes your notebook informative and engaging.
Comment your code cells to explain the purpose and functionality of the code. This is especially important for complex or non-obvious code segments.

## Notebook Execution

Run your notebook entirely to ensure it executes without errors. This includes checking all code cells and ensuring all data visualizations render as expected.
Confirm that your notebook renders correctly on GitHub after pushing, as this ensures your work is viewable by others.

## Evaluation Criteria

- Functionality: The project should be functional and meet all requirements.
- Documentation: The project should be well-written and well-documented.
- Presentation: The project should be presented in a clear and organized manner.
- Professionalism: The project should be submitted on-time and reflect an original, creative effort.

See rubric for additional information.

## Resources

- See [JUPYTER.md](https://github.com/denisecase/datafun-04-spec/JUPYTER.md) for Jupyter Notebook keyboard shortcuts and recommendations.
- See [MARKDOWN.md](https://github.com/denisecase/datafun-04-spec/MARKDOWN.md) for Markdown syntax and recommendations.
- See [Plotting graph For IRIS Dataset Using Seaborn And Matplotlib](https://www.tutorialspoint.com/plotting-graph-for-iris-dataset-using-seaborn-and-matplotlib)
- See [Seaborn Tutorial](https://seaborn.pydata.org/tutorial.html)

## Explore Datasets

As you approach the end of the program,
you have the opportunity perform EDA on a dataset of your choice as part of your capstone project and report.
We recommended that you start considering potential topics and exploring suitable datasets early in the program.
To help find a suitable dataset that sparks your interest, the following resources offer a range of options:

- [List of Seaborn Datasets Installed](https://github.com/mwaskom/seaborn-data)
- [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php)
- [Kaggle Datasets](https://www.kaggle.com/datasets)
- [Data.gov](https://www.data.gov/)
- [Google Dataset Search](https://datasetsearch.research.google.com/)
