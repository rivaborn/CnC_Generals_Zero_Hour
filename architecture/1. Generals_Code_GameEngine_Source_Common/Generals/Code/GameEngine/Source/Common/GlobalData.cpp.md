# Generals/Code/GameEngine/Source/Common/GlobalData.cpp

## Purpose
This file contains the implementation of the `GlobalData` class, which manages global configuration settings and data for the Command & Conquer Generals game engine.

## Responsibilities
- Manages global configuration settings.
- Parses INI files to load and update global data.
- Handles overrides of global data instances.
- Provides methods to reset and initialize global data.

## Key Types
- `GlobalData` (Class): Manages global game settings and configurations.

## Key Functions
### GlobalData::setTimeOfDay
- Purpose: Sets the current time of day and updates lighting parameters accordingly.
- Calls:
  - `m_terrainAmbient[i] = m_terrainLighting[ tod ][i].ambient;`
  - `m_terrainDiffuse[i] = m_terrainLighting[ tod ][i].diffuse;`
  - `m_terrainLightPos[i] = m_terrainLighting[ tod ][i].lightPos;`

### GlobalData::newOverride
- Purpose: Creates a new instance of `GlobalData` to override the existing data.
- Calls:
  - `NEW GlobalData`
  - `*override = *TheWritableGlobalData;`
  - `override->m_next = TheWritableGlobalData;`
  - `TheWritableGlobalData = override;`

### GlobalData::reset
- Purpose: Resets global data by deleting any overrides and restoring the original instance.
- Calls:
  - `delete TheWritableGlobalData;`
  - `TheWritableGlobalData = next;`

### GlobalData::parseGameDataDefinition
- Purpose: Parses an INI file to load or update global game settings.
- Calls:
  - `ini->initFromINI(TheWritableGlobalData, s_GlobalDataFieldParseTable);`
  - `SHGetSpecialFolderPath(NULL, temp, CSIDL_PERSONAL, true)`
  - `CreateDirectory(temp, NULL);`
  - `optionPref.getAlternateMouseModeEnabled();`
  - `optionPref.getScrollFactor();`

## Globals
- `TheWritableGlobalData (GlobalData*)`: The global singleton instance of `GlobalData`.

## Dependencies
- Key includes:
  - "Common/CRC.h"
  - "Common/File.h"
  - "Common/FileSystem.h"
  - "Common/GameAudio.h"
  - "Common/INI.h"
  - "Common/UserPreferences.h"
  - "Common/Version.h"
  - "GameLogic/AI.h"
  - "GameLogic/Weapon.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameClient/Color.h"
  - "GameClient/TerrainVisual.h"
  - "GameNetwork/FirewallHelper.h"
