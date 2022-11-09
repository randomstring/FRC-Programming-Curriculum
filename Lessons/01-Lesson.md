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

![VS Code New Window](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/master/Lessons/imgs/VSCode_New_Window.png)

### 2. Press Control+Shift+P (or it may be Command+Shift+P on a Mac) This will open the Command Palette. Or just click on the "W" in a red hexagon icon in the upper right corner.

![VS Code Command Palette](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/master/Lessons/imgs/Command_Palette.png)

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

![WPILib Project Creator](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/master/Lessons/imgs/WPILib_Project_Creator.png)

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

![WPILib New Project](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/master/Lessons/imgs/WPILib_New_Project.png)

VS Code will ask you if you want to open the project. Select "Yes (Current Window)"

Things should look like this:

![WPILib project init](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/master/Lessons/imgs/WPILib_init.png)

### 4. Initialize Git and Connect your repo to GitHub.com

Next we're going to initialize our git repo and push code to
github.com. We do this now so that we record the initial state of the
code before we start making changes. This way we can track every
change we make and if want to revert back to an earlier working copy
of the code, we can do that.

GitHub also acts as a backup of our code so we don't lose it. GitHub
also let's us share our code with other members of the team so we can
collaborate.

![Initialize local directory to use git](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/master/Lessons/imgs/Git_init.png)

Open the VS Code command palette and type "git init" and select the
"Git: Initialize Repository" option. Select the current directory
(should be called MyFirstRobot).

Go to GitHub.com, make sure you're logged in and navigate to your
Repositories page/tab. In the upper right of the page there should be
a green "New" button for creating a new repo. Click it.

![New GitHub repo](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/master/Lessons/imgs/GitHub_new_repo.png)

Fill out the form just like it is in the picture. The repository name
should match the name of the local project directory. In this case
"MyFirstRobot". The other fields are not critical, but it is good
practice to give a good one sentence description for your
projects. Leave the setting the ".gitignore" option to "None."

Click the green "Clone or download" button and copy the URL. You'll
need that for the next step. For me the URL looks like
"https://github.com/randomstring/MyFirstRobot.git" yours will have
your own username instead of "randomstring."


In the VS Code terminal (from the top menu select View > Terminal or press Ctrl+` ) then run the following command:

```bash
git remote add origin https://github.com/YOUR_USERNAME/MyFirstRobot.git
```

This command connects your local git repository where you will be
making changes, to your remote repository hosted on github.com.
### 5. Commit your Code

For your first commit message use "WPILib generated code"

When committing code to github, you first you stage the changes. In VS
Code you just click the "+" (plus icon) for the files and this sets
the check in message for each of your files. You can click the big "+"
icon at the top to commit all the changed files at once.

Next you click the check mark at the top to finish the commit. 

![Git commit](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/master/Lessons/imgs/VSCode_git_commit.png)

Now you can publish your changes back to GitHub.com. Just click the
little cloud icon in the lower left.

![Publish changes to GitHub](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/master/Lessons/imgs/VSCode_git_publish.png)

You will be prompted for your github username and password by VS Code.

Run the following in the *Terminal* window in VS Code. You can open a new terminal in VSCode by pressing ``Ctr-` `` or running the `>Terminal:Create New Terminal` in the command prompt.

```bash
git config --global user.email "yourname@email.com"
git config --global user.name "your username"
```

![Terminal Example](https://raw.githubusercontent.com/randomstring/FRC-Programming-Curriculum/master/Lessons/imgs/terminal_set_git_config.png)



You have now pushed your code to GitHub! You can now go to your
github.com page and navigate to your new online repo.

### 6. Customize the code

TODO: modify the code to use the correct motor classes and motor ids
as our actual robot. These will differ from those in the example code.

Open src/main/java/frc/robot/Robot.java and scroll down to the function robotInit()

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


