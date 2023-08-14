# Change Point Detection and Segment Analysis
This repository contains Python code that demonstrates the process of reading multiple CSV files from a folder, combining them into a single DataFrame, detecting changepoints within the data, and performing segment analysis with upper and lower target values. The code utilizes libraries such as Pandas, Ruptures, and Matplotlib.
## Contents
- Introduction
- Prerequisites
- Usage
- Functions
- Graphs
- Results
## Introduction
The code demonstrates a practical example of performing changepoint detection and segment analysis on a dataset of diameter measurements. It aims to identify shifts or changes in the data distribution and subsequently analyze each segment based on predefined upper and lower target values.
## Prerequisites
Before running the code, ensure you have the following libraries installed:
- pandas
- os
- ruptures
- matplotlib
You can install them using the following command in your console:
  pip  install pandas os ruptures matplotlib
## Usage
1. Set the folder_path variable to the path of the folder containing your CSV files.
2. Modify the delimiter used in pd.read_csv() according to your CSV file's format.
3. Define the changepoint detection model (e.g., 'l1') and the penalty parameter (pen).
4. Define the upper specification limit (usl), lower specification limit (lsl), and the standard deviation multiplier (n).
Run the script, and it will perform changepoint detection, segment the data, and display graphs illustrating the process.
## Functions
### 'read_csv_files_from_folder(folder_path)'
  This function reads multiple CSV files from a specified folder, creates DataFrames for each file using Pandas, and returns a list of these DataFrames.
### 'fit_pelt(data, model, jump, pen)'
  Applies the PELT (Pruned Exact Linear Time) changepoint detection algorithm to input data and returns the detected changepoints.
### 'calculate_targets(chunk_df, usl, lsl, n)'
  Calculates upper and lower target values for a segment based on data chunk statistics, limits, and a specified standard deviation multiplier.
## Graphs
The code generates various graphs to illustrate the process:
- A graph displaying the original data points with vertical lines indicating detected changepoints.
- A series of graphs displaying each segmented segment's data.
- A series of graphs displaying each segment's analysis, including upper and lower target values, nominal value, and specification limits.
### Results
The code calculates the weighted average upper and lower target values across all segments and computes the tolerance range.
NOTE: Please ensure that you have adjusted the variable names and values according to your dataset and analysis requirements. You will have to edit the values within an IDE of your choice.
Feel free to use, modify, and extend this code for your specific needs. If you have any questions or suggestions, please don't hesitate to reach out.
