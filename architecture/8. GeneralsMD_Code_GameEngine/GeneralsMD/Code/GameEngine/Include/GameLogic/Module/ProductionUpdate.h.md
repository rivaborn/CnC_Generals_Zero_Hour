# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ProductionUpdate.h

## Purpose
Defines the production system for building units and upgrades in Command & Conquer Generals Zero Hour.

## Responsibilities
- Manages production queues for units and upgrades
- Handles door animations during production
- Tracks production progress and quantities
- Provides interface for queuing/canceling production
- Implements special power construction for buildings

## Key Types
- **ProductionEntry (Class)**: Represents a single production item (unit or upgrade)
- **ProductionID (Enum)**: Unique identifier for production entries
- **ProductionType (Enum)**: Type of production (invalid, unit, upgrade)
- **ProductionUpdateModuleData (Class)**: Configuration data for production module
- **ProductionUpdateInterface (Class)**: Interface for production control
- **ProductionUpdate (Class)**: Main production module handling updates and logic
- **DoorInfo (Class)**: Tracks door animation states during production

## Key Functions
### `queueCreateUnit`
- Purpose: Adds a unit to the production queue
- Calls: `addToProductionQueue`, `requestUniqueUnitID`

### `queueUpgrade`
- Purpose: Adds an upgrade to the research queue
- Calls: `addToProductionQueue`

### `update`
- Purpose: Updates production progress and door animations
- Calls: `updateDoors`, various production entry methods

### `onDie`
- Purpose: Handles cleanup when the producing object dies
- Calls: `cancelAndRefundAllProduction`

## Globals
- None

## Dependencies
- `Common/ModelState.h`
- `GameLogic/Module/DieModule.h`
- `GameLogic/Module/UpdateModule.h`
- `MemoryPoolObject`, `ThingTemplate`, `UpgradeTemplate`, `CommandButton` (forward references)
