# Generals/Code/GameEngine/Source/Common/INI/INIWater.cpp

## Purpose
This file contains functions for parsing water settings and transparency from INI files in the Command & Conquer Generals game engine.

## Responsibilities
- Parse water setting definitions from INI files.
- Handle water transparency settings, including overrides.
- Update skybox textures based on new water transparency settings.

## Key Types
- None

## Key Functions
### parseWaterSettingDefinition
- Purpose: Parses a water setting definition from an INI file.
- Calls:
  - `ini->getNextToken()`
  - `stricmp()`
  - `ini->initFromINI()`

### parseWaterTransparencyDefinition
- Purpose: Parses and handles water transparency settings, including overrides and skybox texture updates.
- Calls:
  - `newInstance(WaterTransparencySetting)`
  - `TheWaterTransparency.getNonOverloadedPointer()`
  - `ini->getLoadType()`
  - `wtOverride->markAsOverride()`
  - `wt->friend_getFinalOverride()->setNextOverride(wtOverride)`
  - `TheTerrainVisual->replaceSkyboxTextures(oldTextures, newTextures)`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/INI.h"
  - "Common/GameType.h"
  - "GameClient/TerrainVisual.h"
  - "GameClient/Water.h"
