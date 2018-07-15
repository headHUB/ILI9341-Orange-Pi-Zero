# ILI9341-Orange-Pi-Zero
how to run ILI9341 Orange Pi Zero

You must download linux image with enabled SPI (Armbian has not enabled SPI), 
so download RETRORANGEPI image:
http://www.retrorangepi.org/download/

default login:
--------------
login: root
password: orangepi


My config:
--------------
in
/etc/modules-load.d/fbtft.conf
fbtft_device

in
/etc/modprobe.d/fbtft.conf 
options fbtft_device custom name=fb_ili9341 gpios=reset:1,dc:0,led:3 speed=48000000 fps=25 rotate=90 busnum=1 bgr=1 txbuflen=65536

or just upload content of repository
--------------

