# Manufacturing Target Analysis Application

## Table of Contents
- Description
- Installation
- Usage
- Contribution

### Description
This PyQt6-based application provides a graphical user interface for analyzing manufacturing target data. It allows users to open CSV data files, set specification limits (USL and LSL) for each dataset, and perform analysis on the data.

The application is structured around a main window with tabs for different data sets. Users can input the USL and LSL for each data set, and upon clicking the "Analyze" button, the application will provide insights into the process capability and recommended targets of the manufacturing data and respective parameters.

### Installation
- Clone the repository:
    git clone https://github.com/TitusHefner/Manufacturing-Target_Application.git
- ALTERNATIVELY, copy the code within the "Manufacturing Target Application" file and paste it directly into an IDE of your choice.
- Install the required packages using pip:
    pip install PyQt6 numpy scipy pandas seaborn matplotlib

  ### Usage
  - Run the application in your IDE, or create an executable by using PyInstaller.
  - Steps for exe installation using PyInstaller
      1. pip install pyinstaller  (install PyInstaller.)
      1. cd path/to/the/python/program/directory (navigate to where you saved the .py file of the Manufacturing Target Application.)
      3. pyinstaller --onefile script_name.py (create the executable, make sure to replace "script_name" with the name you saved my application as.)

  - Once the code has been ran in IDE or the executable has been launched, a pop-up window will appear and you will be prompted to input your value1 data. Make sure the formatting is consistent with the code (you can edit the file delimiter option, but the code is designed to work best with .csv files)
  - Click the value1 file selection button, navigate to the file that contains value1, and load the file.
  - Enter in your upper and lower specification limits.
  - Repeat the process for your value2.
  - Click "Run Analysis". This will launch 4 matplotlib windows for each value, for a total of 8 windows. These windows show the process capability, a normality test and other dataset descriptors, the cp gauge graph, and the IMR chart.
 
  - ### Additional Notes
    - The normal UCL and LCL calculations according to Six-Sigma doctrine use 3 * std, whereas in my program, the UCL and LCL (Upper and Lower targets, respectively) are calculated using 2 * sigma. This multiple can be adjusted for each value by navigating to the calculate_target_parameters method for each manufacuring target class and editing the multiple of the standard deviation there.
    - Your data column for analysis must be labeled as "value1" and "value2" respectively, or the program will not recognize your data.
 
  - ### Contributing
    Contributions are welcome! If you find a bug or have suggestions for improvements, please feel free to create an issue or submit a pull request.
      
