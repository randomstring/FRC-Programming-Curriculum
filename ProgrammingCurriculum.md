<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#sec-1">1. Account setup</a></li>
<li><a href="#sec-2">2. Software Installation &amp; Tool Setup</a></li>
<li><a href="#sec-3">3. WPI lib</a></li>
<li><a href="#sec-4">4. PID controllers</a></li>
<li><a href="#sec-5">5. Motor Controllers and WPI built-in functions</a></li>
<li><a href="#sec-6">6. Networking Basics</a></li>
<li><a href="#sec-7">7. Basic Physics</a></li>
<li><a href="#sec-8">8. Electronics, Wiring, and Control Systems</a></li>
<li><a href="#sec-9">9. Resources</a></li>
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

# Networking Basics<a id="sec-6" name="sec-6"></a>

-   Wired vs WiFi
-   Switches, routers, Radios, Mesh Networks
-   Network wiring
-   TCP, UDP, HTTP, HTTPS
-   bandwidth, latency, packet loss
-   WiFi
    -   2.4Ghz vs 5Ghz
    -   WiFi interference

# Basic Physics<a id="sec-7" name="sec-7"></a>

-   speed, acceleration, gravity, motion
    -   newton's laws
-   force, momentum, energy
-   levers
-   Vectors
    -   adding force and motion vectors
-   Friction (?)
-   Elastic vs Inelastic collisions (?)
    -   <https://www.khanacademy.org/science/physics/linear-momentum/elastic-and-inelastic-collisions/v/elastic-and-inelastic-collisions>

# Electronics, Wiring, and Control Systems<a id="sec-8" name="sec-8"></a>

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

# Resources<a id="sec-9" name="sec-9"></a>

-   General
    -   <https://www.team254.com/resources/>
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
