# ILI9341-Orange-Pi-Zero
how to run ILI9341 Orange Pi Zero

You must download linux image with enabled SPI (Armbian has not enabled SPI), 
so download RETRORANGEPI image:
http://www.retrorangepi.org/download/

default login:
--------------
login: root<br/>
password: orangepi<br/>

connection:<br/>
--------------
![alt text](https://raw.githubusercontent.com/Nathalis/ILI9341-Orange-Pi-Zero/master/RPIZERO-28inch_ILI9341.png)


My config:
--------------
in<br/>
/etc/modules-load.d/fbtft.conf<br/>
fbtft_device<br/>

in<br/>
/etc/modprobe.d/fbtft.conf<br/>
options fbtft_device custom name=fb_ili9341 gpios=reset:1,dc:0,led:3 speed=48000000 fps=25 rotate=90 busnum=1 bgr=1 txbuflen=65536<br/>

and you need run at startup:
--------------
con2fbmap 1 8
 

or just upload content of repository
--------------

and install and run this script:
--------------
chmod +x /etc/init.d/LCD.sh
update-rc.d LCD.sh defaults



