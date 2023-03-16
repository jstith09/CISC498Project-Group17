# Calcium Signal
***Calcium Signal*** is a plugin for ImageJ that allows you to detect and analyze calcium cells.

## Install
The target platform for this project is Windows 10. We have made it available for MacOS and Linux as well, but extra steps may have to be performed to get things working.
1. If necessary, download [Python 3](https://www.python.org/downloads/) for your system. Python 3.9.7 or newer is ideal. Ensure that Python has been added to PATH (there should be an option to do this during the installation process). The plugin will make use of the "python" and "python3" commands on your system.
2. If you are a Windows user, please install [Microsoft Visual C++](https://visualstudio.microsoft.com/visual-cpp-build-tools/) 14.0 or higher (if you don't already have it on your system). Choose Desktop Environment with C++. You may be required to restart the computer after this step.
3. If you are a Linux or MacOS user, ensure that pip is installed as your package manager for Python. You may also have to run `sudo apt-get install python3-tk` or `sudo apt-get install python-tk` before running the installation script (on a Mac, those commands are `brew install python-tk` or `brew install python3-tk`).
4. Download the zip file, unzip it inside the *Fiji.app* directory, and run "CalciumSignal Installer.py" from inside the unzipped folder. The script will create the *CalciumSignal* folder within the *plugins* folder. This is where the files used by the program will go.

***NOTE: if you experience problems during the Peak Analysis phase of the project, type the following in a command prompt to downgrade the Matplotlib version, which may fix the problem after restarting the plugin:
`pip install matplotlib==3.4.3`
Otherwise, upgrade your Python installation.***

## Startup
### PoorMan3DReg
<img src="https://github.com/jstith09/calcium/blob/main/poorman.jpg" width="200" height="150">

  - ***Transformation:*** Rigid Body (Default)
    - Translation, Scaled Rotation, Affine
  - ***Z Slices:*** 600 (Default) select number of slices (images) you would like from video
  - ***Projection Type:*** Average Intensity (Default)
    - Max Intensity, Sum Slices
 
### Cell Detector
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/celldetector.jpg" width="200" height="200">

  - ***Threshold:*** Automatically will set to a number. Adjust so that the red is covering the most green that you would like detected in the image window
  - ***Slice:*** Set to 1 (Default)
  - ***Size Filter:*** Min: 10 Max: 262144 (Default)
    - Min and Max size of circles drawn. Can be left as is.
  - ***Exclude objects on edges:*** Checked (Default)

## Windows

### Image Window
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/calciumwindow.jpg" width="200" height="200">

***DISPLAYS WINDOW WITH THE IMAGE YOU OPENED***
  - Detected cells are circled in yellow (ROI)
  - Select the ROI by clicking on them
  - Selected ROI will appear in Roi Manager where you are able to add/delete/rename them

### Menu
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/celldetector.jpg" width="200" height="200">

***NEED TO IMPLEMENT/UPDATE PICTURE***

### Custom Roi Manager
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/customroimanager.jpg">

  - ***Min/Max Cell Diameter:*** Enter values to change what size cells are circled by ROI
  - ***Update Cells:*** Use to update ROI after selecting RC 1/2/3 STD
  - ***Multi Measure:*** ............
  - ***Outlier Analysis:*** Displays an outlier analysis chart
  - ***RC 1/2/3 STD:*** Automatically enters 3 different standard deviations for min/max diameter values
  - ***Grid Suggestions:*** Gives suggested values for 'Create Grid'
  - ***Create Grid:*** Enter values from 'Grid Suggestions' to create grid on image
  - ***Undo [Cntrl + Shift + E]:*** Undo Add/Delete of ROI

### Results Table
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/resultstable.jpg" width="350" height="150">

### ROI Manager
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/roimanager.jpg" width="150" height="200">

  - ***Add:***
  - ***Update:***
  - ***Delete:***
  - ***Rename:***
  - ***Measure:***
  - ***Deselect:***
  - ***Properties:***
  - ***Flatten:***
  - ***More>>:***

## Credits

***Matt Searfass, CJ Spagnolia, Nick Costley, Luke Halko, Jaden Stith ..........***


