# Minibot Assembly
### Instructions on how to build your own mini robot!
#### How to program your minibot is on the following tutorial. 

Creating a minibot is great for testing small projects. It's an easy change to try out new parts out and costs considerably less than a larger robot. 

------------------------------
### PARTS NEEDED:

We use many parts from Sainsmart's 4WD Robot Car Chasis Kit (https://www.sainsmart.com/products/4wd-robot-car-chasis-kit), along with some of our own senors, though you can also build entirely from scratch. 
- Frame
- 4 130 DC Motors
- Pololu Motor Controller Board
![Pololu Motor Controller](/images/minibot/motor-controller.jpg)
- PCS Female Connectors (Small and Large)
![PCS Female Connector](/images/minibot/online-connector.png)
- 2 Brushed motor speed controller 
- Small Wheels 
- Raspberry Pi
- Insullated Wire 
- Heat Shrink
- Small Nuts and Bolts 
- Miniusb to Microusb connector 

### TOOLS:
- Soldering Gun and Supplies 
- Mini Screw Driver
- Heat Gun (OPTIONAL)

------------------------------

### CHASSIS:
1. Assemble your frame with the supplied little nuts and bolts

### MOTORS:
1. Stand the motor on its side with its connection points facing you. You need to solder a PCS female connector to it. The positive red wire should be soldered to the top and the negative black wire on the bottom.
![Motor Battery Wires ](/images/minibot/motor-battery-wires.jpg)

2. Take another motor and solder a yellow wire to each of the motors connectors.
![Motor Closeup View](/images/minibot/motor-closeup.jpg)

3. Line the motor up so that the PCS connector is on your the left and the motor with the yellow wires is on your right.

4. Now solder the yellow wires to the other motor, but solder to the opposite connectors. The yellow wire, for example, that's on top should be soldered to the connection on the bottom on the other motor.
![Motor Far View](/images/minibot/motor-far-view.jpg)

5. Now, attach both motors to the frame (there's two holes on each side of the motor). 

6. Repeat steps 2-5 with the remaining two motors. Use the following image as a reference for these two motors (make sure you have the two sets of motors facing the same way).
![Motor Flipped](/images/minibot/motor-flipped.jpg)

7. From a top view your motor should look like this:
![Motors Top View](/images/minibot/top-view.jpg)

### MOTOR SPEED CONTROLLERS: 
1. On the brushed motor speed controller cut the red power wire going to the battery connector, as it won't be needed.
![Motor Controller Cut Wire](/images/minibot/motor-controller-cut-wire.jpg)

2. On the brushed motor speed controller remove the large PCS female connector, from each of the two boards. 
![Brushed Motor Controller](/images/minibot/brushed-motor-controller.jpg)

3. Solder the two ends together (red to red and black to black)
![Motor Controller Soldered](/images/minibot/motor-controlled-soldered.jpg)

4. Take a PCS Female Connector and cut it so it's only an inch, and strip the ends 
![PCS Female Connector](/images/minibot/pcs-female-connector.jpg)

5. Cut a piece of heat shrink in half. Slip one half around the two positive wires and the other around the two negative wires. 
![Soldered Motor Controller with Heat Shrink](/images/minibot/soldered-motor-controller-with-heat-shrink.jpg)

6. Solder the PCS Connector to it's coorisponding color on the motor controllers
![Soldered to Connector](/images/minibot/soldered-to-connector.jpg)

7. Slip the heat shrink over the connection. Use a heat gun or your soldering gun to secure the connection
![Finished Connection](/images/minibot/soldering-done.jpg)

8. You can now connect the motor controller to the two motors through the small pcs connector. 

### POLOLU BOARD:
1. You will need to solder a small wire within the pololu board, connecting the 5V pin to the first power pin.
![Motor Controller Back View](/images/minibot/motor-controller-back.jpg)

2. Use the collection of 3 female pins on the motor controller, not the one we clipped the power wire off in step 1 of motor speed controllers, to the pololu board. You can connect it to the first column of pins on the board, that are labeled ground, 5V, and signal. It's a bit of a mess, but all the wires coming from the motor controller should be connected to another wire, except for the large pcs connector. 
![Finished Connection](/images/minibot/motor-connections.jpg)

### Battery Supply
1. You can either use a battery pack made for 6 AA batteries or you can use a 5V rechargable battery pack. You will also need a small pcs connector. 
![Battery Supplies](/images/minibot/battery-pack-unsoldered.jpg)

2. Cut a piece of heat shrink in half, and slip it over the wires coming from the battery pack. '
![Heat Shrink](/images/minibot/heat-shrink.jpg)

3. Solder the battery pack to the pcs connector and add the heat shrink over it. 
![Completed Battery](/images/minibot/battery-done.jpg)

4. You can now screw in your battery pack to the bottom of the minibot and connect it to the last big pcs connector coming from the motor controller.

### Connecting to the RaspberryPi: 
1. We will be using the raspberry pi to program our minibot. You will use the miniusb to microusb connector to connect the pololu board to the raspberry pi. 

Congratulations, you have finished a minirobot! In our following tutorial we will show you how to write and download code to make your robot move, and how to add different sensors to it! 
