# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarPrintPositions.cpp

## Purpose
This file provides utility functions for debugging and printing control bar window positions and sizes.

## Responsibilities
- Recursively traverse and print window hierarchy info
- Generate a text file with control bar layout data
- Create temporary window layout for inspection

## Key Types
None

## Key Functions
### PrintInfoRecursive
- Purpose: Recursively prints window position and size info to a file
- Calls: `winGetSize`, `winGetPosition`, `winGetInstanceData`, `winGetChild`, `winGetNext`

### PrintOffsetsFromControlBarParent
- Purpose: Generates a debug file with control bar window layout information
- Calls: `winGetWindowFromId`, `winCreateLayout`, `nameToKey`, `getFirstWindow`, `destroyWindows`, `deleteInstance`

## Globals
None

## Dependencies
- `GameWindowManager.h`
- `WindowLayout.h`
- `PreRTS.h`
- `stdio.h`
- `TheWindowManager`
- `TheNameKeyGenerator`
