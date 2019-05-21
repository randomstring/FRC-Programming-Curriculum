<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#sec-1">1. Account setup</a></li>
<li><a href="#sec-2">2. Software Installation &amp; Tool Setup</a></li>
<li><a href="#sec-3">3. WPI lib</a></li>
<li><a href="#sec-4">4. PID controllers</a></li>
<li><a href="#sec-5">5. Motor Controllers and WPI built-in functions</a></li>
<li><a href="#sec-6">6. Advanced Git and Github</a></li>
<li><a href="#sec-7">7. VS Code</a></li>
<li><a href="#sec-8">8. Driver station</a></li>
<li><a href="#sec-9">9. Networking Basics</a></li>
<li><a href="#sec-10">10. General Computer Science</a></li>
<li><a href="#sec-11">11. Basic Physics</a></li>
<li><a href="#sec-12">12. Electronics, Wiring, and Control Systems</a></li>
<li><a href="#sec-13">13. Resources</a></li>
</ul>
</div>
</div>

# Account setup<a id="sec-1" name="sec-1"></a>

-   github (join team group)
-   trello
-   slack (and channels, #programming)
-   MS Teams

# Software Installation & Tool Setup<a id="sec-2" name="sec-2"></a>

-   github
-   VS Code
-   WPI libs install
-   Driver Station
-   motor controller utilities
-   flashing firmware Roborio, Limelight, radio
-   How to update software

# WPI lib<a id="sec-3" name="sec-3"></a>

-   API overview
-   Command based robot
    -   Robot.java
    -   RobotMap.java
    -   OI.java (xbox controllers)
    -   subsystems
    -   commands
    -   command Groups
    -   controlling motors
    -   sensor input
    -   drivetrains (tank, arcade style)
    -   Network tables (reading/writing values)
    -   subsystems and command interaction (scheduler)

# PID controllers<a id="sec-4" name="sec-4"></a>

-   Bang-Bang controller
-   define P, I, and D
-   arm example
-   speed example
-   steering

# Motor Controllers and WPI built-in functions<a id="sec-5" name="sec-5"></a>

-   motor control
    -   setting motor settings
    -   get position
    -   direct PID control from motor controller
        -   vs. WPI lib PID controller
    -   lead-follow  (speed and position)
    -   motion magic
-   WPI Sensors
    -   Gyro
    -   distance sensors
    -   Hall effect, etc&#x2026;
-   LimeLight
    -   walk through limelight's very good examples
-   Pixy cam
    -   object detection
    -   line follow
-   Pathfollowing basics
    -   position & orientation, start and desired target
    -   path selection
    -   path follow (motor speeds)
    -   tracking changes
    -   adapting to errors
-   Pathfollow libraries
    -   Pure Pursuit
    -   Chezy Drive

# Advanced Git and Github<a id="sec-6" name="sec-6"></a>

-   branching
-   pull requests
-   merging

# VS Code<a id="sec-7" name="sec-7"></a>

-   work flow
-   quick commands for building, saving,
-   Github integration
    -   pull, branch, code, commit, push
-   Build and Gradle
-   installing libraries
-   updating libraries
-   special files
    .gitignore .vscode vendordeps

# Driver station<a id="sec-8" name="sec-8"></a>

-   install
-   setup
-   networktables
    -   reading values
    -   writing values
-   exampe PID tuning with DS parameters

# Networking Basics<a id="sec-9" name="sec-9"></a>

-   Wired vs WiFi
-   Switches, routers, Radios, Mesh Networks
-   Network wiring
-   TCP, UDP, HTTP, HTTPS
-   bandwidth, latency, packet loss
-   WiFi
    -   2.4Ghz vs 5Ghz
    -   WiFi interference

# General Computer Science<a id="sec-10" name="sec-10"></a>

-   data structures
    -   basic types, int, float double, char, strings
    -   lists/arrays
    -   structures
    -   enum (?)
-   Constants
-   Abstract Data Types and functions
    -   Java classes 
        -   basic differences between public and private
    -   Java class organization
        -   one per file
        -   how to import
        -   initialization
        -   constructors
        -   destructures
        -   ADVANCED: garbage collection
    -   accessing Java methods and variables
        -   dot notation ClassName.methodName() Classname.variableName
    -   Class inheritance
        -   base classes for Robot subsystem, command, etc
        -   interation with constructors
        -   scheduling methods you don't see under the hood
-   logic
    -   if, then, else
    -   while
    -   for
-   function calls
    -   parameter passing
    -   return values
    -   side effects
-   Style
    -   code readability
    -   variable naming, camel case, unerscores, captiralization, prefixes
        -   no funny joke names
        -   name variables for what they are
        -   \_foo for local variables
        -   other conventions
    -   adopt a style
        -   automatic java style on file save w/ VSCode

# Basic Physics<a id="sec-11" name="sec-11"></a>

-   speed, acceleration, gravity, motion
    -   newton's laws
-   force, momentum, energy
-   levers
-   Vectors
    -   adding force and motion vectors
-   Friction (?)
-   Elastic vs Inelastic collisions (?)
    -   <https://www.khanacademy.org/science/physics/linear-momentum/elastic-and-inelastic-collisions/v/elastic-and-inelastic-collisions>

# Electronics, Wiring, and Control Systems<a id="sec-12" name="sec-12"></a>

-   RoboRio anatomy
    -   layout
    -   power
    -   CPU
    -   input/output (CAN, digital IO, USB)
    -   USB camera
-   CAN bus 
    -   wiring
    -   debugging
-   Example wiring diagrams

# Resources<a id="sec-13" name="sec-13"></a>

-   General
    -   <http://wpilib.screenstepslive.com/s/currentCS>
    -   <https://www.team254.com/resources/>
    -   <https://betawolves.org/resources/>
-   Intro to Command Based Programming (VS Code & Java)
    -   Part 1: <https://youtu.be/wW_djLkD1B8>
    -   Part 2: <https://youtu.be/9MpJgUUsLZw>
    -   Part 3: <https://youtu.be/5Zr7K_2mnrw>
    -   Part 4: <https://youtu.be/YNluD_TNj5E>
    -   Part 5: <https://youtu.be/oGMy4FJLKy4>
-   Online Lessons
    -   <https://frc-west.github.io/>
    -   FRC & Java <https://stemrobotics.cs.pdx.edu/node/4196?root=4196>
    -   AP CS principles <https://www.khanacademy.org/computing/ap-computer-science-principles>
-   Command Based Programming
    -   TODO these needs sorting
    -   <https://wpilib.screenstepslive.com/s/currentCS/m/java/c/88893>
    -   <https://wpilib.screenstepslive.com/s/currentCS/m/java/l/599745-scheduling-commands>
-   Code Examples:
    -   Motor controllers
    -   <https://github.com/CrossTheRoadElec/Phoenix-Examples-Languages/tree/master/Java>
    -   <https://github.com/REVrobotics/SPARK-MAX-Examples>
-   Control:
    -   <https://www.team254.com/documents/control/>
-   Vision:
    -   <https://www.team254.com/documents/vision-control/>
    -   <http://docs.limelightvision.io/en/latest/>  (in particular Programming section)
-   Path Planning:
    -   Intro: <https://wpilib.screenstepslive.com/s/currentCS/m/84338>
    -   <https://www.youtube.com/watch?v=8319J1BEHwM>
    -   SLIDES: <https://docs.google.com/presentation/d/1xjtQ5m3Ay4AYxS_SfloF2n_vWZnCU25aXZuu9A59xPY/pub?start=false&loop=false&delayms=3000&slide=id.p>
    -   pure pursuit: <https://www.chiefdelphi.com/t/paper-implementation-of-the-adaptive-pure-pursuit-controller/166552>
    -   <https://github.com/Dawgma-1712/FRC-2018/wiki/pure-pursuit>
-   Swerve Drive Resources:
    -   <https://www.chiefdelphi.com/t/team-4048-swerve-drive-code-release/166605>
    -   <https://www.strykeforce.org/resources/Mechanical_Design_Description_of_Stryke_Force_Swerve_Drive_Units.pdf>
    -   <https://github.com/strykeforce/cookiecutter-robot>
    -   <https://www.chiefdelphi.com/t/paper-4-wheel-independent-drive-independent-steering-swerve/107383>
-   Related Chief Delphi threads:
    -   <https://www.chiefdelphi.com/t/your-team-sucks-at-programming-heres-why/358026>
-   Misc Programming Resources:
    -   Python FRC robot simulator <https://github.com/robotpy/pyrobottraining>
-   Advanced Programming (not FRC specific):
    -   <https://www.toptal.com/robotics/programming-a-robot-an-introductory-tutorial>
    -   <https://www.coursera.org/learn/mobile-robot/>
