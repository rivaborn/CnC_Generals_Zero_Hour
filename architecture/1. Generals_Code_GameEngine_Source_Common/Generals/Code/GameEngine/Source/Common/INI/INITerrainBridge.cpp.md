# Generals/Code/GameEngine/Source/Common/INI/INITerrainBridge.cpp

## Purpose
This file handles parsing terrain bridge definitions from INI files in the Command & Conquer Generals game engine.

## Responsibilities
- Parses terrain bridge entries from INI files.
- Manages the creation and initialization of terrain bridges.
- Ensures that existing road items are not redefined as bridges.

## Key Types
- None

## Key Functions
### parseTerrainBridgeDefinition
- Purpose: Parses a terrain bridge definition from an INI file.
- Calls:
  - `getNextToken()`
  - `set(const char*)`
  - `findBridge(AsciiString)`
  - `isBridge()`
  - `newBridge(AsciiString)`
  - `initFromINI(TerrainRoadType*, TerrainFieldParse*)`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/INI.h"
  - "GameClient/TerrainRoads.h"
