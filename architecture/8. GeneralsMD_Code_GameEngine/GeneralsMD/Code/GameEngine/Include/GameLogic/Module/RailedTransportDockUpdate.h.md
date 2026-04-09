# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RailedTransportDockUpdate.h

## Purpose
Defines the `RailedTransportDockUpdate` module for managing railed transport docking mechanics in the game.

## Responsibilities
- Manages docking/unloading logic for railed transport objects
- Provides interface for loading/unloading state checks
- Handles timing and distance calculations for docking animations
- Implements module data parsing and serialization

## Key Types
- **RailedTransportDockUpdateModuleData (Class)**: Contains module configuration data (durations, tolerance)
- **RailedTransportDockUpdateInterface (Class)**: Abstract interface for docking operations
- **RailedTransportDockUpdate (Class)**: Main docking update module implementation
- **RailedTransportDockUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **RailedTransportDockUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### `update`
- Purpose: Handles periodic docking/unloading updates
- Calls: `doPullInDocking`, `doPushOutDocking`, `unloadNext`

### `action`
- Purpose: Processes docking actions from objects
- Calls: Not inferable

### `doPullInDocking`
- Purpose: Animates objects entering the dock
- Calls: Not inferable

### `doPushOutDocking`
- Purpose: Animates objects exiting the dock
- Calls: Not inferable

## Globals
- None

## Dependencies
- `DockUpdate.h` (base class)
- `MultiIniFieldParse` (for config parsing)
- `Object`, `Thing`, `ObjectID` (game entity types)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macro system (`
