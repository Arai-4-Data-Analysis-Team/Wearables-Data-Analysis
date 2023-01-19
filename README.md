# SpineWise Data Analysis Project

This is a project to analyze data derived from movement sensors / wearables. The wearables measure posture and movement throughout the day and give real time feedback through a vibration signal when damaging habits occur so that workers know when they need to adjust their movement technique.

There are two sensor locations: (1) Neck through the collar and (2) Hip through the belt. 25 measurements are captured per second.

Five groups of data are captured:

A. Acceleration (measured in specific gravity) through an accelerometer  
B. Angular Velocities (measured in degrees per second) through a gyroscope  
C. Magnetic Force (measured in milligauss) through a magnetometer  
D. Kal status: Value that can be converted into columns indicating that a certain action is true or false  
E. Alpha & Beta (measured in degrees): Calculated value indicating two interesting angles for 2D spine movements corrected by the neutral position of the person (which      is measured during calibration)  

## Getting Started

Available labelled data:  
•50 csv files  
•Dedicated scription of activities (some activities are quite unusual like walking and turning very fast)  
•Contains 2 labels in Dutch: 1 generic and 1 specific (e.g. staan bewegend)  

Available unlabelled data (combined from neck & belt sensors):  
•665 datasets in .csv format

## Prerequisites

This a list of things you'll need to have this project up-and-running on your local machine. You can also use the `requirements.txt` file:

•[Python 3.x](https://www.python.org/downloads/)  
•[pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/install.html)  
•[matplotlib](https://matplotlib.org/stable/users/installing/index.html)  
•[seaborn](https://seaborn.pydata.org/installing.html)  

We used [Microsoft Power BI Desktop](https://www.microsoft.com/en-us/download/details.aspx?id=58494) to create the dashboard for the machine learning clusters

## Installation

This step by step guide will get you up-and-running on your local machine.

1. Create and activate your virtual environment. We used [anaconda](https://www.anaconda.com/products/distribution) to create our virtual environment.  
   `conda create -n <yourenvname> python=<x.x> anaconda`  
   `conda activate <yourenvname>`  
   
   ***yourenvname*** is your virtual environment name and ***x.x*** is your python version  
   
2. Install additional packages and libraries.  
   `conda install pip`  
   `pip install -r requirements.txt`  
   
3. Open the notebooks in a code editor of your choice running on the virtual environment you just created.

## Pipeline

These are the major steps we took in our analysis process:

A. Preprocessing
1. Determined the useful columns / features from the dataset and dropped the unuseful ones  
2. Transformed timestamp into `seconds` column where 25 rows = 1 second  
3. Added a column for the calculated difference between `alpha_r` and `beta_r` values  
4. Combined / concatenated all labeled data files into one dataset per folder (calibration & movement)

B. Analysis
1. Created a correlation heatmap to determine correlation between features  
2. Created various visualizations using different features and used the most insightful ones for the client report / presentation (see below)  
3. Coordinated with machine learning engineers for visualization of clusters from unsupervised machine learning via a Power BI dashboard

## Visualizations

Here are the visualizations that we presented to the client:

**Correlation heatmap**

![heatmap](https://github.com/SpineWise-Data-Analysis-Team/SpineWise-Data-Analysis/blob/main/assets/heatmap.png)

**Scatter plot of acceleration X & Y values from neck sensor**

![acceleration](https://github.com/SpineWise-Data-Analysis-Team/SpineWise-Data-Analysis/blob/main/assets/acceleration_x_y_neck.png)

**Scatter plot of angular velocities X & Y values from belt sensor**

![gyroscope](https://github.com/SpineWise-Data-Analysis-Team/SpineWise-Data-Analysis/blob/main/assets/gyroscope_x_y_belt.png)

**Top 5 kal status by label**

![kal status](https://github.com/SpineWise-Data-Analysis-Team/SpineWise-Data-Analysis/blob/main/assets/top_5_kal_status.png)

**Distribution of alpha and beta values from belt sensor**

![violin](https://github.com/SpineWise-Data-Analysis-Team/SpineWise-Data-Analysis/blob/main/assets/violin_alpha_beta.png)

**Difference between alpha and beta values from belt sensor**

![alpha beta](https://github.com/SpineWise-Data-Analysis-Team/SpineWise-Data-Analysis/blob/main/assets/difference_alpha_beta.png)

The following is a screenshot of the Power BI dashboard presented to the client:

![dashboard](https://github.com/SpineWise-Data-Analysis-Team/SpineWise-Data-Analysis/blob/main/assets/dashboard_screenshot.png)

## Contributors

[Shakeel Ahmad](https://github.com/shakilkhan8219)  
[Abdulhamid Albaz](https://github.com/Abdulhamid900)  
[Mattias Olsen](https://github.com/auth-ooh-mate)  
[Marlon Tadeo](https://github.com/m9tadeo)  

## Adviser

[Louis De Viron](https://github.com/devironl)

## Timeline

Project Start: `9 January 2023`  
Project End: `20 January 2023`
