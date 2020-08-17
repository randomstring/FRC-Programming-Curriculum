
# Notes for Java Command Based Tutorial

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
  + For Git tab to work, you need to install Git Extensions
    - Git Pull Requests and Issues
    - GitLens
  + Command Pallet is your new best friend
    - use this to build code
    - update WPILib and other libraries
    - create new Java Robot 
    - Control-Shift-P (or Command-Shift-P on MacOS) shortcut
  + 10:55
    - selecting a folder doesn't need your project name in it (as he
      mentions), because when you create a new project or
      download/clone an existing project it already uses a named
      directory (in this example TutorialBot). So he's creating nested
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
    - Robot.java still exists, but much of its code now lives in RobotContainer.java
    - Everything covered in the video is the same

  + 15:10 OI.java
    - no more OI.java
    - instead operator interface/input is configured in
      RobotContainer.java in the ''configureButtonBindings()'' method.

  + 16:10 RobotMap.java now called Constants.java

  + 17:30 Subsystems
    - important, pay attention!

## Video 2: https://www.youtube.com/watch?v=A43CDiXtEdY

  + Note: The template and code for 2020 looks slightly different.

  + 5:00 - Subsystem creation is the same, make sure you choose
  "Subsystem (new)" or "Command (new)" to use the newer 2020 command
  based structure.

  + 7:00 installation and managing Vendor libraries. See:
     - CTRE https://phoenix-documentation.readthedocs.io/en/latest/ch05a_CppJava.html
     - REV robotics: https://www.revrobotics.com/sparkmax-software/
     - other vendors: https://docs.wpilib.org/en/stable/docs/software/wpilib-overview/3rd-party-libraries.html

  + 17:40 Configuring Joystick controls has changed. See: <https://docs.wpilib.org/en/stable/docs/software/commandbased/binding-commands-to-triggers.html> for details on how to configure joystick and button controls.

   I super simple example (not using Command based) can be found here: <https://github.com/wpilibsuite/allwpilib/blob/master/wpilibjExamples/src/main/java/edu/wpi/first/wpilibj/examples/arcadedrivexboxcontroller/Robot.java>

  A command based example can be found here: <https://github.com/wpilibsuite/allwpilib/blob/dc9e560f9b85cb855d3ee50badac68781fc049f3/wpilibjExamples/src/main/java/edu/wpi/first/wpilibj/examples/ramsetecommand/RobotContainer.java#L46-L65>

 + 21:20  Tank drive vs Arcade Drive
    - Tank drive: the driver controls the left and right motor speeds directly using two separate joysticks (the left and right thumb sticks on the Xbox).
    - Arcade drive: the left thumb stick controls the angle of the robot, rotating left/right. The right thumb stick controls the forward/reverse speed.

 + 26:00 no need to define joystick constants. These constants are defined in WPILib GenericHID class. Use the constants there. 

 + 33:40 Always run build before pushing code. It's a good idea to run build before committing changes to avoid committing code that doesn't work. Sometimes you know your code is not working yet, and you want to commit and checkpoint your progress so far. In that case it is OK if the code does not build without errors.

### Choosing CAN id numbers:

The CAN id is the address (like phone number of IP address) of devices
on the CAN bus. The CAN bus is a type of wired network connecting the
RoboRIO to other devices on the robot. Typically motor controllers are
connected to the CAN bus. Each device needs it's own unique CAN id. If
more than one device shares the same CAN Id, then one or more those
devices sharing a CAN id will not be able to communicate.

Be careful to assign unique CAN ids to each motor controller and
sensor on the CAN bus!

How do you know what the CAN ids are for a motor controller? The CAN ids can be set using either Phoenix Tuner software (for CTRE devices) or the SparkMax Client Application (for REV robotics devices).

<https://phoenix-documentation.readthedocs.io/en/latest/ch03_PrimerPhoenixSoft.html?highlight=phoenix%20tuner#what-is-phoenix-tuner>
<https://www.revrobotics.com/sparkmax-software/>

Read more about the CAN bus: <https://docs.wpilib.org/en/stable/docs/software/can-devices/index.html>
  
## Video 3: https://www.youtube.com/watch?v=0Mrc9GxUFhA

+ 2:00 m_time variable
  - in Java it is a good convention to give all your *member* variables that belong to a class the `m_` prefix.
  - member variables are variables that are private to the class
  - using the `m_` prefix also helps differentiate class variables, arguments, and global variables.

+ 6:30 Button Numbers
  - w/ 2020 WPILib button numbers have named constants in the classes
  - for Xbox controllers the Xbox `Button` class defined in [edu.wpi.first.wpilibj.XboxController.Button](https://first.wpi.edu/FRC/roborio/release/docs/java/edu/wpi/first/wpilibj/XboxController.Button.html) has constants for all the button types.
  - HID stands for Human Interface Device (joystick, Xbox controller, mouse, keyboard, etc)

+ 10:20 *WARNING* *WARNING*
  - don't start by having your robot drive autonomously backwards at 70% power for 5 seconds
  - robots can be crazy fast, start out *slow*
  - Always be ready to hit the "kill switch", the space bar on the driver station at the first hint of problems


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
    usually configuration files or directories. That hold information
    about how the code is built (.gradle), VS Code customizations
    (.vscode), WPILib settings (.wpilib that tracks your team number
    for example), .gitignore (what files git should not track), and
    depending on the project possibly several more.
  - For the most part you can ignore all the files beginning with a dot.
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
      the line '''import frc.robot.subsystems.driveSubsystem;'''
    + keeping filenames and directories in sync with your class names
      and hierarchy is important


+ Gradle
  - gradle is a program that builds the robot code from JAVA into
    bytecode that can be deployed to the robot.
  - The process of building can sometimes uncover errors that are not
    apparent in the code from just looking at the syntax. Just because
    VS code doesn't report any errors, doesn't mean the code will
    build correctly. Always run build and correct any build errors
    before committing code to git.
  - Gradle is very powerful and does a lot of heavy lifting behind the
    scenes. The two most important things we need to know are the
    "Build Robot Code" and "Deploy Robot Code" commands.


