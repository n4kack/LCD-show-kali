LCD driver for the Raspberry PI Installation<br>
====================================================
Update: <br>
v1.9-20181204<br>
Update to support MHS40 & MHS32<br>
Update: <br>
v1.8-20180907<br>
Update to support MHS35<br>
Update: <br>
v1.7-20180320<br>
Update to support Raspbian Version:March 2018(Release date:2018-03-13)<br>
Update: <br>
  v1.6-20170824<br>
  Update xserver to support Raspbian-2017-08-16<br>
Update: <br>
  v1.5-20170706<br>
  Update to support Raspbian-2017-07-05,Raspbian-2017-06-21<br>
Update: <br>
  v1.3-20170612<br>
  fixed to support Raspbian-2017-03-02,Raspbian-2017-04-10<br>
Update: <br>
  v1.2-20170302<br>
  Add xserver-xorg-input-evdev_1%3a2.10.3-1_armhf.deb to support Raspbian-2017-03-02<br>
Update: <br>
  v1.1-20160815<br><br>
  
1.)Step1, Install Kali for Pi <br>
====================================================
  a)Download Kali for Pi from: <br>
  https://www.offensive-security.com/kali-linux-arm-images/#1493408272250-e17e9049-9ce8
  b)Use “balenaEtcher” to prepare your SD Card with downloaded image<br>
  c)Grab a copy of the Config.txt file from the newly created boot volume of the SD card, this may come in handy later
     
2.) Step2, Clone my repo onto your pi<br>
====================================================
Use SSH to connect the raspberry pi, <br>
And Ensure that the raspberry pi is connected to the Internet before executing the following commands:
-----------------------------------------------------------------------------------------------------

```sudo rm -rf LCD-show```<br>
```git clone https://github.com/n4kack/LCD-show-kali.git```<br>
```chmod -R 755 LCD-show-kali```<br>
```cd LCD-show-kali/```<br>
  
3.)Step3, According to your LCD's type, excute:
====================================================
In case of 2.4" RPi Display(MPI2401)<br>
  ```sudo ./LCD24-show```<br><br>
In case of 2.8" RPi Display(MPI2801)<br>
  ```sudo ./LCD28-show```<br><br>
In case of 3.2" RPi Display(MPI3201)<br>
  ```sudo ./LCD32-show```<br><br>
In case of 3.5inch RPi Display(MPI3501)<br>
  ```sudo ./LCD35-show```<br><br>
In case of 3.5" HDMI Display-B(MPI3508)<br>
  ```sudo ./MPI3508-show```<br><br>
 In case of 3.2" High Speed display(MHS32)<br>
  ```sudo ./MHS32-show```<br><br>
In case of 3.5" High Speed display(MHS35)<br>
  ```sudo ./MHS35-show```<br><br>
In case of 4.0" High Speed display(MHS40)<br>
  ```sudo ./MHS40-show```<br><br>
In case of 4.0" HDMI Display(MPI4008)<br>
  ```sudo ./MPI4008-show```<br><br>
In case of 5inch HDMI Display-B(Capacitor touch)(MPI5001):<br>
  ```sudo ./MPI5001-show```<br><br>  
In case of 5inch HDMI Display(Resistance touch)(MPI5008)<br>
  ```sudo ./LCD5-show```<br><br>
In case of 7inch HDMI Display-B-800X480(MPI7001)<br>
  ```sudo ./LCD7B-show```<br><br>
In case of 7inch HDMI Display-C-1024X600(MPI7002)<br>
  ```sudo ./LCD7C-show```<br><br><br>
If you need to switch back to the traditional HDMI display<br>
  ```sudo ./LCD-hdmi```<br>
  
Cross everything and hope for the best, coz i have no idea if this will work either <br>
*SPOILER ALERT* it didn't - but all is not lost

Wait a few minutes,the system will restart automatically, 
-------------------------------------------------------------------------------
and will Kernel Panic
power down pi, remove SD card
mount sd card back to your computer
locate the boot volume of the sd card, locate the config.txt file there, 
also locate the one you copied after building the sd card (see Step 1, item c )
open both config.txt files 
copy the content from the one on your computer and paste that data above the 6 lines in the version on the sd card
save the vesion stored on the sd card 
(it should now have both sets of config info. The stuff needed for kali, and the stuff needed for the display)
eject the card, replace in Pi and boot

enjoy with your LCD.  ... and you now might need to calibrate the touch setting (but I'm no help to you here)
-------------------------------------------------------------------------------
The LCD-show.tar.gz also can be download from:
http://www.lcdwiki.com/RaspberryPi-LCD-Driver
<br><br>
