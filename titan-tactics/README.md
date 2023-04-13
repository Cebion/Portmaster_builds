# Titan Tactics

## Source: 

https://gitlab.com/team-potato/titan_tactics/

## Controls:

A			= Accept
B			= Cancel
X			= Menu / End Turn
Y			= Swap Character
L1 / R1			= Rotate Camera
DPAD		        = Move Cursor
Enter			= Enter / Pause

## Building

```
wget https://downloads.tuxfamily.org/godotengine/3.2.3/godot-3.2.3-stable.tar.xz
tar xf godot-3.2.3-stable.tar.xz
cd godot-3.2.3-stable/platform
git clone https://github.com/Cebion/frt.git
cd ../
scons platform=frt tools=no target=release use_llvm=yes module_webm_enabled=no -j12
strip bin/godot.frt.opt.llvm
```
## Copy folders:


## Thanks
Special thanks to: kloptops, and all PortMaster contributors for helping me test it!
