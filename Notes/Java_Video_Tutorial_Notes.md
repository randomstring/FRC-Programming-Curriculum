
# Notes for Java Comand Based Tutorial

YouTube video: FRC Java Tutorial – WPILib 2019 Command Based Framework
 Ep 1: Overview by team 4627. This is a three part video series.
 

## Video 1: https://www.youtube.com/watch?v=64hPDvphcfA

  + Prerequisites: do Lesson 0 and get software install
  + Assumes you know Java
    - syntax
    - classes
    - inheritance
    - polymorphism
  + UPDATE: new URL for instructions replaces screensteps
    - https://docs.wpilib.org/en/latest/docs/getting-started/getting-started-frc-control-system/index.html
  + CTRE Framework:
    - http://www.ctr-electronics.com/installer-archive
    - documentation : http://www.ctr-electronics.com/control-system/hro.html
  + For Git tab to work, you need to install Git Extentions
    - Git Pull Requests and Issues
    - GitLens
  + Command Pallet is your new best friend
    - use this to build code
    - update WPILib and other libraries
    - create new Java Robot 
    - Control-Shift-P (or Command-Shift-P on macOS) shortcut

  + 10:55
    - selecting a folder doesn't need your project name in it (as he
      mentions), because when you create a new project or
      download/clone an existing project it already uses a named
      directory (in this example TutorialBot). So he's creating nexted
      directories called TutorialBot/TutorialBot, where all his code
      will go. That can get confusing, don't do that.
    - better to create/choose a common directory for all projects
    - I create a directory called "GitHub" where all my project folders go.

  + 12:00
    - This video shows the 2019 WPILib code, there are some small
      changes in structure introduced in 2020.
    - no more OI.java  (OI for Operator Input)
    - no more RobotMap.java (now called Constants.java)
    - added RobotContainer.java (this is where the main loop of the robot runs from)

  + 12:57 Robot.java
    - Robot.java is now RobotContainer.java
    - Everything covered in the video is the same

  + 15:10 OI.java
    - no more OI.java
    - instead operator intraface/input is configured in
      RobotContainer.java in the configureButtonBindings() method.

  + 16:10 RobotMap.java now called Constants.java

  + 17:30 Subsystems
    - important, pay attention!



# General Notes:

+ There are two major companies of motor controller, motors, and sensors
  - Cross the Road Electronics (CTRE) 
       - most products are named after birds: Falcon, Talon, etc
  - REV Robotics
       + make NEO motors and controllers SparkMax
  - each has its own library to interface with WPILib.
  - Our team uses both types brands of motors, etc.
  - Each has it's own API (coding interface) 
    + they are very similar (they do the same thing!)
    + however, they are different (this is slightly annoying and sometimes confusing)
    + CTRE Docs: https://www.ctr-electronics.com/downloads/api/java/html/annotated.html
    + CTRE Examples: https://github.com/CrossTheRoadElec/Phoenix-Examples-Languages
    + CTRE Differential Drive Example: <https://github.com/CrossTheRoadElec/Phoenix-Examples-Languages/blob/master/Java%20Talon%20FX%20(Falcon%20500)/DifferentialDrive/src/main/java/frc/robot/Robot.java>
    + REV Robotics Docs: https://www.revrobotics.com/content/sw/max/sw-docs/java/index.html
    + REV Robotics Examples: https://github.com/REVrobotics/SPARK-MAX-Examples
    + REV Robotics Tank Drive Example: https://github.com/REVrobotics/SPARK-MAX-Examples/blob/master/Java/Tank%20Drive%20With%20CAN/src/main/java/frc/robot/Robot.java

+ Files and Directories in your workspace
  - Anything that begins with a "." (dot, also known as a period) are
    usually configutation files or directories. That hold information
    about how the code is built (.gradle), VS Code customizations
    (.vscode), WPILib settings (.wpilib that tracks your team number
    for example), .gitignore (what files git should not track), and
    depending on the project possibly several more.
  - For the most part you can ignore all the files begining with a dot.
  - venderdeps hold information about third party code being used. For
    instance it will hold information about what version of the CTRE
    API you are using. These libraries are installed using the command
    pallet "Manage Vendor Libraries" command.
  
+ Where's the code that controls the robot?
  - it is "hidden" (organized?) in the directory: src/main/java/frc/robot
  - src (short for "source code") is where many projects place code
  - main/java is typical Java project directory organization
  - frc/robot and subfolders correspond to the Java Class hierarchy
    + for example to include the Java class defined in
      src/main/java/frc/robot/subSystem/driveSubsystem.java you use
      the line "import frc.robot.subsystems.driveSubsystem;"
    + keeping filenames and directories in sync with your class names
      and hierarchy is important


+ Gradle
  - gradle is a program that builds the robot code from JAVA into
    bytecode that can be deployed to the robot.
  - The process of building can sometimes unocover errors that are not
    apparent in the code from just looking at the syntax. Just because
    VS code doesn't report any errors, doesn't mean the code will
    build correctly. Always run build and correct any build errors
    before commiting code to git.
  - Gradle is very powerful and does a lot of heavy lifting behind the
    scenes. The two most important things we need to know are the
    "Build Robot Code" and "Deploy Robot Code" commands.


