# Blockout II

# Source: 
http://www.blockout.net/blockout2/

# Controls



## Needed libraries

You have to supply following libraries in the libs folder
- GL4ES libs
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
https://sourceforge.net/projects/blockout/
Compile Imagelib first
make -j12
scp libimagelib.a /usr/lib/aarch64-linux-gnu/
cd include/
scp CImage.h /usr/include/
cd BlockOut/
make -j12

```
Copy folders:
- images
- sounds

# Thanks


