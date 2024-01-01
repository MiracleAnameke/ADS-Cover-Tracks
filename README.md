# ADS Cover Tracks

## Introduction
This lab explores the concept of Alternate Data Streams (ADS) in NTFS file systems to cover tracks. It involves using ADS to hide text and executable files behind seemingly innocuous files without changing their size or functionality. You will use tools like command prompt and hex editor to perform these tasks.

## Before You Begin
- Ensure you have a Windows environment set up as ADS is specific to NTFS file systems.
- Understand the concepts of file streams and how ADS can be used maliciously.
- Ensure all activities are conducted in a controlled environment under ethical guidelines.

## Setting Up the Lab
- Set up a Windows environment with necessary permissions.
- Create a folder named `ads` in the `c:\\security` directory.
- Ensure you have tools like notepad, command prompt, and a hex editor installed.

## Lab Procedure & Screenshots

### Exploit #1 – Cover Tracks with Alternate Data Streams
- **Objective**: Hide a text file behind an image file using ADS.
- **Execution**:
  - Create a text file with your name and save it as `info6001.txt` in the `c:\\security\\ads` folder.
  - Hide this text file behind `plane.jpg` using the command `type info6001.txt > c:\\security\\ads\\plane.jpg:hide.txt`.
  - Retrieve and rename the hidden text to `yourFOLname.txt`.
- **Screenshot 1**: Take a screen capture of the command prompt showing the output of the last two commands (retrieving and renaming the hidden text).
  
  <img src="https://i.imgur.com/loT1EdA.png" height="400px" width="auto" alt="Command Prompt with ADS Commands"/>

### Exploit #2 – Hiding Executable in ADS
- **Objective**: Hide an executable program inside a text file using ADS.
- **Execution**:
  - Hide `felix.exe` behind `yourFOLname.txt` and execute it from the hidden stream.
  - Create a symbolic link to `felix.exe` and execute it to see Felix the cat walking across your screen.
- **Screenshot 2**: Take a screen capture showing the command prompt & Felix.
  
  <img src="https://i.imgur.com/kRiESR1.png" height="400px" width="auto" alt="Command Prompt & Felix"/>

### Exploit #3 – Cover Tracks with Tini
- **Objective**: Modify Tini binary code to change the default listening port and cover tracks.
- **Execution**:
  - Use a hex editor to change the listening port of Tini from 7777 to 8888.
  - Save the modified Tini as `yourfirstname.exe`.
  - Run `yourfirstname.exe` and verify the listening port with the netstat command.
- **Screenshot 3**: Take a screen capture of the netstat command ensuring the process id (PID) is included.
  
  <img src="https://i.imgur.com/xBzfcGw.png" height="400px" width="auto" alt="Netstat with Modified Tini Listening Port"/>

## Conclusion
This lab demonstrates the use of Alternate Data Streams for hiding data and executable files in Windows systems. It illustrates how seemingly normal files can carry hidden data or executables, emphasizing the need for vigilance and robust security practices to detect and mitigate such covert methods.

