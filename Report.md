# Fall 2021 Senior Design Hardware Miniproject - Report

*Team 21: Ashley Chong and Daniel Kao*

## Wifi Data Plots

We measured the traffic congestion patterns on the nearby street in Allston using the Raspberry Pi as a wireless sensor. The data was collected by running [wifi_scan.py](https://github.com/BostonUniversitySeniorDesign/2021-hardware-miniproj/blob/main/wifi_scan.py), which created .json files to log any wifi/ wireless activity. The data was collected in 3 trials and plotted via [wifi_plot.py](https://github.com/BostonUniversitySeniorDesign/2021-hardware-miniproj/blob/main/wifi_plot.py):

### Data Plot 1

![Wifi Data Plot 1](https://github.com/ashleychong1/senior-design-hw-miniproject-team-21/blob/main/Figure_1.png)

### Data Plot 2

![Wifi Data Plot 2](https://github.com/ashleychong1/senior-design-hw-miniproject-team-21/blob/main/Figure_2.png)

### Data Plot 3

![Wifi Data Plot 3](https://github.com/ashleychong1/senior-design-hw-miniproject-team-21/blob/main/Figure_3.png)

The data we collected was from an off-campus apartment in Allston, near a window that faces the nearby street. All three wifi scan trials showed differing levels of wireless activity in the area, with data plot 3 recording the least amount of activity and data plot 1 being recording the most. The data trends in each plots reflect the time of day we measured the data, showing more interactions earlier in the day than later. The plots show similar trends in their drops and peaks. This could show an average number of devices people carry as they walk up and down the street. The matching trend in a plot may show one person walking in and out of the the range, since they carry the same number of wifi connections. A good use case for the Raspberry Pi wifi scan could be to measure the traffic congestion or general traffic conditions at a certain time of the day in order to avoid large crowds when leaving the house.

The main difficulty we faced was figuring out how to copy the JSON files that were created onto our personal laptops. Since the Raspberry Pi only has an older version of the Python library, we needed to run wifi_plot.py on a separate MacBook. We tried many times to copy the file using SCP, which required the MacBook to be connected to the Raspberry Pi. Despite many attempts at connecting the laptop to the Pi, both via wireless connection and via Ethernet cable, we still encountered errors when running the command `scp pi@raspberrypi.local:~/data/*.json .` in the laptop's CLI. In the end, we just decided to send a copy of the JSON files via email, and the rest of the project worked well after that.
