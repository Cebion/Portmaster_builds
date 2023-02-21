# OpenTTD

# Source: 

https://github.com/OpenTTD/OpenTTD

# Controls



## Needed libraries

You have to supply following libraries in the libs folder
- liblzma.so.5
- libicuuc.so.66
- libicui18n.so.66
- libicudata.so.66
 
## Building

```
git clone https://github.com/OpenTTD/OpenTTD.git
mkdir build && cd build
cmake ..
make -j8
```
Copy folders:
- libs
- lang
- game 
- baseset
- ai

You need following files downloaded into baseset:
- opensfx-1.0.3.tar
- openmsx-0.4.2.tar
- opengfx-7.1.tar
# Thanks


