Note: this was for testing purposes as installing this for the 64bit version of Kali 2019.4 (for RPi) resulted in kernel panics, 
remains largely unchanged from github.com/lcdwiki/LCD-show-kali
aside from attempt at getting the script to use a different version of the config.txt file as a base and the instructions given below


LCD driver for the Raspberry PI Installation<br>
====================================================
Update: <br>
v1.9-20181204<br>
As Per github.com/lcdwiki/LCD-show-kali<br>
  
1.) Step 1, Install Kali for Pi <br>
====================================================
  a)Download Kali for Pi from: <br>
  https://www.offensive-security.com/kali-linux-arm-images/#1493408272250-e17e9049-9ce8 <br>
  b)Use “balenaEtcher” to prepare your SD Card with downloaded image <br>
  c)Grab a copy of the Config.txt file from the newly created boot volume of the SD card, this may come in handy later <br>
     
2.) Step 2, Clone repo onto your pi<br>
====================================================
Use SSH to connect the raspberry pi, or plug in a HDMI screen <br>
And Ensure that the raspberry pi is connected to the Internet before executing the following commands:
-----------------------------------------------------------------------------------------------------

```sudo rm -rf LCD-show-kali``` (only need to run this if you have an existing LCD-show-kali folder)<br>
```git clone https://github.com/n4kack/LCD-show-kali.git```<br>
```chmod -R 755 LCD-show-kali```<br>
```cd LCD-show-kali/```<br>
  
3.) Step 3, According to your LCD's type, excute:
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
...and will Kernel Panic
1. power down pi, remove SD card
2. mount sd card back to your computer
3. locate the boot volume of the sd card, locate the config.txt file there, 
4. also locate the one you copied after building the sd card (see Step 1, item c )
5. open both config.txt files 
6. copy the content from the one on your computer and paste that data above the 6 lines in the version on the sd card
save the vesion stored on the sd card 
(it should now have both sets of config info. The stuff needed for kali, and the stuff needed for the display)
7. eject the card, replace in Pi and boot

enjoy with your LCD.  ... and you now might need to calibrate the touch setting (but I'm no help to you here)
-------------------------------------------------------------------------------
The LCD-show.tar.gz also can be download from:
http://www.lcdwiki.com/RaspberryPi-LCD-Driver
<br><br>
