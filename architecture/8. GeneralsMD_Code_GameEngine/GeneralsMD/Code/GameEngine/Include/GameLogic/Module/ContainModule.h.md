# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ContainModule.h

## Purpose
Defines the interface for object containment in the game engine, including garrisoning, transport, and evac systems.

## Responsibilities
- Declares the `ContainModuleInterface` abstract class for container behavior
- Defines enums for enter/exit states and evac dispositions
- Specifies containment management functions (add/remove/kill contained objects)
- Declares player occupancy and weapon bonus handling for containers

## Key Types
- **ContainModuleInterface (Class)**: Abstract interface for container behavior
- **ObjectEnterExitType (Enum)**: Tracks enter/exit requests (WANTS_TO_ENTER, WANTS_TO_EXIT, WANTS_NEITHER)
- **EvacDisposition (Enum)**: Evacuation strategies (EVAC_TO_LEFT, EVAC_TO_RIGHT, EVAC_BURST_FROM_CENTER)
- **ContainedItemsList (typedef)**: List of contained objects
- **ContainIterateFunc (typedef)**: Callback for iterating contained objects

## Key Functions
### `onObjectWantsToEnterOrExit`
- Purpose: Handles enter/exit requests for objects
- Calls: None visible

### `orderAllPassengersToExit`
- Purpose: Orders all passengers to evacuate
- Calls: None visible

### `isValidContainerFor`
- Purpose: Checks if container can hold a specific object type
- Calls: None visible

### `processDamageToContained`
- Purpose: Applies percentage damage to contained units
- Calls: None visible

## Globals
- None

## Dependencies
- `Common/Module.h`
- `GameLogic/WeaponBonusConditionFlags.h`
- `GameLogic/Damage.h`
- Forward declarations: `OpenContain`, `Player`, `ExitInterface`, `Matrix3D`, `Weapon`, `CommandSourceType`
