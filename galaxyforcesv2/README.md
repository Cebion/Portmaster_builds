# Galaxy Forces V2

## Source: 

https://sourceforge.net/p/galaxyv2/code/HEAD/tree/

## Controls:

Start			= Enter
Select			= Back
A			= Attack 1
B			= Attack 2
X			= Belt 3
Y			= Belt 4
L1			= Belt 1
R1			= Belt 2
L2			= Page Forward
R2			= Page Back
L3			= Access Menu
DPAD Up			= Character
DPAD Down		= Log
DPAD Left		= Powers
DPAD Right		= Inventory
Joystick		= Move

## Building

```
wget https://sourceforge.net/projects/galaxyv2/files/galaxyv2/galaxyv2_2.00/galaxyv2_2.00_src.zip
unzip galaxyv2_2.00_src.zip
Add mouse support (Ask on PM discord if not sure)
cp SDL_sim_cursor.h galaxyv2_2.00_src/src/graph
cd galaxyv2_2.00_src
vim src/graph.h
Add this line after #include <SDL.h>
vim src/graph.h
#include "SDL_sim_cursor.h"
vim src/graph.cpp
Add this at top file
#define SDL_SIM_CURSOR_COMPILE 1

Add this just before SDL_Quit();
SDL_SIM_MouseQuit();

Add this after the SDL_INIT if statement
SDL_SIM_MouseInit();

Add SDL_SIm command after m_pRenderer
m_pRenderer = SDL_CreateRenderer(m_pWindow, -1, SDL_RENDERER_ACCELERATED | SDL_RENDERER_PRESENTVSYNC);
SDL_SIM_Set_Renderer(m_pRenderer);

Add
//Update screen
SDL_SIM_RenderCursor(NULL);


vim src/common/global.cpp
Need to change line 220
change strcpy(szDataPath, ""); //not used/found 
to strcpy(szDataPath, "./"); //not used/found


cd build/linux

make -j8
strip server
strip mapeditor
strip galaxyv2
```
## Copy folders:

config.txt

*PAD_ENABLE        0 //always uses the first gamepad listed,
                //if you have trouble with the gamepad, set to 0



## Thanks
Special thanks to @kloptops for helping with mouse support for this this game

