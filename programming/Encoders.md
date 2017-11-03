<b>Ever been on a website written in another language and had to utilize google translate to gain some 
semblance of recognition as to what it was you were looking at?</b>
Encoders work in a similar fashion to Google Translate, of course instead of translating languages it merely translates
given data into another format.

There's lots of different examples of encoders at work all around us, such as:
  * Elevators - Encoders in elevators tell the elevator's controller device its position so that it can properly align itself with the floor and open up the doors
  at the correct position.
  * Cranes - Some large cranes use encoders in order to collect accurate location information to know where it is.
  * Computer Microphones - Encoders are used to convert those signals your microphone picks up into actual data that your computer can understand!
  
Encoders are the reason our robot can use a camera for visual recognition or record it's speed, or know when it's hit a brick wall.

<b>TL;DR:  Encoders are the duct tape which binds our data together.</b>

<b>How do Encoders work?</b>

<img src="http://encoder.com/core/files/encoder/uploads/images/Encoder-exploded-COLOR-v2.jpg"></img>

Encoders are made out of a variety of different technologies and tend to vary quite a bit.  The example shown above, taken from
encoder.com (see sources for link), has a stream of light which comes from the LED and goes through the "Code Disk".  As the light goes
through the "Code Disk" it becomes interrupted as the blades from the "Code Disk" block it from the "Photodetector Assembly" which detects light.  
The result is a binary output of either the light being on and the light being off.  This simple value is then passed to another device,
generally called a "controller" which actually interprets the data.

Most optical sensors work like the one pictured above by relying on the interruption of light picked up by another sensor.

<b> How we use encoders! </b><br>
Here is an example of encoders in python:

```python
# Set current position to zero
        self._reset_encoder_position()

        self.profile_executor = ProfileExecutor(
            coefs, motion_profile,
            lambda: self._get_encoder_position() / 1023,
            lambda output: self.forward_at(-output), 0.08)
    def _reset_encoder_position(self):
        self.fl_motor.setEncPosition(0)

    def _get_encoder_position(self):
        return -self.fl_motor.getPosition()



```



<i>Sources (Read for more information):
http://encoder.com/blog/company-news/what-is-an-encoder/ 
https://en.wikipedia.org/wiki/Encoder
</i>



