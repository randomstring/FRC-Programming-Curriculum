# Lesson 0

The goal of this homework assignment is to create a working
development environment so you can write code and run it on a FRC
robot. 

If you don't have access to a computer at home, the team and the
schools have computers for use during meetings and in their libraries
or computer labs. In special circumstances the team may have a spare
laptop that can be loaned out to students in need.

The software required can be installed on a Windows or a Mac. Laptops
are preferable as it makes it easier to collaborate in programming
meetings and to get code onto the robot. Windows and Mac are on even
footing for programming (this is done using VS Code). However, many of
the supporting programs, like the driver station for controlling the
robot are Windows only. The team has dedicated Windows laptops for
this, so it's only a minor inconvenience to use a Mac for coding and the
shared team laptop as a driver station.

If you get stuck or aren't sure how to proceed, ask me or the rest of
the sub-team for help!

# Account setup
    
Our team uses several different services to store and track changes in
    our code and to communicate with our fellow programmers.
    
1. [Github](https://github.com/FRC-Sonic-Squirrels) to store our code,
   track changes, and collaborate.

2. [Microsoft Office 365/Teams](https://login.microsoftonline.com/) is
   a suite of services including online meetings, chat, email, file
   sharing. To get an account, contact Jason Reiner or Bryn Dole so
   they can create an account for you.
    
Start by going to <https://github.com/join> and creating an
account. When choosing an account name and avatar, keep in mind your
GitHub account will be visible to all and should meet team and school
standards. Github is also a good way to share your work with others
and can act as a coding resume. Next, email your GitHub username to
your programming lead and/or mentor so they can grant you access to
your team's Github repositories (that's what Github calls a project
folder).
	
Next, you will need to join the Sonic Squirrel Microsoft Teams and 
the #programming Team. The easiest way to do this is to email the team
(sonicsquirrels@gmail.com) and ask to be added. Make sure you include
your name and email in the message so the admin knows who you are.
    
If you already have a MS Teams account and a @sonicsquirels.com email
you can log in via the website space <https://teams.microsoft.com/> or
download and install the MS Teams app on your desktop and/or
smartphone. Then add yourself to the programming Team. Click on
"Teams" in the left side bar, then click on the "Join or Create Team"
in the upper left. Next select the Programming Team to join. Feel free
to join any other Teams that look interesting.

Here is a [direct link to Programming Team discussion on Microsoft Teams](https://teams.microsoft.com/l/team/19%3a0b27cc1537dc4ea5b0b6a7387bacc1cd%40thread.tacv2/conversations?groupId=39c4b64e-fd6d-4f8f-9c24-a9369ee1f34d&tenantId=c193446f-2653-4470-a85b-3a5a94ee8ab5).

Teams has a desktop app for both Mac and PC, and smartphone apps for
both the iOS and Android. Installing 

While you're waiting to get added to the team's accounts, take a
moment to browse your team's code on Github. Team 2930's code resides
at <https://github.com/FRC-Sonic-Squirrels/> for the code last two robots is at
<https://github.com/FRC-Sonic-Squirrels/FRC-2019-Public> and
<https://github.com/FRC-Sonic-Squirrels/2020-RobotCode>.


# Software Installation Requirements
    
Next we need to setup the development environment on your
      computer. This is a set of tools for editing, building, testing,
      and deploying code. The software is all free. The tools we will
      install are:
    
1. *VS Code* This is an IDE (Integrated Development Environment) that
        is a file editor with added intelligence that understands the code
        you write and helps automates much of the process of editing,
        debugging, and running programs.
2. *FIRST supplied tools* These include programs for generating
        robot programs using an interactive GUI (Graphical User
        Interface), a robot path planner, WPIlib (code that controls
        the robots motors and sensors), a Java Runtime Environment,
        and Shuffleboard (a tool for monitoring what's happening on the
        robot.) Don't worry about the details yet. What you need to know is
        this is code that gets used by VS Code and the robot and makes
        our work *much* easier.
3.  *GitHub desktop* This is a GUI for working with code stored on
        github.com. Most of your interactions with GitHub will be handled
        by VS Code and this installs the programs VS Code will use behind
        the scenes.
    
To install the software you'll need a computer or access to
one. Pretty much any PC, Mac, or Linux computer or laptop will work. A
laptop you can bring to programming meetings is ideal. Almost any
laptop, even very old and slow ones, will work. The team has a few
laptops that can be shared. The team can help you setup an old cast
off laptop. And our high schools have libraries and computer labs for
after-school computer time.
	  
If you don't have a laptop that you can bring to meetings, we're
working on possible solutions to allow students to keep their working
environment on a portable thumb drive. If this sounds useful to you,
speak up so we can put time into making this solution work for anyone.
    
Your laptop will need WiFi in order to connect to the school network
and also to connect to the robot. A USB 2.0/3.0 port is useful for
hardwired connections to the robot. Having an Ethernet port, or
USB-to-Ethernet adapter, is a nice to have but not necessary.

## Software Installation
    
Follow the instructions outlined here. Note, the main instruction is
to follow the link to wpilib.screenstepslive.com and follow the
detailed instructions there.
    
<https://github.com/wpilibsuite/allwpilib/releases>
    
You start by downloading the appropriate software bundle for your
computer and operating system. To do this scroll down to the section
of the page that looks like this:

![Download links look like this](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/master/Lessons/imgs/Download_Links.png)

Download the bundle, extract it (TODO: specific instructions) , and
then run the installer. Follow the installation steps outlined on the
official FRC website:
<https://frc-docs.readthedocs.io/en/latest/docs/getting-started/getting-started-frc-control-system/wpilib-setup.html>


Here's a YouTube video installation
guide: <https://www.youtube.com/watch?v=AWf_4dxKpT8> NOTE: This video
is from January 2019, some file names will have changed due to new
software releases.


### TL;DR Quick Start Guide

If you have all your accounts set up, you can jump straight to the installation.


 1. Follow instructions for your computer. Select download VS Code with all other installs. <https://frc-docs.readthedocs.io/en/latest/docs/getting-started/getting-started-frc-control-system/wpilib-setup.html>
 2. No need to install LabView.
 3. Install FRC tools *Windows Only* <https://docs.wpilib.org/en/latest/docs/getting-started/getting-started-frc-control-system/frc-game-tools.html>
 4. Install GitHub extention for VSCode <https://code.visualstudio.com/docs/editor/github>
 

Notes:
 - When finishing the FRC tools install, ignore the request for a serial number.

### Install Git

Go to <https://git-scm.com/> and download and install git.

When installing use all the suggested defaults settings. 

### GitHub Desktop

Next install the GitHub desktop software. If given the choice, install CLI (Command Line Interface) tools.
<https://desktop.github.com/>

To complete the installation of GitHub Desktop, you will be prompted to sign into your github accout.

### GitHub VSCode Integration

Follow directions to install the "GitHub Pull Requests and Issues" extention to VS Code. <https://code.visualstudio.com/docs/editor/github>

# Resources

## GitHub and Git

FIRST has a great introduction to Git and GitHub here: <https://docs.wpilib.org/en/latest/docs/software/basic-programming/git-getting-started.html>

## Robot Harware

Background about the hardware of the robot can be found at this
website about [control system
hardware](https://docs.wpilib.org/en/latest/docs/getting-started/getting-started-frc-control-system/control-system-hardware.html).

## Robot Control

The official software guide can be found here: [getting started with
FRC control
systems](https://docs.wpilib.org/en/latest/docs/getting-started/getting-started-frc-control-system/intro.html).

# Advanced Topics
    
If you don't have a laptop you can try to install all the software
onto a portable thumb drive or some other type of portable media. This
will let you carry your entire programming environment with you. You
just need to borrow a computer with the same operating system and run
VS Code directly from your thumb drive. The school has sets of
classroom laptops we could use for this purpose.
    
WARNING: We haven't actually tried this yet!

<https://www.chiefdelphi.com/t/portable-vscode-install/356115>

