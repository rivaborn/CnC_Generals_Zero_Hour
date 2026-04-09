# Generals/Code/GameEngine/Source/GameLogic/Object/Update/MobMemberSlavedUpdate.cpp

## Purpose
This file contains the implementation of `MobMemberSlavedUpdate`, a class responsible for managing the behavior of units that are slaved to a master unit in Command & Conquer Generals. The class handles tasks such as following the master, responding to damage, and maintaining formation.

## Responsibilities
- Manage the movement and behavior of slaved units.
- Respond to damage received by the master or the slave.
- Ensure slaves remain close to their master.
- Handle self-tasking logic for slaves when not directly commanded.

## Key Types
- `MobMemberSlavedUpdate` (Class): Manages the update logic for slaved units.
- `MobStates` (Enum): Represents different states of the mob member's behavior.

## Key Functions
### MobMemberSlavedUpdate::update
- Purpose: Updates the state and behavior of the slaved unit each frame.
- Calls:
  - `TheGameLogic->findObjectByID`
  - `getAIUpdateInterface`
  - `chooseLocomotorSet`
  - `aiMoveToPosition`
  - `aiAttackObject`

### MobMemberSlavedUpdate::onEnslave
- Purpose: Starts the slaving effects when a unit is enslaved.
- Calls:
  - `startSlavedEffects`

### MobMemberSlavedUpdate::onSlaverDie
- Purpose: Stops the slaving effects and kills the slave if the master dies.
- Calls:
  - `stopSlavedEffects`
  - `kill`

## Globals
- `CLOSE_ENOUGH` (Real): Distance threshold for considering units close enough to each other.
- `CLOSE_ENOUGH_SQR` (Real): Square of the distance threshold.

## Dependencies
- Key includes and external symbols used but not defined here:
  - `GameClient/InGameUI.h`
  - `GameClient/Drawable.h`
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
  - `GameLogic/Module/MobMemberSlavedUpdate.h`
  - `GameLogic/Module/SpawnBehavior.h`
