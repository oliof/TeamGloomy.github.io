---
title: Connecting Neopixels to a Fly-RRF-36
tags: []
keywords: 
last_updated: 12/06/2023
summary: "How to connect Neopixels to a Fly-RRF-36"
sidebar: mydoc_sidebar
permalink: fly_rrf_36_neopixels.html
folder: mydoc
comments: false
toc: false
datatable: true
---

## Overview

The Fly-RRF-36 has support for connecting Neopixels using the header called "rgbled" (GPIO26).  

### Configuration

The Neopixels should be configured in config.g using M950 as detailed [here](https://docs.duet3d.com/en/User_manual/Reference/Gcodes#m950-create-heater-fan-spindle-or-gpioservo-pin).  
For example, using the default toolboard address of 124 with RGBW Neopixels   
```
M950 C"124.rgbled" E0 T2
```

[M150](https://docs.duet3d.com/en/User_manual/Reference/Gcodes#m150-set-led-colours) can then be used to set the colours and brightness.  
For example, the below example will set 3 RGBw neopixels to white.  
```
M150 E0 R0 B0 U0 W255 S3 F0
```