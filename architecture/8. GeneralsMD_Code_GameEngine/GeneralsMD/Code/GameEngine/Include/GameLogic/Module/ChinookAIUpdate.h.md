# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ChinookAIUpdate.h

## Purpose
Defines the AI update logic for Chinook helicopters, including flight states and supply/attack behaviors.

## Responsibilities
- Manages Chinook flight states (taking off, flying, landing, etc.)
- Handles supply ferrying and combat operations
- Controls rope deployment for troops/units
- Implements state machine for Chinook behavior
- Provides upgradeable supply boost mechanics

## Key Types
- **ChinookAIUpdateModuleData (Class)**: Stores Chinook-specific configuration (rope physics, particle effects, supply boost)
- **ChinookFlightStatus (Enum)**: Tracks Chinook flight state (taking off, flying, combat drop, landing, landed)
- **ChinookAIUpdate (Class)**: Core AI logic for Chinook helicopters

## Key Functions
### `update()`
- Purpose: Main AI update loop for Chinook behavior
- Calls: State machine updates, command processing

### `aiDoCommand()`
- Purpose: Executes AI commands for the Chinook
- Calls: Command parsing, state transitions

### `privateCombatDrop()`
- Purpose: Handles combat drop operations
- Calls: Rope deployment logic, troop unloading

### `privateAttackObject()`
- Purpose: Manages attack commands, including occupant coordination
- Calls: Occupant attack delegation

## Globals
- None

## Dependencies
- `GameLogic/AIStateMachine.h`
- `GameLogic/Module/SupplyTruckAIUpdate.h`
- Inherits from `SupplyTruckAIUpdate`
- Uses `AICommandParmsStorage`, `Coord3D`, `ObjectID` types
