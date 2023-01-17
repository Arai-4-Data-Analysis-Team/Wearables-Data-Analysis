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
