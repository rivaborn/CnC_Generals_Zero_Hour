# GeneralsMD/Code/GameEngine/Include/Common/Player.h

## Purpose
Header file defining the `Player` class and related structures for the game's player system.

## Responsibilities
- Declares the `Player` class and its data structures
- Defines player-related enums and types
- Provides forward declarations for player-related classes
- Includes snapshot serialization methods

## Key Types
- **Player (Class)**: Main player class representing a game participant
- **PlayerRelationMap (Class)**: Manages player relationships (allies/enemies)
- **SpecialPowerReadyTimerType (Struct)**: Tracks special power cooldown timers
- **KindOfPercentProductionChange (Class)**: Production cost/time modifiers
- **BattlePlanStatus (Enum)**: Battle plan types (bombard, hold line, search & destroy)
- **ScienceAvailabilityType (Enum)**: Science availability states (available, disabled, hidden)

## Key Functions
### update()
- Purpose: Player update opportunity
- Calls: Not inferable

### canBuild()
- Purpose: Check if player can build a given template
- Calls: allowedToBuild()

### hasScience()
- Purpose: Check if player has a specific science
- Calls: Not inferable

### addUpgrade()
- Purpose: Add or update upgrade status
- Calls: Not inferable

### onUpgradeCompleted()
- Purpose: Handle upgrade completion events
- Calls: Not inferable

## Globals
- **NUM_HOTKEY_SQUADS (const Int)**: Maximum number of hotkey squads (10)

## Dependencies
- Common game headers (AcademyStats, Energy, GameType, etc.)
- Memory pool and snapshot system headers
- STL containers (hash_map, list)
- Thing and Team class headers
- Upgrade and Science system headers
