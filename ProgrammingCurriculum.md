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
<li><a href="#sec-11">11. Debugging code</a></li>
<li><a href="#sec-12">12. What is it like to be a Programmer?</a></li>
<li><a href="#sec-13">13. Basic Physics</a></li>
<li><a href="#sec-14">14. Electronics, Wiring, and Control Systems</a></li>
<li><a href="#sec-15">15. Programming Projects</a></li>
<li><a href="#sec-16">16. Suggested Programming Calendar</a></li>
<li><a href="#sec-17">17. Resources</a></li>
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
-   OI
    -   WhenPressed, WhilePressed, Toggle, etc
    -   instantiating of commands classes
-   WPI Sensors
    -   Gyro
    -   distance sensors
    -   Hall effect, etc&#x2026;
-   WPI USBCamera class
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
    -   comments
        -   need to be accurate and up to date
        -   add to the code to increase understanding
        -   comments should explain WHY not WHAT, the what should be obvious from your code.
        -   include refernces to documentation, API, etc
    -   adopt a style
        -   automatic java style on file save w/ VSCode

# Debugging code<a id="sec-11" name="sec-11"></a>

-   print to the console
    -   print values, weird conditions, errors
-   check for expected and unexpected values (assert statements)
-   defensive programming (ignore bad input, or just STOP)
-   check your assumptions
-   If you are confused about what the code is doing, then you don't
    understand the code or you don't understand what's going
    on. LEARN what's really happening, don't keep changing the code.

# What is it like to be a Programmer?<a id="sec-12" name="sec-12"></a>

-   expect to spend lots of time googling and reading webpages
    -   alway backup your code
        -   ABC: Always Be Commiting. Use version control (github for example)
    -   Use branches
        -   bookmark working code, keep experimental code off the main branch
    -   nothing ever works the first time
    -   every line of code is an opportunity for a bug
        -   off by one errors ( < vs <= )
    -   study other peoples code
    -   copy from the best
    -   learning how to debug
        -   ask for help
        -   explain your problem to someone (or rubber duck)
    -   typing skills are important

# Basic Physics<a id="sec-13" name="sec-13"></a>

-   speed, acceleration, gravity, motion
    -   newton's laws
-   force, momentum, energy
-   levers
-   Vectors
    -   adding force and motion vectors
-   Friction (?)
-   Elastic vs Inelastic collisions (?)
    -   <https://www.khanacademy.org/science/physics/linear-momentum/elastic-and-inelastic-collisions/v/elastic-and-inelastic-collisions>

# Electronics, Wiring, and Control Systems<a id="sec-14" name="sec-14"></a>

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

# Programming Projects<a id="sec-15" name="sec-15"></a>

-   the best way to learn is to have a project, a reason to learn and use the skills
-   Clean room program last year's robot from scratch

# Suggested Programming Calendar<a id="sec-16" name="sec-16"></a>

-   Pre-Season
    -   practice robot, with basic drive and a few sensors
-   week -2
    -   update software for new season
        = driverstation
        = firmware for roborio, radio
        = VSCode
        = motor contoller firmware
        = everything
-   Week 0
    -   survey build teams, make list of components
    -   plan subsystems, basic commands,
    -   create code for drivable robot
    -   plan Driverstation layout
    -   plan vision systems and camera placement
    -   start writing subsystem (even if just stubs)
    -   pic CAN bus, IO assignments for sensors, etc.
    -   Give specs to Control subteam
-   Week 1
-   Week 2
-   Week 3
-   Week 4
-   Week 5
-   Week n+1

# Resources<a id="sec-17" name="sec-17"></a>

-   General
    -   <http://wpilib.screenstepslive.com/s/currentCS>
    -   <https://frc-docs.readthedocs.io/en/latest/>
    -   <https://www.team254.com/resources/>
    -   <https://betawolves.org/resources/>
-   Places to Ask for Help
    -   <https://www.chiefdelphi.com/tags/programming>
    -   <https://discord.gg/frc>
-   Intro to Command Based Programming (VS Code & Java)
    -   Part 1: <https://youtu.be/wW_djLkD1B8>
    -   Part 2: <https://youtu.be/9MpJgUUsLZw>
    -   Part 3: <https://youtu.be/5Zr7K_2mnrw>
    -   Part 4: <https://youtu.be/YNluD_TNj5E>
    -   Part 5: <https://youtu.be/oGMy4FJLKy4>
-   Online Lessons
    -   <https://github.com/FRCTeam3255/FRC-Java-Tutorial>
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