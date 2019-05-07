# GPS Provisioning Script

## Table of contents
- [Summary](#sum)
- [Requirements](#requirements)
- [Installation](#install)
- [CUPS Setup](#CUPS)
- [Printer Setup](#psetup)
- [Running the Script](#run)
- [References](#ref)
- [Extra](#extra)

<div id='sum'/>

## Summary
**WARNING: Only able to work on Mac currently and with Python 3.7.2. To avoid complications, it is highly recommended to run the provisioning script in a virtual environment and Python release 3.7.2**

Summary of Provisioning Script


<div id='requirements'/>

## Requirements
**Python (3.7.2)**

**CUPS (if mac)**

<div id='install'/>

## Installation
- To install python go [here](https://www.python.org/downloads/)
- Hover over the "Downloads" button and choose your operating system ("Windows" or "Mac OS X")

**For Windows**
- Under "Stable Releases" download eiather downloader or installer for 3.7.2 release
- For a video tutorial on of python 3.7.2 on windows go [here](https://www.youtube.com/watch?v=ndrCfBJkkvE)

**For Mac OS X**
- Under "Stable Releases" download correct installer
- For a video tutorial of python 3.7.2 on mac go [here](https://www.youtube.com/watch?v=8BiYGIDCvvA)

**NOTE: For Mac OS X users, you may have to install Common Unix Printing System (CUPS) for setting up the printer. Instructions on this can be accessed at the lower section or by clikcing [here](#CUPS)**

<div id='CUPS'/>

## CUPS Setup (MAC OS X Users only)
**Open your Web browser and follow the instructions**
- Type or command/paste http://localhost:631/printers/ 
- **NOTE: if you see "Web interface is Disabled" follow steps below**
- Open Terminal application on Mac
- either type or command/paste "WebInterface=yes" into the terminal and run command
- Refreseh the page where "Web interface is Disabled" is at

**Once you are on the CUPS page**
- Select the "Home" tab
- Select "Adding Printers and Classes"
- Click "Add Printer"
- Login with your username and password for your mac.
- Plugin your zebra printer via USB cable then refresh browser

**After refreshing the page, your printer should appear**
- Select the zebra label printer that you are using. This will be under "Local Printers"
- Change the name of the printer for ease of use during usage of the script.
- Uncheck "Share This Printer"
- Click "Continue"
- Choose the correct option in the "Model" options
- Choose the type of your printer.
- Select "Add Printer"

**After Adding the Printer**
- Change the media size to "Custom"
- Set the width to "2.25" and the height to "1"
- Change the units to "Inches"
- Change the resolution to "300 DPI"
- Set the media Tracking to "Non-continuous (Web sensing)"
- Choose "Set Default Options"

**Go back to the http://localhost:631/printers page**
- Select on the name of the printer you just created
- Under the "Administration" tab, click there and choose `Set Default Options`
- Click "Printer Settings"
- Change the Darkness to "24"
- Select the "Set Default Options" tab

If more information is needed users can go [here](http://support.ordercup.com/support/solutions/articles/217695-installing-the-cups-driver-for-zebra-printers-on-mac-os-x)

<div id='psetup'/>

## Printer Setup
- Open Terminal
- _Pip usage_
- *ENTER* in Terminal or CMD `pip3.7 install -r requirements.txt`

<div id='printerwin'/>

## To set up the printer on windows
- To Be Determined

<div id='run'/>

## Running the Script
**For MAC**
- Open Terminal 
- Type the following: `python3.7 runner.py`

<div id='ref'/>

## References
- [John Cobb](https://github.com/johncobb/cfgmdm)

<div id='extra'/>

## Extra Information
- The COM Port is the name or location of the serial port.
- for virutalenv setup: https://sourabhbajaj.com/mac-setup/Python/virtualenv.html
