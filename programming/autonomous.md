# Creating an Autonomous

Autonomous is code that is used to make the robot move by itself. 
Our autonomous mainly uses a Boilerplate to create states for the robot to follow.
We utilize the ```AutonomousStateMachine``` from ```magicbot``` to create a progression of commands for the robot to follow.
Create your autonomous file in a directory called "Autonomous" in your project.

To create a state for autonomous, you have to import the ```AutonomousStateMachine```.
You also need to import any components that you will be using from the components subdirectory.

```
python
from magicbot import AutonomousStateMachine, state
from magicbot import AutonomousStateMachine, timed_state
from components.genericdrivetrain import Drivetrain
from components.genericmanipulator import Manipulator
```
Then, you need to create the autonomous class.

```
python
class GenericAutonomous(AutonomousStateMachine):
    MODE_NAME = name # name of autonomous as seen in autonomous chooser
    DEFAULT = True # if true, this is default autonomouse mode selected
    
```

After importing, you can create your first ```state``` 
There are two types of states: ```state``` and ```timed_state```

```
python
   @timed_state(duration = 1, next_state = 'manipulate', first = True)
   def drive(self):
      pass # All of the code for this command goes here
      
   @state()
   def manipulate(self)
      pass # All of the code for this command goes here
```

There are several parameters in the state and timed_state:
1. duration in timed_state is the duration of the autonomous
2. next_state specifies the next state that is run
3. first specifies the first state that is run in autonomous
