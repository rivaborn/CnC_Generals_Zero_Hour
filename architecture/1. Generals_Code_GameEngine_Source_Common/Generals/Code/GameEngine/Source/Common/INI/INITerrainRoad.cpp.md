# Generals/Code/GameEngine/Source/Common/INI/INITerrainRoad.cpp

## Purpose
This file handles parsing terrain road definitions from INI files in the Command & Conquer Generals game engine.

## Responsibilities
- Parses terrain road entries from INI files.
- Manages the creation and initialization of `TerrainRoadType` objects.
- Ensures no redefinition of bridges as roads.

## Key Types
- None

## Key Functions
### parseTerrainRoadDefinition
- Purpose: Parses a terrain road definition from an INI file.
- Calls:
  - `getNextToken`
  - `set`
  - `findRoad`
  - `isBridge`
  - `newRoad`
  - `initFromINI`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Common/INI.h`
  - `GameClient/TerrainRoads.h`
