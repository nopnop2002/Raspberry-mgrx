# Raspberry-mgrx
2D graphics library for FrameBuffer

MGRX is a 2D graphics library derived from the GRX library.   
GRX was originaly written by Csaba Biegl.   
<http://grx.gnu.de/>   
MGRX was originaly written by M.Alvarez.   
<http://www.fgrim.com/mgrx/>   

This was transplanted for RaspberryPi & OrangePi.   
I tested by the following environment.   
Raspberry Pi + ILI9341 SPI TFT.    
OrangePi PC + ILI9325 Parallel TFT.   

---

# Install
```
sudo apt-get install libjpeg-dev libpng-dev
git clone https://github.com/nopnop2002/Raspberry-mgrx
cd Raspberry-mgrx
make -f makefile.lnx libs
sudo make -f makefile.lnx install
make -f makefile.lnx test
```

---

# Demonstration
```
$ export MGRXDRV="linuxfb gw <width> gh <height> nc <colors>"
<width> is width of FrameBuffer.
<height> is height of FrameBuffer.
Values for nc can be 2, 16, 256, 64K or 16M.

You can get these by the following command.
$ fbset -i -fb <device of framebuffer>

$ export FRAMEBUFFER=<device of framebuffer>
If you have 320x240 TFT module like ILI9341, it'll be as follows.
```

- Case of RPi
```
$ export MGRXDRV="linuxfb gw 320 gh 240 nc 64k"   
$ export FRAMEBUFFER=/dev/fb1   
$ cd $HOME/mgrx_rpi/test   
$ ./demomgrx   
```

- Case of OPi
```
$ export MGRXDRV="linuxfb gw 320 gh 240 nc 64k"   
$ export FRAMEBUFFER=/dev/fb8   
$ cd $HOME/mgrx_rpi/test   
$ ./demomgrx   
```

---

# Operation

When the item is chosen by an arrow key and ENTER is pushed, demonstration starts.   
demomgrx is a simple launcher program.   
It's possible to start each demonstration program directly by a command line.   

![main1](https://user-images.githubusercontent.com/6020549/234507732-61dbce20-df70-40a7-be90-175ff88a314d.png)   
![main2](https://user-images.githubusercontent.com/6020549/234507739-ec4e9d01-2f4c-4e3a-abed-bcc233aff741.png)   
![main3](https://user-images.githubusercontent.com/6020549/234507741-9d380983-1992-4cd4-8aa5-0d94843d781b.png)   

---

# Programmer's manual

<http://www.fgrim.com/mgrx/mgrx10pm.htm>   
