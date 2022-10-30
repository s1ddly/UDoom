# UDoom
Doom, but compiled on ubuntu.  
Built using [this](https://www.youtube.com/watch?v=9JgQfQHHhTw) video.  
## Pre-Requisites
In order to compile doom, you will need to do the following packages installed:  
- build-essential  
- libx11-dev  
- libext-dev  
- xserver-Xephyr  
## Build Instructions
There were some issues with the stock code released for doom, I have followed the instructions in the video to make the required changes.  
### Compiling Doom
To compile Doom, it is super simple.  
1. Find a copy of the doom wad file(you can grab a copy from this [website](https://www.doomworld.com/classicdoom/info/shareware.php) right [here](http://www.doomworld.com/3ddownloads/ports/shareware_doom_iwad.zip))  
2. Place it into the linuxdoom-1.10 folder  
3. cd into the linuxdoom-1.10 folder and run the make command
4. Launch a new window using Xephyr of size 640 by 480, with 8 bits of color depth  
5. Run the binary at linuxdoom-1.10/linux/linuxxdoom passing the appropriate option to target the Xephyr display  
In practice, this looks like:  
```
cp <PATH TO YOUR WAD FILE>/DOOM1.WAD UDoom/linuxdoom-1.10/doom1.wad
cd UDoom/linuxdoom-1.10/
make
```
Now at this point, you should open another terminal window and launch the Xephyr window:  
```
Xephyr :2 -ac -screen 640x480x8
```
Return to the other terminal and run the below:  
```
./linux/linuxxdoom -2
```
Congratulations! You are now running Doom on your Ubuntu PC!  
*Note: So far, this only runs on Ubuntu 22.04.1 LTS*