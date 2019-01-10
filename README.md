# Step by step setup the touch screen on F6

## 1.wiring diagram

![1547105450498](images\1547105450498.png)

As you can see, this is a serial screen, the hardware is connected to F6 by serial port 2.
On the F6, there are two interfaces that can be connected to the touch screen. By default, the FPC connector is used.

![1547106602098](images\1547106602098.png)

note：If you want to connect via J1, please note that the TX and RX of the serial port need to be crossed.

![1547107811426](images\1547107811426.png)

The screen does not have an SD card socket for printing, so we have gave an SD card module for free.

![1547107139417](images\1547107139417.png)

wiring diagram:



## 2.Software setup 

In order to use this serial screen, you need to configure marlin and add some codes.

We have uploaded the configured marlin source code to github: https://github.com/FYSETC/Marlin-F6

(If you just want to test the screen, you can download the .hex file directly and uploade it to F6 with xloader. https://github.com/FYSETC/Marlin-F6/blob/master/Marlin/Marlin.F6.TFT.hex)

The screen of the shipment we have burned the firmware, if you want to make some changes, here is the screen firmware : https://github.com/FYSETC/FYSTLCD.

1.uploade the firmware to F6

2.connect the touch screen to F6 by the FPC cable

3.connect the SD module to F6 by the gray cable

4.power up the F6 with 12V or 24V power supply ,(You can't just use the USB to power the board, if you do

 that, the screen will be powerless and display white screen.) 

## 3.Customize your own UI 

We created the UI using Adobe xDesign, and convert each one pic into a 24-bit BMP image，Import these images into the IDE of the screen,  and write the screen firmware .
Inside the screen firmware on github, you can see these .bmp images. If you want to change the color, you only need to replace these images.

the .XD file slao on the github：

