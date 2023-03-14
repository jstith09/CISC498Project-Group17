# Calcium Signal
***Calcium Signal*** is a plugin for ImageJ that allows you to detect and analyze calcium cells.

## Install
The target platform for this project is Windows 10. We have made it available for MacOS and Linux as well, but extra steps may have to be performed to get things working.
1. If necessary, download [Python 3](https://www.python.org/downloads/) for your system. Python 3.9.7 or newer is ideal. Ensure that Python has been added to PATH (there should be an option to do this during the installation process). The plugin will make use of the "python" and "python3" commands on your system.
2. If you are a Windows user, please install [Microsoft Visual C++](https://visualstudio.microsoft.com/visual-cpp-build-tools/) 14.0 or higher (if you don't already have it on your system). Choose Desktop Environment with C++. You may be required to restart the computer after this step.
3. If you are a Linux or MacOS user, ensure that pip is installed as your package manager for Python. You may also have to run `sudo apt-get install python3-tk` or `sudo apt-get install python-tk` before running the installation script (on a Mac, those commands are `brew install python-tk` or `brew install python3-tk`).
4. Download the zip file, unzip it inside the *Fiji.app* directory, and run "CalciumSignal Installer.py" from inside the unzipped folder. The script will create the *CalciumSignal* folder within the *plugins* folder. This is where the files used by the program will go.

NOTE: if you experience problems during the Peak Analysis phase of the project, type the following in a command prompt to downgrade the Matplotlib version, which may fix the problem after restarting the plugin:
`pip install matplotlib==3.4.3`
Otherwise, upgrade your Python installation.

## Startup
### PoorMan3DReg
<img src="https://github.com/jstith09/calcium/blob/main/poorman.jpg" width="200" height="150">

  - Transformation -
  - Z Slices -
  - Projection Type -
 
### Cell Detector
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/celldetector.jpg" width="200" height="200">

  - Threshold -
  - Slice -
  - Size Filter
  - Exclude objects on edges

## Windows

### Custom Roi Manager
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/customroimanager.jpg">

  - Min/Max Cell Diameter:
  - Update Cells:
  - Multi Measure:
  - Outlier Analysis:
  - RC 1/2/3 STD:
  - Grid Suggestions:
  - Create Grid
  
### Image Window
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/calciumwindow.jpg" width="200" height="200">

### Menu
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/celldetector.jpg" width="200" height="200">

### Results
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/resultstable.jpg" width="350" height="150">

### Roi Manager
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/roimanager.jpg" width="150" height="200">

## Credits

Matt Searfass, CJ Spagnolia, Nick Costley, Luke Halko, Jaden Stith


