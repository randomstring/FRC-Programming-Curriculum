# Lesson 1

The goal of this lesson is to use VS Code and its automated code
generation tool to create a new robot project, add our own custom
code, build that program, and deploy it to a robot!

You will also publish this code to your GitHub account.

Don't worry if you can't code (yet). This exercises is about getting
familiar with the tools you'll be using.

## Building a Test Project

### 1. Launch VS Code and create a new project

If you used the PC installer, it should have a shortcut link on the
desktop top run VS Code.

Next open a new window by pressing Ctrl+Shift+N (or Command+Shift+N on the mac)

![VS Code New Window](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/main/Lessons/imgs/VSCode_New_Window.png)

### 2. Press Control+Shift+P (or it may be Command+Shift+P on a Mac) This will open the Command Palette. Or just click on the "W" in a red hexagon icon in the upper right corner.

![VS Code Command Palette](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/main/Lessons/imgs/Command_Palette.png)

This is a text window where you can execute commands to build code,
update vendor libraries, set your team number, change the the Java
library path, and many other tasks. Most of the time it's easier to
just click on menu, files, and icons, but sometimes the command
palette is the easiest way and sometimes the only way to run certain
commands.

### 3. In the Command Palette, type "WPILib: Create a new project" and hit return.

The command Palette will try to auto-complete and guess what
command. So you can just type "new project" for instance and then
select "WPILib: Create a new project" from the list of suggestions.

![WPILib Project Creator](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/main/Lessons/imgs/WPILib_Project_Creator.png)

Work your way through the options, feel free to explore, but for this lesson select:

```
  Project Type: Template
  Language: Java
  Project Base: Command Robot
  Project Name: MyFirstRobot
  Team Number: 2930
```

Select a folder to place your project into. This should be your local
"GitHub" directory, for instance your "Documents/GitHub" directory
that you set up in lesson 0. This should *NOT* include the name of
your project, that directory will get automatically created when you
click the "Generate Project" button at the bottom.
  
Then click on "Generate Project"

![WPILib New Project](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/main/Lessons/imgs/WPILib_New_Project.png)

VS Code will ask you if you want to open the project. Select "Yes (Current Window)"

Things should look like this:

![WPILib project init](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/main/Lessons/imgs/WPILib_init.png)

### 4. OPTIONAL: Github

This is a great time to start using GitHub. For instructions on creating your first GitHub repo see the [GitHub Lesson 1](./01a-Optional-Github.md).

### 5. Customize the code

