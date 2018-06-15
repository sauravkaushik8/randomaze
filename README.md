# randomaze
  A Random Maze framework to build reinforcent learning players on top of.

                  Install from GitHub :  pip3 install git+git://github.com/sauravkaushik8/randomaze.git
                                                     OR 
                                Install from PyPi :  pip3 install randomaze

### Example: 

```python
>>> #Loading Maze from randomaze 
>>> from randomaze import Maze
>>>
>>> #Defining a 4X4 Maze - 1: Player, 2: Goal, 3: Pit
>>> obj = Maze(4,4)
>>> obj.print_maze()
[[1. 0. 0. 3.]
 [0. 0. 0. 0.]
 [0. 2. 0. 0.]
 [0. 0. 0. 0.]]
>>>
>>> #Playing a Random series of actions
>>> op = None
>>> while(op == None):
...     op = obj.move(take_random_action = True)
...     obj.print_maze()
...
Action:  Right
Old: 1 1
New: 2 1
[[0. 1. 0. 3.]
 [0. 0. 0. 0.]
 [0. 2. 0. 0.]
 [0. 0. 0. 0.]]
Action:  Right
Old: 2 1
New: 3 1
[[0. 0. 1. 3.]
 [0. 0. 0. 0.]
 [0. 2. 0. 0.]
 [0. 0. 0. 0.]]
Action:  Down
Old: 3 1
New: 3 2
[[0. 0. 0. 3.]
 [0. 0. 1. 0.]
 [0. 2. 0. 0.]
 [0. 0. 0. 0.]]
Action:  Up
Old: 3 2
New: 3 1
[[0. 0. 1. 3.]
 [0. 0. 0. 0.]
 [0. 2. 0. 0.]
 [0. 0. 0. 0.]]
Action:  Left
Old: 3 1
New: 2 1
[[0. 1. 0. 3.]
 [0. 0. 0. 0.]
 [0. 2. 0. 0.]
 [0. 0. 0. 0.]]
Action:  Right
Old: 2 1
New: 3 1
[[0. 0. 1. 3.]
 [0. 0. 0. 0.]
 [0. 2. 0. 0.]
 [0. 0. 0. 0.]]
Action:  Right
Old: 3 1
[[0. 0. 1. 3.]
 [0. 0. 0. 0.]
 [0. 2. 0. 0.]
 [0. 0. 0. 0.]]
>>>
>>> #Printing the Result:
>>> print(op)
Lost!
```
