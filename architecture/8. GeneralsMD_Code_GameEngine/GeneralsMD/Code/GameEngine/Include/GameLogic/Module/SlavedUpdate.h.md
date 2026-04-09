# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SlavedUpdate.h

## Purpose
Defines the SlavedUpdate module for managing units that follow a master unit (e.g., scout drones, repair drones).

## Responsibilities
- Manages slaved unit behavior (scouting, attacking, guarding, repairing)
- Handles enslavement/disengagement logic
- Controls repair state transitions and effects
- Configures via INI-based module data

## Key Types
- **SlavedUpdateModuleData (Class)**: Configuration data for slaved behavior (ranges, repair settings).
- **RepairStates (Enum)**: States for repair sequence (NONE, UNPACKING, READY, WELDING, etc.).
- **SlavedUpdate (Class)**: Core module implementing slaved unit logic.

## Key Functions
### `doScoutLogic`
- Purpose: Handles scouting behavior for slaved units.
- Calls: Not inferable.

### `doAttackLogic`
- Purpose: Manages attack behavior when master targets an enemy.
- Calls: Not inferable.

### `doRepairLogic`
- Purpose: Controls repair state machine and healing logic.
- Calls: Not inferable.

### `update`
- Purpose: Main update loop for slaved unit logic.
- Calls: Not inferable.

## Globals
- **SLAVED_UPDATE_RATE (Int)**: Update frequency (LOGICFRAMES_PER_SECOND/4).

## Dependencies
- `Common/INI.h`, `GameLogic/Module/UpdateModule.h`
- `DamageInfo`, `ModelConditionFlagType` (forward declarations)
