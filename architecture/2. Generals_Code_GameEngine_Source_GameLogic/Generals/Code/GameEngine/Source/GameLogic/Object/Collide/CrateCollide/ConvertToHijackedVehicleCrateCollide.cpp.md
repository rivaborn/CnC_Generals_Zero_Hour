# Generals/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/ConvertToHijackedVehicleCrateCollide.cpp

## Purpose
This file implements the behavior for a crate that hijacks and converts an enemy vehicle, switching its control to the player's team and killing its driver.

## Responsibilities
- Validate if a target vehicle can be hijacked.
- Execute the hijacking process, including changing ownership, setting status flags, and transferring AI control.
- Handle audio events and script interactions related to the hijacking.
- Manage the visibility and collision properties of the hijacker during the conversion.

## Key Types
- None

## Key Functions
### isValidToExecute
- Purpose: Determines if a target vehicle is valid for hijacking based on various conditions (e.g., not dead, not an aircraft, not already hijacked).
- Calls:
  - CrateCollide::isValidToExecute
  - other->isEffectivelyDead
  - other->isKindOf
  - getObject()->getRelationship

### executeCrateBehavior
- Purpose: Executes the hijacking process, including changing ownership, setting status flags, and transferring AI control.
- Calls:
  - TheRadar->tryInfiltrationEvent
  - TheEva->setShouldPlay
  - other->setTeam
  - other->setStatus
  - targetAI->aiMoveToPosition
  - targetAI->aiIdle
  - dozerAI->cancelTask
  - TheAudio->addAudioEvent
  - TheScriptEngine->transferObjectName
  - jackerExp->setVeterancyLevel
  - targetExp->setVeterancyLevel
  - hijackerUpdate->setTargetObject
  - hijackerUpdate->setIsInVehicle
  - hijackerUpdate->setUpdate
  - obj->setStatus
  - ThePartitionManager->unRegisterObject
  - obj->getDrawable()->setDrawableHidden

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/PlayerList.h"
  - "Common/Radar.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameClient/Eva.h"
  - "GameClient/InGameUI.h"
  - "GameLogic/ExperienceTracker.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Module/ConvertToHijackedVehicleCrateCollide.h"
  - "GameLogic/Module/HijackerUpdate.h"
  - "GameLogic/Module/ContainModule.h"
  - "GameLogic/Object.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/ScriptEngine.h"
  - "GameLogic/Module/DozerAIUpdate
