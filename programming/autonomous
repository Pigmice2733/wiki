Autonomous is code that is used to make the robot move by itself. 
Our autonomous mainly uses a Boilerplate to create states for the robot to follow.
We utilize the AutonomousStateMachine from magicbot to create a progression of commands for the robot to follow.

To create a state for autonomous, you have to import the AutonomousStateMachine.
You also need to import any components that you will be using from the components subdirectory.

```
from magicbot import AutonomousStateMachine, state
from components.genericdrivetrain import Drivetrain
from components.genericmanipulator import Manipulator
```
Then, you need to create the autonomous class.

```
class GenericAutonomous(AutonomousStateMachine):
    MODE_NAME = name // name of autonomous as seen in autonomous chooser
    DEFAULT = True // if true, this is default autonomouse mode selected
    
```

After importing, you can create your first state. 
There are two types of states: state and timedstate

```
   @timed_state(duration = 1, next_state = 'manipulate', first = True)
   def drive(self):
      pass // All of the code for this command goes here
      
   @state()
   def manipulate(self)
      pass // All of the code for this command goes here
```
