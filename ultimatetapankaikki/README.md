# Ultimate Tapan Kaikki

## Source: 
https://github.com/suomipelit/ultimatetapankaikki

## Controls

## Needed libraries

You have to supply following libraries in the libs folder
- libzstd.so.1
- libwebp.so.6
- libtiff.so.5
- libSDL2_image-2.0.so.0
- liblzma.so.5
- libjbig.so.0
 
## Building

```
git clone git@github.com:Cebion/ultimatetapankaikki.git
mkdir build && cd build 
cmake .. 
make -j8

```
Copy folders:
- WAVS
- MUSIC_OGG
- MUSIC
- LEVS
- FNTS
- EFPS

Copy files:
- PALETTE.TAB
- OPTIONS.CFG

# Thanks
- Special thanks to @kloptops for helping me debug the game

