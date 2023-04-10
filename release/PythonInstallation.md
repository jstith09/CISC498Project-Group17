Installation instructions for a previous calciumsignal version made in python. Very outdated.

Install

The target platform for this project is Windows 10. We have made it available for MacOS and Linux as well, but extra steps may have to be performed to get things working.

If necessary, download Python 3 for your system. Python 3.9.7 or newer is ideal. Ensure that Python has been added to PATH (there should be an option to do this during the installation process). The plugin will make use of the "python" and "python3" commands on your system.
If you are a Windows user, please install Microsoft Visual C++ 14.0 or higher (if you don't already have it on your system). Choose Desktop Environment with C++. You may be required to restart the computer after this step.
If you are a Linux or MacOS user, ensure that pip is installed as your package manager for Python. You may also have to run sudo apt-get install python3-tk or sudo apt-get install python-tk before running the installation script (on a Mac, those commands are brew install python-tk or brew install python3-tk).
Download the zip file, unzip it inside the Fiji.app directory, and run "CalciumSignal Installer.py" from inside the unzipped folder. The script will create the CalciumSignal folder within the plugins folder. This is where the files used by the program will go.