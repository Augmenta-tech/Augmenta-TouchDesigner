Augmenta for Touch Designer
=======================

A TouchDesigner Augmenta TOX created by [Gamgie](http://www.gamgie.com) and [Théoriz](http://www.theoriz.com/en/).

TOX Explanation
-------------------------------------
This Tox help you to receive and use Augmenta data.
It has 3 outputs : 
- a CHOP : containing the scene parameter.
- a DAT : containing the table updated with all person detected by the system. Please refer below for parameter explanation.
- a TOP : containing a debug view similar to Augmenta simulator.

How to use
-------------------------------------
If you don't have access to Augmenta system, you can test your creation with the [simulator](https://github.com/Theoriz/Augmenta-Simulator/releases).
Check if your OSC output port in the simulator is the same as the augmenta TOX.
You should see now the render output view moving according to the simulator data.

Data
-------------------------------------
```
* Augmenta OSC Protocol :

  /au/personEntered   args0 arg1 ... argn
  /au/personWillLeave args0 arg1 ... argn
  /au/personUpdated   args0 arg1 ... argn

  where args are :


  0: pid (int)                        // Personal ID ex : 42th person to enter stage has pid=42
  1: oid (int)                        // Ordered ID ex : if 3 person on stage, 43th person might have oid=2
  2: age (int)                        // Time on stage (in frame number)
  3: centroid.x (float 0:1)           // Position projected to the ground
  4: centroid.y (float 0:1)               
  5: velocity.x (float -1:1)           // Speed and direction vector
  6: velocity.y (float -1:1)
  7: depth (float 0:1)                // Distance to sensor (in m) (not implemented)
  8: boundingRect.x (float 0:1)       // Top view bounding box
  9: boundingRect.y (float 0:1)
  10: boundingRect.width (float 0:1)
  11: boundingRect.height (float 0:1)
  12: highest.x (float 0:1)           // Highest point placement
  13: highest.y (float 0:1)
  14: highest.z (float 0:1)           // Height of the person

  /au/scene   args0 arg1 ... argn

  0: currentTime (int)                // Time (in frame number)
  1: percentCovered (float 0:1)       // Percent covered
  2: numPeople (int)                  // Number of person
  3: averageMotion.x (float 0:1)          // Average motion
  4: averageMotion.y (float 0:1)
  5: scene.width (int)                // Scene size
  6: scene.height (int)
  7: scene.depth (int)

```


Documentation
-------------

https://github.com/Theoriz/Augmenta/wiki

Version
-------------
TouchDesigner 2020.20620
