# Thermomorph

## Source: 

https://github.com/rameshvarun/thermomorph

## Controls:

DPAD			= Switch Between Monitor / Corridor
A			= Flamethrower
B			= Flamethrower

## Building

```
wget https://github.com/love2d/love/releases/download/11.4/love-11.4-linux-src.tar.gz
tar xf love-11.4-linux-src.tar.gz
cd love-11.4/
./configure
LOVE_GRAPHICS_USE_OPENGLES=1 make -j12
strip src/.libs/liblove-11.4.so
scp src/.libs/liblove-11.4.so device/libs
scp src/.libs/love device/
```

## Thanks

Special thanks to: all PortMaster contributors for helping me test it!
