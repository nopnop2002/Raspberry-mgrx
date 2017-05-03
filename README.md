# mgrx_rpi
2D graphics library for FrameBuffer

MGRX is a 2D graphics library derived from the GRX library.   
GRX was originaly written by Csaba Biegl.   
MGRX was originaly written by M.Alvarez.   

This is for RaspberryPi.   

---

Requirements   

sudo apt-get install libjpeg-dev

---


Install   

git clone https://github.com/nopnop2002/mgrx_rpi   
cd $HOME\mgrx100_rpi/   
make -f makefile.lnx libs   
sudo make -f makefile.lnx install   
make -f makefile.lnx   

---

Demonstration   

export MGRXDRV="linuxfb gw <width> gh <height> nc <colors>"   
<width> is width of FrameBuffer.   
<height> is height of FrameBuffer.   
You can get these by the following command.   
fbset -i -fb <device of framebuffer>   .

export FRAMEBUFFER=<device of framebuffer>   

If you have 320x240 TFT, it'll be as follows.   

export MGRXDRV="linuxfb gw 320 gh 240 nc 64k"   
export FRAMEBUFFER=/dev/fb1   
cd $HOME/mgrx100_rpi/test   
./demomgrx   

