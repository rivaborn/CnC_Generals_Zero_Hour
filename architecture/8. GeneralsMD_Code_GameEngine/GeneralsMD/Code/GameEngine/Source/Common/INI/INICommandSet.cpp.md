# GeneralsMD/Code/GameEngine/Source/Common/INI/INICommandSet.cpp

## Purpose
Parses command set definitions from INI files for the game's UI system.

## Responsibilities
- Parses command set definitions from INI files
- Delegates parsing to ControlBar class
- Supports context-sensitive UI configuration

## Key Types
None

## Key Functions
### parseCommandSetDefinition
- Purpose: Parses command set definitions from an INI file
- Calls: ControlBar::parseCommandSetDefinition

## Globals
None

## Dependencies
- INI.h (INI class)
- GameClient/ControlBar.h (ControlBar class)
- PreRTS.h (engine precompiled header)
