# Vehicle-hail-dent-detection

This is the software part of the hail detection system, and should be used along with the hardware system. Download this folder to your desktop, then start terminal to type in the following commands. 
You can also skip to the dent detection section and run the software with pre-taken photos in the folder.

## Image acquisition
This is the GUI installation guide for Raspberry Pi. 

### Installing
(If you are our sponsor and have our Rasberry Pi, you don't need to install anything, just skip to running.)<br/>
Install Python3
```
sudo apt-get install python3-dev libffi-dev libssl-dev -y
```
Install Tkinter
```
sudo apt-get install python-tk
```
Copy the pigui.py file into a folder

### Running
Go to the folder of the pigui.py, for example:
```
cd Desktop/ME470
```
Run program
```
python3 pigui.py
```
Click "clear files" to delete old images. Then click take photo for 23 times as another operator pushes the light along the 23 tick. Then switch to a Windows machine and use WinSP to copy the 23 raw images into the working folder.


## File transfer

Install WinSCP: https://winscp.net/eng/index.php
<br/>

Connect to Raspberry Pi.(username: pi, password: me470)
<br/>

Obtain Raspberry Pi MAC address:
<br/>
Type the following command in Raspberry Pi terminal
```
ifconfig wlan0
```
The MAC address should be something like "fe80::5280:6726:a47d:f38c"



## Dent detection
It is recommended to install and run on Windows. 
```
cd Desktop/Vehicle-hail-dent-detection/
```

### Installing software
Install virtual environment
```
pip install virtualenv
```

Create virtual environment for python3

```
virtualenv -p python3 env
```

Start virtual environment
```
source env/bin/activate
```

install dependencies
```
pip install -r requirements.txt
```

### Running
```
python3 Simpler.py
```
Assuming there are already 23 raw images copied over from raspberry pi, the program should run with no problem. Click through the buttons. After the last step, go to the folder and open detected.jpg for a clearer result.

### Finishing
Quit virtual environment
```
deactivate
```
