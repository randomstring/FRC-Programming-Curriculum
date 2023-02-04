# Adding a Gyro

Here are instructions for adding a gyro to the Minibot DriveTrain subsystem.

You can look at the full Odometry cable Minibot brancth athttps://github.com/FRC-Sonic-Squirrels/MiniBot2023/tree/Odometry

1. install the vendor dependency for the NAVX gyro. The vendordep url is: https://dev.studica.com/releases/2023/NavX.json

2.  add gyro to drivetrain subsystem, this will go into the class variables (with the declarations of the motors and motor controllers).

```Java
       // The gyro sensor
       private final AHRS gyro = new AHRS(SPI.Port.kMXP);
```

3. Add the following methods for resetting the gyro and to get the current header.

```Java
  /**
   * Zeroes the heading of the robot.
   */
  public void zeroHeading() {
    gyro.reset();
  }

  /**
   * Returns the heading of the robot.
   *
   * @return the robot's heading in degrees, from 180 to 180
   */
  public double getHeading() {
    //
    return Math.IEEEremainder(gyro.getAngle(), 360) * -1.0);
  }
```

4. add a call to `zeroHeading()` to the DriveTrain subsystem initialize() to reset the gyro when the robot starts up.

