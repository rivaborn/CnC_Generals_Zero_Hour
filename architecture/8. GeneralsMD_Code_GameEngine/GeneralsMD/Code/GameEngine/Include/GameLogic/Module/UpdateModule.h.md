# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/UpdateModule.h

## Purpose
Defines the core update module system for game objects, including interfaces for various update behaviors and scheduling mechanisms.

## Responsibilities
- Declares base classes for update modules and their interfaces
- Defines scheduling enums and helper types for update timing
- Provides interfaces for specialized update behaviors (projectiles, docking, etc.)
- Establishes the module data structure and factory macros

## Key Types
- **UpdateModuleInterface (Class)**: Base interface for all update modules
- **UpdateModule (Class)**: Core update module implementation with scheduling support
- **UpdateSleepTime (Enum)**: Defines sleep durations for update scheduling
- **SleepyUpdatePhase (Enum)**: Specifies update phases for ordering
- **ProjectileUpdateInterface (Class)**: Interface for projectile-specific updates
- **DockUpdateInterface (Class)**: Interface for docking behavior updates
- **ExitInterface (Class)**: Interface for object exit/entry management
- **ExitDoorType (Enum)**: Types of exit doors for production/exit management

## Key Functions
### `setWakeFrame`
- Purpose: Schedules the next update call for an object
- Calls: None visible

### `friend_setNextCallFrame`
- Purpose: Sets the absolute frame for the next update call
- Calls: None visible

### `frameToSleepTime`
- Purpose: Converts frame counts to sleep time values
- Calls: None visible

## Globals
- **UPDATE_SLEEP_FOREVER (Enum)**: Constant for infinite sleep duration
- **FOREVER (Symbol)**: Used in frame calculations

## Dependencies
- `Common/Module.h`, `Common/GameType.h`, `Common/DisabledTypes.h`
- `GameLogic/Module/BehaviorModule.h`
- `MultiIniFieldParse`, `ThingTemplate`, `ObjectID`, `Coord3D`, `WeaponSlotType`, `WeaponTemplate`, `ParticleSystemTemplate`, `DamageInfo`, `CommandButton`, `Waypoint`, `CommandOption`
