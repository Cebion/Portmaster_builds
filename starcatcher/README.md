# Starcatcher

## Source: 

https://github.com/Escada-Games/starcatcher

## Controls:

A			= Jump
B			= Jump
X			= Jump

## Building

```
wget https://downloads.tuxfamily.org/godotengine/3.5/godot-3.5-stable.tar.xz
tar xf godot-3.5-stable.tar.xz
cd godot-3.5-stable/platform
git clone https://github.com/Cebion/frt.git
cd ../
scons platform=frt tools=no target=release use_llvm=yes module_webm_enabled=no -j12
strip bin/godot.frt.opt.llvm
```
## Copy folders:


## Thanks
Special thanks to: kloptops, and all PortMaster contributors for helping me test it!
