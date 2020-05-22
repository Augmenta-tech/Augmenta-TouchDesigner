Augmenta for Touch Designer
============================

A [TouchDesigner](https://derivative.ca/) Augmenta plugin created by [Gamgie](http://www.gamgie.com) and [THEORIZ](http://www.theoriz.com/en/).

How to install
-------------------------------------

In your computer, go to the folder : `C:\Program Files\Derivative\TouchDesignerXXX\Samples\COMP`

Create an Augmenta folder

Copy the *augmenta.tox* file to this folder

How to use
-------------------------------------
In Touch designer, open *Palette Browser* (Alt+l)

At the top, under Derivative category, you should see an Augmenta folder.

Drag and drop the augmenta TOX in your project

How to test
------------------------------------
Download the Augmenta [simulator](https://github.com/Theoriz/Augmenta-Simulator/releases).

Check if your OSC output port in the simulator is the same as the OSC input port of the Augmenta TOX.

You should see now the render output view moving according to the simulator data.

An example file is provided to see it in action. 

TOX Explanation
-------------------------------------
This Tox help you to receive and use Augmenta data.
It has 3 outputs : 
- a CHOP : containing the scene parameter.
- a DAT : containing the table updated with all person detected by the system. Please refer below for parameter explanation.
- a TOP : containing a debug view similar to Augmenta simulator.


Data
-------------------------------------
https://github.com/Theoriz/Augmenta/wiki#data

Documentation
-------------
https://github.com/Theoriz/Augmenta/wiki

Version
-------------
TouchDesigner 2020.20620
