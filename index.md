---
layout: default
---

# Comparing Fixed and Variable Segment Durations for Adaptive Video Streaming

*Susanna Schwarzmann, Nick Hainke, TU Berlin*  
*Thomas Zinner, NTNU - Norwegian University of Science and Technology*  
*Christian Sieber, TU Munich*  
*Werner Robitza, Alexander Raake, TU Ilmenau*  

A holistic comparison of fixed and variable segment durations within the adaptive video streaming eco-system. We provide a large-scale investigation of video encoding efficiency to quantify the savings with respect to bitrate and storage for variable segment durations. Moreover, measurements with a variety of different bandwidth configurations are performed in a testbed to evaluate the impact of segment duration variability on the performance of the dash.js reference implementation.

## Video Encoding

![Encoding](figures/frames.png)

HAS services typically utilize a fixed segment duration. Due to the content-agnostic placement of I-frames at the beginning of each segment, additional encoding overhead is introduced. In order to mitigate this overhead, variable segment durations, which take scene-cuts during the video seg- mentation process into account, have been proposed recently. As a consequence, a lower number of I-frames is needed as compared to fixed segment durations, thus achieving a lower video bitrate without quality degradation.

### Encoding

Detailed Instructions:
* [Creating Job Files For Encoding Container](https://github.com/fg-inet/video-scripts/blob/master/README.md).
* [Usage Of Docker Encoding Container](https://github.com/fg-inet/docker-video-encoding/blob/master/README.md)

## DASH Steaming

![DASH Stream Testbed](https://raw.githubusercontent.com/fg-inet/DASH-streaming-setup/master/images/setup.JPG)

## Overview 
The setup consists of three virtual machines. 
   * The __server__, which hosts the video content 
   * The __netem__, which throttles the bandwidth, as for example defined by traces 
   * The __client__, which uses DASH.js to stream the video

### Installation Instructions
Detailed Installation Instructions are listed [here](https://github.com/fg-inet/DASH-streaming-setup/blob/master/README.md).
