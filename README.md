# My First Data Science Project : Stack Overflow 2017 Survey Analysis
This repository & README includes my first data analysis &amp; visualizations

## Table of contents

- [Analysis](#Analysis)
- [Project](#Project)
- [Motivation](#Motivation)
- [Installation](#Installation)
- [Usage](#usage)
- [Libraries](#libraries)
- [Contributions](#contributions)
- [License](#license)
- [Thanks](#thanks)
- [Project Process (Data Preparation - Modelling - Visualization)](#Projectprocess)

## Analysis
This project analyzes the Stack Overflow 2017 survey data using Python programming language. Below, you can find information about how to use the project and what each code snippet does.

#### Project
This project aims to analyze the demographic information, work habits, and preferences of developers who participated in the Stack Overflow 2017 survey. 
The goal is to extract interesting insights from the survey data and understand the overall trends in the developer community.

#### Motivation
Inspired by the 2017 Stack Overflow survey, our project embarks on a data-driven journey to uncover the intricate interplay between programming languages and job-seeking dynamics across different countries. By delving into the multifaceted landscape of employment and skills, we aspire to provide a comprehensive understanding of how developers' expertise, job-seeking status, and geographic location intersect. This endeavor ignites our passion, as it promises to shed light on the global job market and empower both job seekers and employers with invaluable insights for making informed decisions.

#### Installation
Clone this project to your computer: git clone https://github.com/Caner-Kut/my-data-science-project.git
Install the required Python packages by running the following command: pip install -r requirements.txt
#### Usage
Add the Stack Overflow 2017 survey data to the data folder.
Open the Stack_Overflow_Survey_Analysis.ipynb file with Jupyter Notebook or JupyterLab.
Run the code snippets to perform the analysis.
Check the results folder for the generated visualizations.
#### Libraries
Pandas Link: https://pandas.pydata.org/
Matlotlib Link: https://matplotlib.org/
Numpy Link :https://numpy.org/

```python
# Import libraries
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
```
#### Contributions
This project is open-source and we welcome contributions! If you would like to contribute to the project, please submit a pull request.
#### License
This project is licensed under the MIT License. For more information, please see the LICENSE file.
#### Thanks
[![Udacity](https://cdn.iconscout.com/icon/free/png-256/free-udacity-1-282901.png?f=webp)](https://cdn.iconscout.com/icon/free/png-256/free-udacity-1-282901.png?f=webp)

## Project Process (Data Preparation - Modelling - Visualization)

The tech industry is constantly evolving, and programming languages play a crucial role in its development. In this blog post, we will analyze the usage of programming languages and the job-seeking trends in the tech industry using a dataset from a survey conducted among professionals. By exploring this data, we aim to gain insights into the most popular programming languages and the job-seeking behavior of professional developers.

### We will try to answer this kind of questions in analysis,you will find code in python file.Here is the some sample code related analysis.

```python
# Prepare to data ;
#(only professional developer job seeking by country) 
onlyprof_jobseeking_bycountry = df.dropna(subset=['Professional', 'Country','JobSeekingStatus'], how='any') # Dropping rows with missing values in 'Professional', 'Country', and 'JobSeekingStatus' columns
onlyprof_jobseeking_bycountry # show dataframe
```

```python
#it could be better if we see the 'Professionals in chart'
colors = ['red', 'blue', 'green', 'orange','pink']
(status_professional/df.shape[0]).plot(kind="bar",color=colors);
plt.title("Professional Status");
```

```python
country_counts = actively_status['Country'].value_counts() # Calculate the count of job seekers actively looking for a job in each country.
```

range_by_country=(country_counts[:20]/df.shape[0]) # Calculate the relative frequency of the top 20 countries in the 'country_counts' DataFrame
# by dividing their counts by the total number of records in the original 'df' DataFrame. 

plt.figure(figsize=(12, 6))
(country_counts[:20]/df.shape[0]).plot(kind='bar',color=colors)
plt.xlabel('Country')
plt.ylabel('Proportion')
plt.title('Professional Developer Job Seekers by Country')
plt.xticks(rotation=45)
plt.show()
```

 #### For Medium Blog Post Link is also here  : https://medium.com/@canerkutt/analyzing-stack-overflow-survey-data-unveiling-insights-from-developers-c27a8fd8b71d/ 

You can read the blog related our analysis.

*This README file provides information on how to use the project, installation steps, usage instructions, contributions, and licensing details. You can customize this example to fit your project accordingly.

