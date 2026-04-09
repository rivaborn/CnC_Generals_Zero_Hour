# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/SlavedUpdate.cpp

## Purpose
Handles behavior of slaved units (e.g., scout drones) that follow and assist their master units.

## Responsibilities
- Manages slaved unit positioning relative to master
- Handles repair logic for damaged masters
- Implements attack/scout/guard behaviors based on master's state
- Manages visual/audio effects for slaved state
- Handles team switching when master changes allegiance

## Key Types
- SlavedUpdate (Class): Main module for slaved unit behavior
- RepairStates (Enum): States for repair animation sequence
- CLOSE_ENOUGH (const Real): Minimum distance threshold (15 units)

## Key Functions
### update
- Purpose: Main update loop for slaved behavior
- Calls: doRepairLogic, doAttackLogic, doScoutLogic, doGuardLogic, stopSlavedEffects

### doAttackLogic
- Purpose: Positions slaved unit near master's target
- Calls: aiMoveToPosition, setWeaponBonusCondition

### doRepairLogic
- Purpose: Handles master unit repair sequence
- Calls: setRepairState, attemptHealing, aiMoveToPosition

### startSlavedEffects
- Purpose: Initializes slaved state visuals and effects
- Calls: receiveGrant (StealthUpdate)

### stopSlavedEffects
- Purpose: Cleans up slaved state when master dies
- Calls: clearStatus, clearDisabled

## Globals
- CLOSE_ENOUGH (Real): Distance threshold constant
- CLOSE_ENOUGH_SQR (Real): Squared distance threshold

## Dependencies
- GameLogic headers (Object, AIUpdate, Locomotor)
- Common utilities (RandomValue, Xfer)
- GameClient (Drawable, ParticleSys)
- Module/SlavedUpdate.h (module data)
