# GeneralsMD/Code/GameEngine/Source/Common/INI/INIWater.cpp

## Purpose
Handles parsing of water-related settings from INI files for the game's water system.

## Responsibilities
- Parses water settings definitions for different times of day
- Manages water transparency settings with override support
- Updates skybox textures when water transparency is overridden

## Key Types
- `WaterSetting` (struct): Stores water configuration per time of day
- `WaterTransparencySetting` (struct): Manages water transparency and skybox textures
- `OVERRIDE<WaterTransparencySetting>`: Handles override logic for transparency settings

## Key Functions
### `parseWaterSettingDefinition`
- Purpose: Loads water settings for a specific time of day from INI
- Calls: `ini->getNextToken()`, `ini->initFromINI()`

### `parseWaterTransparencyDefinition`
- Purpose: Parses water transparency settings with override support
- Calls: `newInstance()`, `ini->initFromINI()`, `TheTerrainVisual->replaceSkyboxTextures()`

## Globals
- `WaterSettings` (array): Stores water settings for all times of day
- `TheWaterTransparency` (OVERRIDE pointer): Global water transparency settings
- `TimeOfDayNames` (array): Names of supported times of day

## Dependencies
- `INI.h`, `GameType.h`, `TerrainVisual.h`, `Water.h`
- `AsciiString`, `stricmp`, `INI_INVALID_DATA` exceptions
