# Calcium Signal
***Calcium Signal*** is a plugin for ImageJ that allows you to detect and analyze calcium cells.

## Install
***!!!!NEEDS UPDATING!!!!***

The target platform for this project is Windows 10. We have made it available for MacOS and Linux as well, but extra steps may have to be performed to get things working.
1. If necessary, download [Python 3](https://www.python.org/downloads/) for your system. Python 3.9.7 or newer is ideal. Ensure that Python has been added to PATH (there should be an option to do this during the installation process). The plugin will make use of the "python" and "python3" commands on your system.
2. If you are a Windows user, please install [Microsoft Visual C++](https://visualstudio.microsoft.com/visual-cpp-build-tools/) 14.0 or higher (if you don't already have it on your system). Choose Desktop Environment with C++. You may be required to restart the computer after this step.
3. If you are a Linux or MacOS user, ensure that pip is installed as your package manager for Python. You may also have to run `sudo apt-get install python3-tk` or `sudo apt-get install python-tk` before running the installation script (on a Mac, those commands are `brew install python-tk` or `brew install python3-tk`).
4. Download the zip file, unzip it inside the *Fiji.app* directory, and run "CalciumSignal Installer.py" from inside the unzipped folder. The script will create the *CalciumSignal* folder within the *plugins* folder. This is where the files used by the program will go.

***NOTE: if you experience problems during the Peak Analysis phase of the project, type the following in a command prompt to downgrade the Matplotlib version, which may fix the problem after restarting the plugin:
`pip install matplotlib==3.4.3`
Otherwise, upgrade your Python installation.***

## Startup & Usage
After launching Fiji, navigate to Plugins -> Calcium Signal -> Run Calcium Signal....

Running Calcium Signal without an image uploaded to Fiji will prevent it from starting.

Allow a few moments for the image registration and edge detection to complete. Then, make corrections as needed in the ROI Manager dialogue.

After running multi-measure, the peak analysis phase will begin. You will find the peak analysis outputs in Fiji.app/plugins/CalciumSignal/pythonscript/cell_data.

### PoorMan3DReg
<img src="https://github.com/jstith09/calcium/blob/main/poorman.jpg" width="200" height="150">

  - ***Transformation:*** 
    - Choose a different selection to pick how the image will be changed
      - Rigid Body(Default)
        - Default, Translation + Rotation
      - Translation
      - Scaled Rotation
        - Translation + Rotation + Scaling
      - Affine
        - Translation + Rotation + Scaling + Skewing
  - ***Z Slices:*** 600 (Default) select number of slices (images) you would like from video
  - ***Projection Type:***
    - Average Intensity (Default)
      - Uses an average of the values of the voxels
    - Max Intensity
      - Uses the maximum value of the voxels
    - Sum Slices
      - Averages between the individual slices of voxels
 
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


***NEED TO IMPLEMENT/UPDATE PICTURE***

### Custom Roi Manager
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/customroimanager.jpg">

  - ***Min/Max Cell Diameter:*** Enter values to change what size cells are circled by ROI
  - ***Update Cells:*** Use to update ROI after selecting RC 1/2/3 STD
  - ***Multi Measure:*** Uses the built in ImageJ Multimeasure command to take two ore more slices and take the Area, Min, and Max of all of them then store the result as one measurement.
  - ***Outlier Analysis:*** Displays an outlier analysis chart
  - ***RC 1/2/3 STD:*** Automatically enters 1/2/3 different standard deviations for min/max diameter values
  - ***Grid Suggestions:*** Gives suggested values for 'Create Grid'
  - ***Create Grid:*** Enter values from 'Grid Suggestions' to create grid on image
  - ***Undo [Cntrl + Shift + E]:*** Undo Add/Delete of ROI

### Results Table
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/resultstable.jpg" width="350" height="150">
  - Allows for saving and editing of the results of the slices
  - Contains different measurements and labels depending on the operations used

### ROI Manager
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/roimanager.jpg" width="150" height="200">

  - ***Add:*** When a part of the image is selected, this will add the specific pixels selected to the list. If no part of the image is selected, will return an error.
  - ***Update:*** With an item in the list selected, allows the user to change the size of selected pixels or move the selection. Changes will not be saved unless the update button is clicked a second time after changes were made.
  - ***Delete:*** Deletes the selected item from the list, if nothing is selected, will prompt the user if they wish to delete the entire list.
  - ***Rename:*** Prompts the user to rename the selected item in the list.
  - ***Measure:*** Upon clicking, brings up a new "Results" window, stating the number, mean, minimum, and maximum of the original selection on the image.
<img src="https://github.com/jstith09/CISC498Project-Group17/blob/main/bc6c2b810fab817679cd3362378b3d71.png" width="150" height="150">

  - ***Deselect:*** Deselects the current selection in the group, clicking it while nothing is selected will do nothing.
  - ***Properties:*** Opens up a new tab of the current selection, giving ways to edit the selection
    - ***Name/Range*** Shows the name and allows the user to change it
    - ***Position*** Gives the position of the current selection or group
    - ***Group*** Changes what group the selection is in
    - ***Stroke/Fill color*** Changes the color of the lines/fill of the selection block on the image.
    - ***Width*** Changes the stroke width of the selection box.
    - ***List coordinates*** Lists the coordinates
  - ***Flatten:*** Creates a new RGB image that has the overlay rendered as pixel data.
  - ***More>>:*** ETC.

## Credits

***Matt Searfass, CJ Spagnolia, Nick Costley, Luke Halko, Jaden Stith ..........***


