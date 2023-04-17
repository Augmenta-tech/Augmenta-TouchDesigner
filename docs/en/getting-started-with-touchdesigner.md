# Getting started with TouchDesigner

<div>

<figure><img src=".gitbook/assets/TD_top.gif" alt=""><figcaption><p>Example project using Augmenta in TouchDesigner</p></figcaption></figure>

 

<figure><img src=".gitbook/assets/ezgif.com-video-to-gif (1).gif" alt=""><figcaption><p>Touchdesigner example in real condition</p></figcaption></figure>

</div>

### Touchdesigner

[TouchDesigner ](https://derivative.ca/)is a node based visual programming language for real time interactive multimedia content, developed by the Toronto-based company Derivative. It's been used by artists, programmers, creative coders, software designers, and performers to create performances, installations, and fixed media works.

### Video tutorial

{% embed url="https://www.youtube.com/watch?v=7YzUEzS3R2g" %}

This video shows how to open the example in TouchDesigner and how to set up Augmenta Fusion to send TUIO data to it.



## Written tutorial

Prerequisites:

* Having [TouchDesigner ](https://derivative.ca/download)installed on your computer
* Having [Augmenta simulator](https://augmenta.tech/downloads) installed on your computer

### Install

Download Touchdesigner example here

{% file src=".gitbook/assets/Augmenta-Example.toe" %}

Once TouchDesigner is open, you can see the example's processing graph with:

* An "Augmenta" box, which is the .tox that takes Augmenta inputs
* A CHOP that will contain the Augmenta scene infos (width, height, resolution)
* A DAT that will contain the detected objects data
* A SOP example using the Augmenta data
* A TOP example using the Augmenta data

The first thing you can do is to add the Augmenta tox to your saved components. Open the "Palette" panel, then in the "My Components" section create a folder (through right click). Finally drag the "Augmenta" tox on that new folder to save it. Now you can search it there if you want to start a new project.

The next step is to open Augmenta Fusion. In the "Sources" pannel, add a new generator source. This will allow you to generate points to test your interactive content. Untick the "Auto clear" option so that the points in the generator will stay. If you click somewhere while holding the ALT key in the generator source it will create a point that will stay there. You can also just click but the point will disappear as soon as you release the mouse button.

We now have to add an output in Augmenta Fusion, to send the generated data to TouchDesigner. Go to the Outputs pannel and right click in it (or click on the green "+" button) and select "TouchDesigner" > "TUIO (default)" to create a TUIO output with the TouchDesigner preset. Check which port was assigned to the output (it should default to 13000).

We can now go back to TouchDesigner to see if we receive data. Click on the "Augmenta" tox, select the "Augmenta" tab and check that the "Protocol" field is set to "TUIO" and the "OSC / TUIO port" field is the same as the output port in Augmenta Fusion.&#x20;

You should now see rendered objects in the debug view and in the different example SOP/TOPS.

## Workflow in details

Augmenta Fusion can send data to TouchDesigner through 2 protocols:

* TUIO : the preferred way, more stable and best integrated with TouchDesigner
* OSC : our own protocol, parsed in the .tox

If you have Augmenta Fusion, you should prefer using the TUIO outputs.

If you do not have access to Augmenta Fusion, you can use the [Augmenta Simulator](https://github.com/Augmenta-tech/Augmenta-Simulator) to send OSC data to the .tox.

## More ressources

### Using Notch in TouchDesigner

We also have a video tutorial on how to set up a Notch block inside TouchDesigner [here](https://youtu.be/SuFydPuyIlI).

The corresponding example files can be found [here](https://github.com/Augmenta-tech/Notch-with-Data-in-TD).

