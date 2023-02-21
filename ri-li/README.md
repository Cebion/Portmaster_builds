# Ri-Li

# Source: 

https://ri-li.sourceforge.net/index.html

# Controls

DPAD - Control track switches

## Needed libraries

You have to supply following libraries in the libs folder
- SDL12.Compat libs
- libfluidsynth.so.2
- libinstpatch-1.0.so.2
- libjack.so.0
- libjbig.so.0
- liblzma.so.5
- libmad.so.0
- libmikmod.so.3
- libreadline.so.8
- libSDL_image-1.2.so.0
- libSDL_mixer-1.2.so.0
- libtiff.so.5
- libtinfo.so.6
- libwebp.so.6
- libzstd.so.1
 
## Building

```
git clone git@github.com:Cebion/Ri-Li.git
./configure 
make -j8
```
Copy folders:
- Sounds
- data

## Thanks
Special thanks to @kloptops for helping me port this game to Portmaster
with tips to compile the game on newer gcc


