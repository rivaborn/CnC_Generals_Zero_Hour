# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/PropagandaCenterBehavior.cpp

## Purpose
This file implements the behavior for a Propaganda Center in Command & Conquer Generals, handling brainwashing of captured units.

## Responsibilities
- Manages brainwashing process of captured units.
- Handles unit restoration to original owners upon deletion.
- Updates brainwashing status and exits units when conditions are met.

## Key Types
- **PropagandaCenterBehaviorModuleData (struct):** Stores configuration data for the Propaganda Center behavior, such as brainwash duration.
- **PropagandaCenterBehavior (class):** Implements the logic for the Propaganda Center's behavior, including brainwashing and unit management.

## Key Functions
### PropagandaCenterBehavior::onDelete
- Purpose: Handles cleanup when the Propaganda Center is deleted, restoring captured units to their original owners.
- Calls:
  - `TheGameLogic->findObjectByID`
  - `obj->restoreOriginalTeam`

### PropagandaCenterBehavior::update
- Purpose: Updates the brainwashing process, checking if a unit has been brainwashed long enough and then exiting it from the center.
- Calls:
  - `TheGameLogic->getFrame`
  - `reserveDoorForExit`
  - `brainwashingSubject->setTemporaryTeam`
  - `ai->setSurrendered`
  - `exitObjectViaDoor`

### PropagandaCenterBehavior::onRemoving
- Purpose: Handles the removal of a unit from the Propaganda Center, resetting brainwashing subject if necessary.
- Calls:
  - `PrisonBehavior::onRemoving`

## Globals
- None

## Dependencies
- **Includes:**
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameClient/InGameUI.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Module/PropagandaCenterBehavior.h"
