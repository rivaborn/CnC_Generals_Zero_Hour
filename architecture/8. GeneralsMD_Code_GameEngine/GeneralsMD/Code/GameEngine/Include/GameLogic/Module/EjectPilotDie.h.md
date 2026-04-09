# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/EjectPilotDie.h

## Purpose
Defines a game module that creates a new object when the parent object dies.

## Responsibilities
- Manages ejection of pilot objects upon parent object death
- Handles creation of objects in-air or on-ground based on module data
- Provides invulnerability timing for ejected objects
- Implements standard module macros for memory management and serialization

## Key Types
- **EjectPilotDieModuleData (Class)**: Stores configuration for ejection behavior (object creation lists and invulnerability time)
- **EjectPilotDie (Class)**: Module that handles pilot ejection logic on object death
- **EjectPilotDieMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **Thing (Class)**: Forward reference to game entity
- **ObjectCreationList (Class)**: Forward reference to object creation template

## Key Functions
### ejectPilot
- Purpose: Creates a new object from the given creation list at the dying object's position
- Calls: Not inferable from header

### onDie
- Purpose: Handles the death event to trigger pilot ejection
- Calls: ejectPilot

### getEjectPilotDieInterface
- Purpose: Returns the module interface for type checking
- Calls: None

## Globals
- None

## Dependencies
- `DieModule.h` (base class)
- `Common/INI.h` (INI parsing)
- `Thing` class (game entity)
- `ObjectCreationList` class (object templates)
- `DieModuleData` (base module data)
- `MultiIniFieldParse` (INI parsing)
- `UnsignedInt` (basic type)
- `DamageInfo` (damage event data)
- `Object` (game object base)
