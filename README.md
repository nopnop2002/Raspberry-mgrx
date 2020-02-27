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

# Requirements

sudo apt-get install libjpeg-dev libpng-dev

---

# Install

git clone https://github.com/nopnop2002/Raspberry-mgrx
cd Raspberry-mgrx
make -f makefile.lnx libs
sudo make -f makefile.lnx install
make -f makefile.lnx test

---

# Demonstration

export MGRXDRV="linuxfb gw &lt;width&gt; gh &lt;height&gt; nc &lt;colors&gt;"   
&lt;width&gt; is width of FrameBuffer.   
&lt;height&gt; is height of FrameBuffer.   
Values for nc can be 2, 16, 256, 64K or 16M.   
You can get these by the following command.   
fbset -i -fb &lt;device of framebuffer&gt;   

export FRAMEBUFFER=&lt;device of framebuffer&gt;   
If you have 320x240 TFT module like ILI9341, it'll be as follows.   

&lt;Case of RPi&gt;   
export MGRXDRV="linuxfb gw 320 gh 240 nc 64k"   
export FRAMEBUFFER=/dev/fb1   
cd $HOME/mgrx_rpi/test   
./demomgrx   

&lt;Case of OPi&gt;   
export MGRXDRV="linuxfb gw 320 gh 240 nc 64k"   
export FRAMEBUFFER=/dev/fb8   
cd $HOME/mgrx_rpi/test   
./demomgrx   

---

# Operation

When the item is chosen by an arrow key and ENTER is pushed, demonstration starts.   
demomgrx is a simple launcher program.   
It's possible to start each demonstration program directly by a command line.   

![main1](https://cloud.githubusercontent.com/assets/6020549/25655340/834fa7b0-302f-11e7-943b-1d80b255a9d3.png)

![main2](https://cloud.githubusercontent.com/assets/6020549/25655348/8861486c-302f-11e7-87bd-e32a518ed616.png)

![main3](https://cloud.githubusercontent.com/assets/6020549/25655353/8bb1c604-302f-11e7-8177-bc02b774a55d.png)


---

# Programmer's manual

<http://www.fgrim.com/mgrx/mgrx10pm.htm>   
