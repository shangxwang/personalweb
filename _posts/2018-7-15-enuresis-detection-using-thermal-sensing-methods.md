---
title: Enuresis Detection Using Thermal Sensing Methods
date: 2018-7-15
comment: false
---
This is my undergraduate research project: to develop a bed-based toolset to monitor a disabled child’s health and activity during the night. My role in this project is to design an anutomate system using thermal sensing methods (theromocouple and digital temperature sensor) for enuresis detection. Sleep quality in children with severe disabilities is correlated to their daytime wellness and ability to learn. Enuresis, or bed wetting, can significantly affect sleep quality. Such an automated system would eliminate the need to conduct manual bed checks several times during the night for each child. 


## Workflow 
1. 16 thermocouples are placed underneath the mattress and connected the the NI9213 module for temperature acquisition. 

2. Bedwetting detection is automated through Labview and Ubidots. When bed wetting occurs, it will trigger the alarm in Labview and as sending a text message to smart phone through Ubidots.
<img src="https://github.com/shangxwang/shangxwang.github.io/blob/master/github/scattervariance.png?raw=true"/>

3. Digital temperature sensor (TMP107) was later used to replace thermocouple to promte the system go wireless. This involves PCB layout design and wireless communication via bluetooth.
<img src="https://github.com/shangxwang/shangxwang.github.io/blob/master/github/TMP107.png?raw=true"/>



