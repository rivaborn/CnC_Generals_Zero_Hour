# Generals/Code/GameEngine/Source/GameLogic/Object/Update/SlavedUpdate.cpp

## Purpose
This file implements the `SlavedUpdate` class, which manages the behavior of units that are slaved to a master unit in Command & Conquer Generals. It handles various tasks such as repairing the master, attacking its targets, and scouting.

## Responsibilities
- Manage the state and behavior of slaved units.
- Handle repair logic for the master unit.
- Implement attack and scout behaviors based on the master's actions.
- Ensure slaved units remain close to their master.

## Key Types
- **SlavedUpdate (Class)**: Manages the update logic for slaved units.
- **RepairStates (Enum)**: Represents different states in the repair process.

## Key Functions
### SlavedUpdate::update
- Purpose: Updates the state and behavior of the slaved unit.
- Calls:
  - `startSlavedEffects`
  - `stopSlavedEffects`
  - `doRepairLogic`
  - `doAttackLogic`
  - `doScoutLogic`
  - `doGuardLogic`

### SlavedUpdate::doAttackLogic
- Purpose: Handles the logic for attacking the master's target.
- Calls:
  - `aiMoveToPosition`

### SlavedUpdate::doScoutLogic
- Purpose: Handles the logic for scouting the master's movement destination.
- Calls:
  - `aiMoveToPosition`

### SlavedUpdate::doGuardLogic
- Purpose: Handles the logic for guarding the master's position.
- Calls:
  - `aiMoveToPosition`

### SlavedUpdate::doRepairLogic
- Purpose: Handles the logic for repairing the master unit.
- Calls:
  - `attemptHealing`
  - `setRepairState`

## Globals
- **CLOSE_ENOUGH (Real)**: Distance threshold for close proximity checks.
- **CLOSE_ENOUGH_SQR (Real)**: Square of the distance threshold.

## Dependencies
- Key includes and external symbols used but not defined here:
  - `Common/RandomValue.h`
  - `Common/Xfer.h`
  - `GameLogic/AIPathfind.h`
  - `GameLogic/Damage.h`
  - `GameLogic/GameLogic.h`
  - `GameLogic/Locomotor.h`
  - `GameLogic/Object.h`
  - `GameLogic/PartitionManager.h`
  - `GameLogic/TerrainLogic.h`
  - `GameLogic/Module/AIUpdate.h`
  - `GameLogic/Module/BodyModule.h`
  - `GameLogic/Weapon.h`
