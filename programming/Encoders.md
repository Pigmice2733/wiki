# Encoders


**Encoders measure how fast a motor spins.**

Which is immeasurably important, it's the reason why our robot can actually turn and still drive straight.  This is because of the fact we can precisely measure how quickly our motor is turning and what angle it's turned in which allows us to make sure we have all our wheels facing the right direction.  Without encoders our robot would easily just end up flipping over due to the fact half of the motors were facing the wrong direction. 

There's lots of different examples of encoders at work all around us, 
such as:
  * Elevators - Encoders in elevators tell the elevator's controller device its position so that it can properly align itself with the floor and open up the doors at the correct position.
  * Cranes - Some large cranes use encoders in order to collect accurate location information to know where it is.

**TL;DR:  Encoders are the reason we can tell our robot to drive at angles.**

**How do Encoders (generally) work?**

![Image of encoder](http://encoder.com/core/files/encoder/uploads/images/Encoder-exploded-COLOR-v2.jpg)

There are a lot of encoders in the world at large.  Hardware encoders are made out of a variety of different technologies and tend to vary quite a bit as do their purposes.  The encoder in the example shown above is used to detect the speed of which the motor is spinning.  This specific encoder, taken from [encoder.com](http://encoder.com/blog/company-news/what-is-an-encoder/), has a stream of light which comes from the LED and goes through the "Code Disk".  As the light goes through the "Code Disk" it becomes interrupted as the blades from the "Code Disk" block it from the "Photodetector Assembly" which detects light.  The result is a binary output of either the light being on or the light being off.  This simple value is then passed on to another device, generally called a "controller" which actually interprets the data.  Because the controller can obtain these simple values it can measure how frequently the light is being blocked from which it can determine the speed of the motor.  It can check whether or not the motor is actually running based on if there is no change in the on or off value over a long period of time.

Most optical sensors work like the one pictured above by relying on the interruption of light picked up by another sensor.

## How we use encoders

We use the *robotpy library* for interfacing to our robot's components with Python, and the library has a class interface to [the Encoder library](http://robotpy.readthedocs.io/projects/wpilib/en/latest/wpilib/Encoder.html) (yes they call it the encoder library).  Below is an example made by a user on github, [virtuald ("Dustin Spicuzza")](https://github.com/virtuald), which uses an encoder to munipulate a motor.  
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



*Sources (Read for more information):

*RobotPy documentation*
https://robotpy.readthedocs.io/en/stable/
*Furthur reading on what Encoders are*
http://encoder.com/blog/company-news/what-is-an-encoder/ 
https://en.wikipedia.org/wiki/Encoder
https://www.dacast.com/blog/software-vs-hardware-encoders-for-live-video-streams/
*





