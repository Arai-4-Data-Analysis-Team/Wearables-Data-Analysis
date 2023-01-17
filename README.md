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

This a list of things you'll need to have a copy of the `pipeline` notebook up-and-running on your local machine:

•Python 3.x  
•pandas  
•matplotlib

## Installation

This step by step guide will get you up-and-running on your local machine.

1. Create and activate your virtual environment  
2. Install additional packages and libraries  
3. Open the notebooks in a code editor of your choice running on the virtual environment you just created

## Usage

The actual project was run using the entire dataset provided by the client. Only samples of the dataset are provided here in `data` folder.

## Pipeline

These are the major steps we took in our analysis process:

1. Determined the useful columns / features from the dataset and dropped the unuseful ones  
2. Added a column for the calculated difference between `alpha_r` and `beta_r` values  
3. Created a correlation matrix to determine correlation between features  
4. Created various visualizations using different feature combinations and used the most insightful ones for the client report / presentation  
5. Coordinated with Machine Learning Engineers for visualization of clusters from unsupervised machine learning  

## Deployment

## Contributors

## Timeline

Project Start: `9 January 2023`
Project End: 
