<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#sec-1">1. Overview</a></li>
<li><a href="#sec-2">2. Weeks:</a></li>
</ul>
</div>
</div>



# Overview<a id="sec-1" name="sec-1"></a>

Combination of offline and in-person classwork. Given the limited
amount of time, much of the setup and work is to be done outside of
the classroom. Class time is primarily for answering questions,
lecture time, and working with the robot.

Possible host office hours (Skype or in person)

# Weeks:<a id="sec-2" name="sec-2"></a>

1.  Classroom: Meta
    -   What is the job of a programmer on an FRC team.
    -   Discuss strategies for learning programming
        -   Meetings are primarily for learning concept specific to
            programming the robot or working on the robot.
        -   requires learning general programming concepts on your own time
    -   Discuss future lesson plans
        -   focused on doing
    -   Discuss strategies for learning to code
        -   no substitute for practice
        -   pick a project and code it
        -   learn to touch type
    -   Review season calendar, programming goals, pre-season prep and learning
    -   Pep talk: This is a lot of work, but you can do it!
    -   list resources for learning programming
2.  Homework: Software Setup
    -   students will be provided with instructions on how to install all the needed software.
    -   YouTube Videos
    -   GOALS:
        -   FRC utilities installed
        -   VS Code installed
        -   GitHub account
        -   clone Robot code
        -   build Robot code
        -   run driver station
3.  Classroom Session: Debug SW Setup
    -   Experienced students with working systems will buddy up with new
        people to help getting everyone up and running
    -   GOALS:
        -   get everyone to the point they can deploy to robot
        -   change code, build, deploy to robot
    -   REQUIREMENTS:
        -   need multiple laptops
        -   USB thumb drives pre-loaded with install libraries
        -   Simple test robot GitHub repo for testing (no pixy libs for example)
4.  Homework: Programming The Robot in VS Code 
    -   YouTube introduction videos
    -   Use VS Code to create new Command Based Robot code using Template
    -   Add code to drive a simple robot
        -   Arcade Drive (use CAN motors)
    -   GOALS:
        -   generate robot code from template
        -   Every student creates a GitHub repo checks in code
        -   modify base robot to drive
5.  Classroom: Hands on with Robot
    -   Lecture & discussion of Command based programming
        -   <https://www.chiefdelphi.com/t/what-is-the-best-way-to-teach-incoming-freshmen/362661/39>
    -   deploy code you built the week before
    -   debug code
    -   GOAL:
        -   everyone deploys their code to the robot and drives it
    -   REQUIREMENTS:
        -   robot
        -   multiple roboRIOs (test deploy)
6.  Homework: Robot subsystem
    -   add subsystem & command for arm control
        -   safety code, stop motor if it goes to far
        -   safety motor speed (multiply by 0.5) for testing
    -   include smart dashboard display of 
        -   arm position (encoder value)
        -   graph motor speed/power  -1.0 - 1.0
        -   PID constants
    -   Use NetworkTables to change PID constants on the fly
    -   REQUIREMENTS:
        -   sample code for smart dashboard & network tables
7.  Classwork: Test Everyone's Subsystem Code
    -   Discussion of PID tuning
    -   Give everyone a chance to deploy code test PID tuning
    -   REQUIREMENTS:
        -   robot
        -   or roboRIO with motor controller and motor, anything requiring PID
8.  Homework: Study Last Year's Code
    -   GOAL:
        -   every student has a list of questions about how/why code works
9.  Classwork: Discuss Code
    -   answer questions
    -   overview
    -   lessons learned
    -   what we could have done better
