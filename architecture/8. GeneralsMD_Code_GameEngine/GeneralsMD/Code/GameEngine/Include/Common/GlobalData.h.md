# GeneralsMD/Code/GameEngine/Include/Common/GlobalData.h

## Purpose
Header defining the `GlobalData` class, which centralizes game-wide configuration and settings used by both client and logic subsystems.

## Responsibilities
- Stores game configuration (graphics, audio, physics, etc.)
- Manages time-of-day and weather settings
- Provides access to user data paths
- Handles global lighting and rendering parameters
- Supports debug flags and performance tuning

## Key Types
- `GlobalData` (Class): Main container for global game settings
- `TerrainLighting` (Struct): Stores ambient/diffuse lighting and position data
- `_TerrainLOD` (Enum): Terrain detail levels
- `BodyDamageType` (Enum): Damage states for movement penalties
- `AIDebugOptions` (Enum): AI debugging flags

## Key Functions
### `init()`
- Purpose: Initializes global data
- Calls: Not inferable

### `setTimeOfDay()`
- Purpose: Updates time-of-day settings
- Calls: Not inferable

### `parseGameDataDefinition()`
- Purpose: Parses game data from INI files
- Calls: Not inferable

### `newOverride()`
- Purpose: Creates a new override instance of GlobalData
- Calls: Not inferable

## Globals
- `MAX_GLOBAL_LIGHTS` (const Int): Maximum number of global lights (3)
- `TheWritableGlobalData` (GlobalData*): Singleton instance of GlobalData

## Dependencies
- `Common/GameCommon.h`, `Common/AsciiString.h`, `Common/GameType.h`
- `Common/GameMemory.h`, `Common/SubsystemInterface.h`
- `GameClient/Color.h`, `Common/STLTypedefs.h`
- Forward declarations: `FieldParse`, `INI`, `WeaponBonusSet`
