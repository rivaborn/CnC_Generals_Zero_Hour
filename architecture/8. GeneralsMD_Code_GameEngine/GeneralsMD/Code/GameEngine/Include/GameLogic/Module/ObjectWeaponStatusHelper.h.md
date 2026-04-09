# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ObjectWeaponStatusHelper.h

## Purpose
Manages weapon status updates for game objects, ensuring model condition adjustments occur after other updates.

## Responsibilities
- Adjusts object model condition based on weapon status
- Runs updates in the final phase (PHASE_FINAL)
- Ensures continuous updates (never sleeps)

## Key Types
- **ObjectWeaponStatusHelperModuleData (Class)**: Module data container (empty)
- **ObjectWeaponStatusHelper (Class)**: Helper class for weapon status management
- **ObjectWeaponStatusHelperMagicEnum (Enum)**: Not inferable
- **ObjectWeaponStatusHelper_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### `getUpdatePhase`
- Purpose: Returns the update phase (PHASE_FINAL) for this helper.
- Calls: None

### `ObjectWeaponStatusHelper`
- Purpose: Constructor initializes the helper and sets it to always update.
- Calls: `getObject()`, `getTemplate()->canPossiblyHaveAnyWeapon()`, `setWakeFrame()`

### `update`
- Purpose: Adjusts model condition for weapon status and ensures continuous updates.
- Calls: `getObject()->adjustModelConditionForWeaponStatus()`

## Globals
None

## Dependencies
- `Common/ThingTemplate.h`
- `GameLogic/Object.h`
- `GameLogic/Module/ObjectHelper.h`
- `ModuleData`, `ObjectHelper`, `Thing`, `SleepyUpdatePhase`, `UpdateSleepTime`
