# SpaceX API wrapper in Python
<div align="center">

[![GitHub release](https://img.shields.io/github/release/phadnisvinay30/SpaceX-Python.svg)](https://github.com/Amporu/SparkVerse/releases)


### Simple and Easy API Wrapper for [r-spacex/SpaceX-API](https://github.com/r-spacex/SpaceX-API)!

<br><br>

</div>

## Documentation
This is a python simulator that is best use for autonomous driving systems based on a camera module.
<br>


## Installation
To install via `pip` use:
```sh
pip install sparkverse #Python2.x
pip3 install sparkverse #Python3.x

```
To install via running 'install.sh' script
```sh
sudo sh install.sh
```
## Basic Usage
The usage of the wrapper is very easy. It does not require any initialisation. Just import and start coding:
```python
from sparkverse.simulator import Simulator
import sparkverse.external_data as ex #contains all maps preinstalled alltoghether with the library

import cv2
Simulator.setMap(ex.LEVEL1) #set the desired map LEVEL1 to LEVEL7 or input path to image file
while(Simulator.isRunning):
  frame,map=Simulator.getCamera() #extract camera and map
  """code here"""
  concatenated=cv2.vconcat([frame,map]) #attach the map and camera frame
  Simulator.Display(concatenated)      #special display with keyboard input for easy user experience
```
