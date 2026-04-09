# GeneralsMD/Code/GameEngine/Source/Common/GlobalData.cpp

## Purpose
Manages global game configuration data, including graphics, audio, physics, and gameplay settings.

## Responsibilities
- Defines and initializes global game parameters via INI parsing
- Handles time-of-day and weather lighting configurations
- Manages override stacks for configuration changes
- Provides access to game-wide constants (physics, UI, etc.)
- Computes CRC checksums for executable and script files

## Key Types
- `GlobalData` (Class): Main configuration container with game-wide settings
- `FieldParse` (Struct): INI field parsing definition structure
- `LightingInfo` (Struct): Time-of-day lighting parameters

## Key Functions
### `GlobalData::newOverride`
- Purpose: Creates a new configuration override instance
- Calls: `NEW GlobalData`, `*override = *TheWritableGlobalData`

### `GlobalData::reset`
- Purpose: Removes all configuration overrides
- Calls: `delete TheWritableGlobalData`

### `GlobalData::parseGameDataDefinition`
- Purpose: Parses INI configuration into global data
- Calls: `INI::initFromINI`, `OptionPreferences` methods

### `GlobalData::setTimeOfDay`
- Purpose: Updates lighting based on time of day
- Calls: None (direct member assignments)

## Globals
- `TheWritableGlobalData` (GlobalData*): Current active configuration instance
- `GlobalData::m_theOriginal` (GlobalData*): Original configuration instance

## Dependencies
- Common: `INI`, `FileSystem`, `GameAudio`, `UserPreferences`
- GameLogic: `AI`, `Weapon`, `BodyModule`
- GameClient: `Color`, `TerrainVisual`
- GameNetwork: `FirewallHelper`
