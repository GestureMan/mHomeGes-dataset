# mHomeGes-dataset


This dataset contains the gesture samples used in mHomeGes.
It is collected by millimeter-wave (mmWave) FMCW radar and has proven to have a satisfactory classification accuracy for 10 arm gestures within 1.2 meters to 3 meters. 

## Gesture Space

In this dataset, we define 10 arm gestures for recognition to facilitate the human-computer interaction in smart home scenarios.
Surpassing the whole-body activities, arm gestures can be performed frequently, especially for the senior.
In addition to these predefined gestures, the dataset also archives random actions at random positions in daily life, which will help the anti-interference ability of gesture recognition via the proposed methods in mHomeGes.
Specifically, the ten gestures are as follows: 

<img src="https://raw.githubusercontent.com/GestureMan/mHomeGes-dataset/master/fig/gesturePic.png" width="500"  alt="gesturePic"/><br/>

## Collection Settings

We set 13 discrete positions as anchor points, so as to give mHomeGes the ability to serve the gestures from random positions:


<img src="https://raw.githubusercontent.com/GestureMan/mHomeGes-dataset/master/fig/anchor.png" width="550"  alt="anchor"/><br/>



## Directory Structure

**Predefined gestures**: We set the gesture samples into the form of ``*distance*/*userNumber*/*gesture*''.

**Random actions**: We leave this part of data into a single folder ``dailyRandom''.

**Other documents**: We provide a gesture instruction in the home directory which describes how to perform each arm gesture in details. Note that however, the volunteers learn the gestures only by watching how we perform them.


## Data Structure

**Data structure**: The data structure of each gesture is 7* n, where n is various with frames and 7 are 'frame id’, 'detected points in each frame’, 'x coordinate of each point’, 'y coordinate of each point’, 'z coordinate of each point’, 'velocity of each point’ and 'reflection intensity of each point’. In each '.csv’ file, the gestures can be divided by a large interval between each two of them.

**Notice**: In each CSV file, the lost frames are the delimiters among different actions of the same gesture. We asked the volunteers to hold still for about 1 second after each action so as to generate empty frames, and then use these frames as delimiters between each action.

## Parameters of mmWave Radar

In this mmWave gesture dataset, we utilize the TI-IWR1443 single-chip 76-GHz to 81-GHz mmWave sensor evaluation module.

| Radar parameters | vaule |
| ----- | ----- |
| Rx channels | 4 |
| Tx channels | 3 |
| chirp cycle time | 158 μs |
| ADC sampling rate | 7.5 kHz |
| Rx gain | 42 dB |
| frame periodicity | 100 ms |
| dynamic point detection | CFAR-CA |
| point energy threshold | 1130 dB |