Next you will customize the code so it works with your robot. If you get stuck, consult the reference [MiniBot Code](https://github.com/FRC-Sonic-Squirrels/MinibotCode) in the team's Github repo.

The outline of the steps will be:
1. Install required vendor code to control motors.
2. Create a [subsystem](https://docs.wpilib.org/en/stable/docs/software/commandbased/subsystems.html) to control the drivetrain motors.
3. Instantiate a class to get user input from an [XboxController](https://first.wpi.edu/wpilib/allwpilib/docs/release/java/edu/wpi/first/wpilibj/XboxController.html).
4. Create a [command](https://docs.wpilib.org/en/stable/docs/software/commandbased/commands.html) that takes input from the Xbox controller and tells the drivetrain to move the robot.
5. [Build and deploy](https://docs.wpilib.org/en/stable/docs/software/vscode-overview/deploying-robot-code.html) the code to the robot.
6. Drive a robot!

#### Adding Vendor a Dependency

Most robots use motor and controls electronics from [Rev Robotics](https://www.revrobotics.com/), [Cross the Road Electronics](https://store.ctr-electronics.com/) or both. Each of these vendors for FRC parts provide their own code for controlling their respective electronics. These are not included in your WPILib installation by default and must be added to your code repository before you can use them. 

For this project we will be using REV Neo motors for our simple robot. So we will add the REV Robotics vender dependency. These vender dependency files get put in the `venderdeps` directory in your code repo. 

We will want to add the REV vender dependency file from `https://software-metadata.revrobotics.com/REVLib.json` you can copy it by hand, or follow the [instructions on installing vender dependencies](https://docs.wpilib.org/en/stable/docs/software/vscode-overview/3rd-party-libraries.html).

*NOTE: Vender libraries are updated each competition year and sometimes mid season, so confirm you are installing the latest version.*


#### Creating Constants

Open the file `Constants.java` and edit it to look like this:

[MinBot Constants](https://github.com/FRC-Sonic-Squirrels/MinibotCode/blob/5667e958312aba5ce13b4ff313da0657d39875fa/src/main/java/frc/robot/Constants.java#L18-L24)

<script src="https://gist.github.com/randomstring/6b8e9610ccbfb1b70901472a5fcda9c8.js"></script>

#### Creating a Subsystem

[Subsystems](https://docs.wpilib.org/en/stable/docs/software/commandbased/subsystems.html) are Java classes that control a specific part of the robot. Read the [WPIlib documenation on subsystems](https://docs.wpilib.org/en/stable/docs/software/commandbased/subsystems.html) for more detailed information. They have a very good explanation.

The first, and most important, subsystem for any robot is for the drivetrain. Otherwise we have a robot that can't move, and a stationary robot isn't very useful.

Open src/main/java/frc/robot/Robot.java and scroll down to the function robotInit()

1. create `Drivetrain.java` subsystem in subsystem folder
2. edit `Drivetrain.java` to have
  * two motors, using the [CANSparkMax](https://codedocs.revrobotics.com/java/com/revrobotics/cansparkmax) class
  * create a [DifferentialDrive](https://first.wpi.edu/wpilib/allwpilib/docs/release/java/edu/wpi/first/wpilibj/drive/DifferentialDrive.html) class

Create the Drivetrain.java file, but right clicking (or Ctr-clicking if you're using a Mac) the `subsystems` directory name in VSCode's file explorer. Then select the `Create new class/command` option. In the selector box that appears, type in `Subsystem` and make sure to select `Subsystem (new)`. Next it will ask you for a name for the new subsystem, this will be both the name of the file and the name of the class that is created. Classes should always start with a capital letter. Type `Drivetrain` into the box and continue. 

Now a file names `Drivetrain.java` will appear in your subsystem folder. Click on it to open it (if it isn't already) and edit it as follows.


#### Adding a XBox Controller

TODO: add XBOX controller to `RobotContainer.java`
#### Putting it Together

TODO: new code, explanation

### 7. build code

From the command pallet type "build" and select "WPILib: Build Robot Code"

TODO: Check for errors. 


### 8. deploy code to robot (in class)


# Resources

 - VS Code
   + keyboard shortcuts: https://code.visualstudio.com/docs/getstarted/keybindings#_keyboard-shortcuts-reference

 - GitHub
   + pushing a new repo to GitHub.com:  https://gist.github.com/c0ldlimit/4089101
   + about remote repos:  https://help.github.com/en/github/using-git/managing-remote-repositories


# Next Steps

## Getting a Copy of the Team's Robot Code

The next thing to try is to download the team's current robot code and
building that.

Start by creating a new window. In VS Code open a new window
(Control-Shift-N) and then in the command palette type "git clone" and
give the URL
https://github.com/FRC-Sonic-Squirrels/2020-RobotCode.git

## Importing 3rd Party Libraries

Much of the code that interfaces directly with the robot's hardware
(motor controllers and sensors) is supplied by the manufacturers of
those device. To make use of those devices on your robot, you will
need to download and install the 3rd party software. VS Code has a
function "Manage Vendor Libraries" that can be access through the
WPILib command pallet. Check this [comprehensive list of 3rd party
software](https://docs.wpilib.org/en/latest/docs/software/vscode-overview/3rd-party-libraries.html#rd-party-libraries).

Chances are your robot will use sensors and motors from Rev Robotics,
Cross the Road Electronics (CTRE), or both. Here are the instructions
for installing these two major 3rd party libraries.

### Rev Robotics

Go to the "JAVA API Installer" section on
https://www.revrobotics.com/sparkmax-software/ and follow the
instructions.

1. In VS Code, open a project and from the command pallet choose
"Manage Vendor Libraries", check "install new (online)", and then
enter this url:
https://www.revrobotics.com/content/sw/max/sdk/REVRobotics.json

### Cross the Road Electronics

1. Download latest installer from
https://github.com/CrossTheRoadElec/Phoenix-Releases/releases and run it.

2. Then in VS Code, open a project and from the command pallet
choose "Manage Vendor Libraries", check "install new (offline)", and
then select CTRE.


