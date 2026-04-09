# Generals/Code/GameEngine/Source/GameLogic/Object/Update/SpecialAbilityUpdate.cpp

## Purpose
Handles processing of unit special abilities, including preparation, triggering, and cleanup.

## Responsibilities
- Manages the lifecycle of special abilities for game units.
- Handles unpacking, preparation, and packing phases.
- Ensures proper targeting and execution of special abilities.
- Cleans up resources after ability completion or interruption.

## Key Types
- None

## Key Functions
### update
- Purpose: Updates the state of a special ability, handling various stages like approach, unpack, prepare, trigger, pack, and finish.
- Calls:
  - `validateSpecialObjects`
  - `handlePackingProcessing`
  - `triggerAbilityEffect`
  - `resetPreparation`
  - `endPreparation`
  - `startPacking`
  - `finishAbility`

### initiateIntentToDoSpecialPower
- Purpose: Initializes the intent to perform a special power, setting up targets and other parameters.
- Calls:
  - `getSpecialAbilityUpdateModuleData`
  - `findObjectByID`
  - `createSpecialObject`

### killSpecialObjects
- Purpose: Destroys all special objects associated with the ability.
- Calls:
  - `TheGameLogic->destroyObject`
  - `setWeaponLock`

### validateSpecialObjects
- Purpose: Validates and removes any invalid special objects from the list.
- Calls:
  - `findObjectByID`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/GameAudio.h"
  - "Common/GlobalData.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/Object.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/SpecialAbilityUpdate.h"
