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
Here is some Python code which illustrates the usage of encoders, here in this example we have this piece of python code
take the data from a camera and then takes the data to then display a video feed.
```python

from picamera.array import PiRGBArray
from picamera import PiCamera
import time
import cv2

# initialize the camera and grab a reference to the raw camera capture
camera = PiCamera()
camera.resolution = (640, 480)
#camera.resolution = (1920, 1080)
camera.framerate = 32
rawCapture = PiRGBArray(camera, size=(640, 480))
#rawCapture = PiRGBArray(camera, size=(1920, 1080))

# allow the camera to warmup
time.sleep(0.1)

# capture frames from the camera
for frame in camera.capture_continuous(rawCapture, format="bgr", use_video_port=True):
	# grab the raw NumPy array representing the image, then initialize the timestamp
	# and occupied/unoccupied text
	image = frame.array

	# show the frame
	cv2.imshow("Frame", image)
	key = cv2.waitKey(1) & 0xFF

	# clear the stream in preparation for the next frame
	rawCapture.truncate(0)

	# if the `q` key was pressed, break from the loop
	if key == ord("q"):
		break


```



<i>Sources (Read for more information):
http://encoder.com/blog/company-news/what-is-an-encoder/ 
https://en.wikipedia.org/wiki/Encoder
</i>



