# Encoders

**Encoders measure the rotation of motors and axles.**

We primarily use encoders to make our robot drive a specific distance in **autonomous**. The encoder tells us the angle that a motor is at, and from that we can calculate the distance that the robot has driven. We also can use encoders in **swerve drive** to measure the angle each module is turned at which allows us to make sure we have all our wheels facing the right direction.

There's lots of different examples of encoders at work all around us, such as:
  - Elevators - Encoders in elevators tell the elevator's controller device its position so that it can properly align itself with the floor and open up the doors at the correct position.
  - Cranes - Some large cranes use encoders in order to collect accurate rotation information to know where it is.

**How do Encoders (generally) work?**

![Encoder Diagram](http://encoder.com/core/files/encoder/uploads/images/Encoder-exploded-COLOR-v2.jpg)
### *Diagram taken from http://encoder.com/blog/company-news/what-is-an-encoder/*

There are a lot of encoders in the world at large. Hardware encoders are made out of a variety of different technologies and tend to vary quite a bit as do their purposes. The encoder in the example shown above is used to detect the speed of which the motor is spinning. This specific encoder, taken from [encoder.com](http://encoder.com/blog/company-news/what-is-an-encoder/), has a stream of light which comes from the LED and goes through the "Code Disk". As the light goes through the "Code Disk" it becomes interrupted as the blades from the "Code Disk" block it from the "Photodetector Assembly" which detects light. The result is a binary output of either the light being on or the light being off. This simple value is then passed on to another device, generally called a "controller" which actually interprets the data. Because the controller can obtain these simple values it can measure how frequently the light is being blocked from which it can determine the speed of the motor. It can check whether or not the motor is actually running based on if there is no change in the on or off value over a long period of time.

Most optical sensors work like the one pictured above by relying on the interruption of light picked up by another sensor.

## How to program encoders

We use the [*robotpy library*](https://robotpy.readthedocs.io/en/stable/) for interfacing to our robot's components with Python, and the library has a [`Encoder` class](http://robotpy.readthedocs.io/projects/wpilib/en/latest/wpilib/Encoder.html). Below is an example made by a user on github, [@virtuald (Dustin Spicuzza)](https://github.com/virtuald), which uses an encoder to manipulate a motor. 

```python
#!/usr/bin/env python3

import wpilib

class MyRobot(wpilib.IterativeRobot):
    
    def robotInit(self):
        
        self.stick = wpilib.Joystick(0)
        self.motor = wpilib.Jaguar(0)

        self.encoder = wpilib.Encoder(0, 1)
    
    def teleopInit(self):
        pass
    
    def teleopPeriodic(self):

        v = self.stick.getX()
        encoder_value = self.encoder.get()

        # limit the motor to only travel between 0 and 180
        if encoder_value < 0:
            v = max(0, v)
        elif encoder_value > 180:
            v = min(0, v)
        
        self.motor.set(v)

if __name__ == '__main__':
    wpilib.run(MyRobot)
```

## Sources (read for more information):

- [RobotPy documentation](https://robotpy.readthedocs.io/en/stable/)
- [Encoder Products Company](http://encoder.com/blog/company-news/what-is-an-encoder/)
