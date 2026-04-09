# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/TransportAIUpdate.h

## Purpose
Defines the `TransportAIUpdate` class, which extends AI behavior for transport units (e.g., vehicles carrying soldiers).

## Responsibilities
- Overrides AI update methods for transport-specific logic.
- Manages occupant behavior during attacks.
- Provides state machine customization for transport units.
- Handles evacuation legality checks.

## Key Types
- **TransportAIUpdate (Class)**: Extends `AIUpdateInterface` to customize transport unit AI.
- **TransportAIUpdateMagicEnum (Enum)**: Not inferable (likely unused placeholder).
- **TransportAIUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder).

## Key Functions
### `TransportAIUpdate(Thing*, const ModuleData*)`
- Purpose: Constructor for the transport AI update module.
- Calls: Not inferable (constructor body not shown).

### `getAiFreeToExit(const Object*) const`
- Purpose: Determines if a unit is free to exit the transport.
- Calls: Not inferable.

### `makeStateMachine()`
- Purpose: Creates the AI state machine for transport units.
- Calls: Not inferable.

### `privateAttackObject(Object*, Int, CommandSourceType)`
- Purpose: Extends attack behavior to include occupants.
- Calls: Not inferable.

### `privateAttackPosition(Coord3D*, Int, CommandSourceType)`
- Purpose: Extends position-based attack behavior to include occupants.
- Calls: Not inferable.

### `privateForceAttackObject(Object*, Int, CommandSourceType)`
- Purpose: Forces occupants to attack a target.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `AIUpdate.h` (parent class interface).
- Memory pool and module macros (internal SAGE engine utilities).
