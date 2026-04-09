# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarPrintPositions.cpp

## Purpose
This file provides utility functions for debugging and printing the layout positions of control bar windows in the game UI.

## Responsibilities
- Recursively traverse and print window positions/sizes to a file
- Generate a debug file with control bar layout information
- Create temporary window layouts for inspection

## Key Types
None

## Key Functions
### PrintInfoRecursive
- Purpose: Recursively prints window position and size data to a file
- Calls: `winGetSize`, `winGetPosition`, `winGetInstanceData`, `m_decoratedNameString.str`, `winGetChild`, `winGetNext`

### PrintOffsetsFromControlBarParent
- Purpose: Creates a debug file with control bar window layout information
- Calls: `winGetWindowFromId`, `nameToKey`, `winCreateLayout`, `fopen`, `PrintInfoRecursive`, `fclose`, `destroyWindows`, `deleteInstance`

## Globals
None

## Dependencies
- `PreRTS.h`
- `stdio.h`
- `GameClient/GameWindowManager.h`
- `GameClient/WindowLayout.h`
- `TheWindowManager`
- `TheNameKeyGenerator`
