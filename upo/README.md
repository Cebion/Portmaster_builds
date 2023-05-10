# Upo

## Source: 

https://github.com/TheJeme/upo

## Controls:

Left Stick			= Avoid Obstacles
A				= Left Mouseclick
R1				= Left Mouseclick

## Building

```
wget https://github.com/love2d/love/releases/download/11.4/love-11.4-linux-src.tar.gz
tar xf love-11.4-linux-src.tar.gz
cd love-11.4/
./configure
make -j12
strip src/.libs/liblove-11.4.so
scp src/.libs/liblove-11.4.so device/libs
scp src/.libs/love device/
```

## Thanks

Special thanks to: all PortMaster contributors for helping me test it!
