# Generals/Code/GameEngine/Source/GameLogic/Object/Update/CommandButtonHuntUpdate.cpp

## Purpose
This file implements the `CommandButtonHuntUpdate` module, which handles hunting behavior for units using special powers or weapons. It ensures that idle units target new enemies when a specific command button is active.

## Responsibilities
- Manage hunting behavior for units with special abilities.
- Target and attack nearby enemy units based on command button input.
- Handle different types of commands (special powers, weapons).
- Periodically scan for targets within a specified range.

## Key Types
- `CommandButtonHuntUpdateModuleData`: Stores configuration data like scan rate and range.
- `CommandButtonHuntUpdate`: Manages the hunting logic for units.

## Key Functions
### CommandButtonHuntUpdate::update()
- Purpose: Main update function that checks if the unit is idle and targets enemies.
- Calls:
  - `huntSpecialPower()`
  - `huntWeapon()`

### CommandButtonHuntUpdate::huntSpecialPower(AIUpdateInterface *ai)
- Purpose: Handles hunting logic for special powers.
- Calls:
  - `scanClosestTarget()`
  - `doCommandButtonAtObject()`

### CommandButtonHuntUpdate::huntWeapon(AIUpdateInterface *ai)
- Purpose: Handles hunting logic for weapons.
- Calls:
  - `setWeaponLock()`

### CommandButtonHuntUpdate::scanClosestTarget(void)
- Purpose: Scans for the closest target within a specified range.
- Calls:
  - `iterateObjectsInRange()`
  - `canDoSpecialPowerAtObject()`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `ActionManager.h`
  - `Player.h`
  - `RandomValue.h`
  - `SpecialPower.h`
  - `ThingTemplate.h`
  - `Xfer.h`
  - `ControlBar.h`
  - `Drawable.h`
  - `GameLogic.h`
  - `PartitionManager.h`
  - `Object.h`
  - `ObjectIter.h`
  - `CommandButtonHuntUpdate.h`
  - `AIUpdate.h`
  - `CollideModule.h`
  - `SpecialAbilityUpdate.h`
  - `SpecialPowerModule.h`
  - `ScriptEngine.h`
