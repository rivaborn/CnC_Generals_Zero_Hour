# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/PropagandaTowerBehavior.cpp

## Purpose
This file implements the behavior for the Propaganda Tower in Command & Conquer Generals, handling its effects on nearby units and structures.

## Responsibilities
- Track objects within a specified radius.
- Apply healing and weapon bonuses to allied units.
- Manage upgrades that enhance the tower's effects.
- Handle object creation, capture, death, and update events.

## Key Types
- **ObjectTracker (Class)**: Tracks objects within the Propaganda Tower's influence area.
- **PropagandaTowerBehaviorModuleData (Struct)**: Stores configuration data for the Propaganda Tower behavior.

## Key Functions
### PropagandaTowerBehavior::update
- Purpose: Updates the tower's influence on nearby units and structures.
- Calls:
  - `doScan`
  - `effectLogic`

### PropagandaTowerBehavior::onCapture
- Purpose: Handles changes in ownership of the tower.
- Calls:
  - `removeAllInfluence`

### PropagandaTowerBehavior::doScan
- Purpose: Scans for objects within the tower's influence area and applies effects.
- Calls:
  - `FXList::doFXObj`
  - `ThePartitionManager->iterateObjectsInRange`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/GameState.h"
  - "Common/Player.h"
  - "GameLogic/Object.h"
  - "GameLogic/Weapon.h"
  - "GameLogic/Module/PropagandaTowerBehavior.h"
