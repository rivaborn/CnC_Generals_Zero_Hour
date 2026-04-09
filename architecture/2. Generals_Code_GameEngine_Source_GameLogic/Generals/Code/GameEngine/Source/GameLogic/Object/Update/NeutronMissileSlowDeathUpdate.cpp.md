# Generals/Code/GameEngine/Source/GameLogic/Object/Update/NeutronMissileSlowDeathUpdate.cpp

## Purpose
This file contains the implementation for the `NeutronMissileSlowDeathBehavior` class, which handles the slow death update logic for neutron missile superweapons in Command & Conquer Generals.

## Responsibilities
- Manages the slow death behavior of neutron missiles.
- Handles explosions and scorch effects over time.
- Updates object states and applies damage within specified radii.

## Key Types
- **NeutronMissileSlowDeathBehaviorModuleData (struct)**: Stores configuration data for neutron missile blasts, including delays, radii, and damage settings.
- **NeutronMissileSlowDeathBehavior (class)**: Implements the slow death behavior logic for neutron missiles.

## Key Functions
### NeutronMissileSlowDeathBehavior::update
- Purpose: Updates the state of the neutron missile's slow death behavior, triggering explosions and scorch effects at specified intervals.
- Calls:
  - `SlowDeathBehavior::update()`
  - `FXList::doFXPos()`
  - `doBlast()`
  - `doScorchBlast()`

### NeutronMissileSlowDeathBehavior::doBlast
- Purpose: Executes a blast effect, applying damage and force to objects within the specified radius.
- Calls:
  - `ThePartitionManager->iterateObjectsInRange()`
  - `Object::topple()`
  - `Object::attemptDamage()`

### NeutronMissileSlowDeathBehavior::doScorchBlast
- Purpose: Applies scorch effects to objects within the specified radius, setting them on fire and changing their model condition.
- Calls:
  - `ThePartitionManager->iterateObjectsInRange()`
  - `Object::setModelConditionState()`

## Globals
- None

## Dependencies
- **Includes**:
  - "PreRTS.h"
  - "Common/GameState.h"
  - "Common/Player.h"
  - "Common/Xfer.h"
  - "GameClient/FXList.h"
  - "GameClient/Drawable.h"
  - "GameClient/GameClient.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/ObjectIter.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/Module/FlammableUpdate.h"
  - "GameLogic/Module/PhysicsUpdate.h"
  - "GameLogic/Module/NeutronMissileSlowDeathUpdate.h"
  - "GameLogic/Module/ToppleUpdate.h"
  - "GameLogic/TerrainLogic.h"

- **External Symbols**:
  - `TheGameLogic`
  - `TheTerrainLogic`
  - `TheGameClient`
