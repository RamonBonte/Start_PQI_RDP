# Start_PQI_RDP

## Aim
Being able to use Progenesis QI without licensing problems when you are logged in using RDP.
This .bat file will allow you to open existing Progenesis QI experiments and make and license new experiments with the dongle.

## Prerequisites
- Progenesis QI with a dongle on a remote pc (Tested with Progenesis V2.4 & Windows 10 Pro (build 1903))
- Administrator rights on the remote pc
- Your current RDP session id 
  
## Instructions

**Download the bat file**
1. Download or clone the repository to get access to the bat file.

**Retrieving your current session id**
1. Open CMD
2. Type query session and hit enter
3. Your session id is the number before "Active"
4. Memorize this number or write it down. You need this number in the next step.

**Modify the bat - file to match your situation**
1. Open notepad
2. Click File > Open...
3. Change the filter to _All Files_
4. Locate the saved bat - file and open it
5. Change tscon **1** /dest:console into tscon **"your id"** /dest:console
6. Save the changes you made

**Please note:** That Progenesis QI is installed on the default location on my pc. If you installed Progenesis QI on a different location. You also have to change the second line in the bat file to match the path where Progenesis QI is currently installed on our pc.

**Excuting the bat file**
1. Locate the bat file
2. Right-click on the bat file
3. Click on Run as administrator
4. The file will be executed. As a result your RDP connection will be terminated and Progenesis QI will be launch by the local user.

**Next**
1. Login on your remote pc with RDP
2. Progenesis QI will be launched and will recognize the dongle when you open an experiment.
3. You can close the terminal window by hitting the spacebar

## Known limitation
- Only 1 PQI experiment can be opened this way


## To be tested
- Opening multiple experiments. So you can analyze ESI-(+) and ESI-(-) simultaneously




