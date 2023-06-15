# Readme.md

### Augmenta for Touch Designer

A [TouchDesigner](https://derivative.ca/) Augmenta plugin created by [Gamgie](http://www.gamgie.com/) and [THEORIZ](http://www.theoriz.com/en/).

### Youtube tutorial

[https://www.youtube.com/watch?v=7YzUEzS3R2g](https://www.youtube.com/watch?v=7YzUEzS3R2g)

### Scene examples

#### 0 - SOP

This example uses SOP and particles

[![TD-SOP](https://user-images.githubusercontent.com/64955193/135990922-5dede4f0-ff97-479e-921b-e6aef9efb53b.gif)](https://user-images.githubusercontent.com/64955193/135990922-5dede4f0-ff97-479e-921b-e6aef9efb53b.gif)

#### 1 - TOP

This example uses TOP and reaction diffusion

[![TopTD2 0](https://user-images.githubusercontent.com/64955193/136021020-8ad71680-81fa-4254-876b-115b768685d5.gif)](https://user-images.githubusercontent.com/64955193/136021020-8ad71680-81fa-4254-876b-115b768685d5.gif)

### How to install

In your computer, go to the folder : `C:\Program Files\Derivative\TouchDesignerXXX\Samples\COMP`

Create an Augmenta folder

Copy the _augmenta.tox_ file to this folder

### How to use

In Touch designer, open _Palette Browser_ (Ctrl+B)

At the top, under Derivative category, you should see an Augmenta folder.

Drag and drop the augmenta TOX in your project

### How to test

**OSCV3**

Open Augmenta Fusion, add a generator source, then a OSCV3 output for Touch Designer.

Check that the output port in Fusion is the same as the OSCV3 port set in the Augmenta TOX.

Place a generated point by holding "alt" key while clicking in the source (this way it will stay after releasing the mouse). Then look in TouchDesigner, you should see a renderepoint at the corresponding position.

### TOX Explanation

This Tox help you to receive and use Augmenta data. It has 3 outputs :

* a CHOP : containing the scene parameter.
* a CHOP : containing a transform array for Notch
* a DAT : containing the table updated with all person detected by the system. Please refer below for parameter explanation.
* a TOP : containing a debug view similar to Augmenta simulator.

### With [Notch](https://www.notch.one/)

Example with a Notch block and TUIO/OSC data in Touch Designer

[https://github.com/Augmenta-tech/Notch-with-Data-in-TD](https://github.com/Augmenta-tech/Notch-with-Data-in-TD)

### Data

[https://github.com/Augmenta-tech/Augmenta/wiki/Data](https://github.com/Augmenta-tech/Augmenta/wiki/Data)

### Doc

[https://github.com/Augmenta-tech/Augmenta/wiki](https://github.com/Augmenta-tech/Augmenta/wiki)

### Version

TouchDesigner 2020.42700
