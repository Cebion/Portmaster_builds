# Abe's Amazing Adventure

# Source: 

https://abe.sourceforge.net/

# Controls



## Needed libraries

- You have to supply following libraries in the libs folder
	- SDL1.2-Compat library libSDL-1.2.so
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
wget https://sourceforge.net/projects/abe/files/abe/abe-1.1/abe-1.1.tar.gz
./autogen.sh
./configure
make -j8
```
Copy folders:
images
maps
savegame
sounds

# Thanks


