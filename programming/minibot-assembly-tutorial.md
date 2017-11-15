Creating a minibot is great for testing small projects. It's an easy change to try out new parts out and costs considerably less than a larger robot. 

This is a tutorial on how to assemble one of your own. How to program your minibot is on the following wiki page.
------------------------------
PARTS NEEDED:

We use many parts from Sainsmart's 4WD Robot Car Chasis Kit (https://www.sainsmart.com/products/4wd-robot-car-chasis-kit), along with our own. Though you can also build entirely from scratch. 
- Frame
- 4 X 130 DC Motors
- Pololu Motor Controller Board
![Pololu Motor Controller](/images/motor-controller.jpg)
- PCS Female Connectors (Small and Large)
![PCS Female Connector](/images/online-connector.png)
- 2 X Brushed motor speed controller 
- Small Wheels 
- Raspberry Pi (a seperate wiki page shows how to program the minibot)
- Insullated Wire 
- Heat Shrink
- Small Nuts and Bolts 

TOOLS:
- Soldering Supplies 
- Mini Screw Drivers
- Heat Gun (OPTIONAL)

------------------------------

CHASSIS:
1. Assemble your frame with little nuts and bolts 

MOTORS: 
1. If you stand the motor on it's side, with it's connector points facing towards you, you need to solder a PCS Female Connector to it. The positive red side should be soldered to the top and the negative red side on the bottom.
![Motor Battery Wires ](/images/motor-battery-wires.jpg)

2. Take another motor and solder a yellow wire to each of the motors connector.
![Motor Closeup View](/images/motor-closeup.jpg)

3. Line the motor up so you have your motor with the pcs connector on the left and the motor with just regular yellow wires on the right.

4. Now solder the yellow wires to the other motor, but solder to the opposite connector. The red wire that's on top should be soldered to the connector on the bottom, and visa vera for the negitive. Your wires should be criss crossed with the pcs connector coming out.
![Motor Far View](/images/motor-far-view.jpg)

5. You can now attach both motors to the frame. 

6. Repeat steps 2-6 with the other two motors. When you attached the last two motors in, remember to attach them as a reflection of the last two. 

POLOLU BOARD:
1. You will need to solder a small wire within the pololu board, connecting the 5V pin to the first power pin
![Motor Controller Back View](/images/motor-controller-back.jpg)

MOTOR SPEED CONTROLLERS: 
1. On the brushed motor speed controller cut the red power wire going to the battery connector, as it won't be needed
![Motor Controller Cut Wire](/images/motor-controller-cut-wire.jpg)

2. On the brushed motor speed controller remove the large pcs female connector, from each of the two boards. 
![Brushed Motor Controller](/images/brushed-motor-controller.jpg)

3. Solder the two ends together (red to red and black to black)
![Motor Controller Soldered](/images/motor-controlled-soldered.jpg)

4. Take a PCS Female Connector and cut it so it's only an inch, and strip the ends 
![PCS Female Connector](/images/pcs-female-connector.jpg)

5. Cut a piece of heat shrink in half. Slip one half around the two positive wires and the other around the two negative wires. 
![Soldered Motor Controller with Heat Shrink](/images/soldered-motor-controller-with-heat-shrink.jpg)

6. Solder the PCS Connector to it's coorisponding color on the motor controllers
![Soldered to Connector](/images/soldered-to-connector.jpg)

7. Slip the heat shrink over the connection. Use a heat gun or your soldering gun to secure the connection
![Finished Connection](/images/soldering-done.jpg)
