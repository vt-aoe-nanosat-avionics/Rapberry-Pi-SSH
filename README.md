# Rapberry-Pi-SSH
This repository goes over how to SSH into the Raspberry Pi and test that you can flash a board while away from the lab

## Setting up SSH on the Pi
This step is rather simple to do as it only requires one command and turning something on in settings! You will need to install openssh-server, and to do this, type in the following:
```bash
sudo apt install openssh-server
```
After doing this, go to Settings --> System --> Secure Shell and turn it on. You will probably need a password in order to turn it on. To verify that it has been install correctly, simply type in the following command into the terminal: 
```bash
sudo systemctl status ssh
```
You should see something familar below: 

![alt text](https://github.com/vt-aoe-nanosat-avionics/Rapberry-Pi-SSH/blob/main/Images/Screenshot%20From%202024-10-29%2013-02-27.png)

## Accessing via Powershell
Next will be verify that you can access the Pi from your device. In order to do this you need do the following first:
1) Ensure that you are on the same WiFi network as the Pi as you won't be able to access it otherwise
2) Make sure you know your username on the Pi when trying to access it as this is important
3) Verify that you have the correct IP address. To do this, go to your Pi, Go to Settings --> WiFi --> Network Options (The one that the Pi is currently connected to) --> IPV4 Address

Once you have done all the correct information, navigate to Powershell on your Windows computer, and type in the following:
```bash
ssh (username)@IPV4
```
From here, type in yes to accept and then enter your password associated with the Pi. After doing all of this, you should have been prompted with something like this below:

![alt text](https://github.com/vt-aoe-nanosat-avionics/Rapberry-Pi-SSH/blob/main/Images/Powershell%20Screenshot.JPG)

This should indicate that you have done this correctly. NOTE: SSH IS SLOW, BUT IT IS BENEFICIAL WHEN YOU WANT TO WORK ON THE PI FROM A DISTANCE.
