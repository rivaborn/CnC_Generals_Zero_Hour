# Generals/Code/GameEngine/Source/GameLogic/Object/Update/StructureToppleUpdate.cpp

## Purpose
This file contains the implementation for the `StructureToppleUpdate` class, which handles the logic for structures toppling over when damaged in Command & Conquer Generals.

## Responsibilities
- Handle the initialization and destruction of structure topple updates.
- Parse configuration data from INI files.
- Manage the state transitions of a structure as it topples.
- Apply visual effects and damage during the toppling process.
- Update the structural integrity and position of the structure.

## Key Types
- `StructureToppleUpdate` (Class): Manages the toppling behavior of structures.
- `StructureToppleUpdateModuleData` (Struct): Stores configuration data for structure topple updates.
- `AngleFXInfo` (Struct): Holds information about angle-based visual effects.

## Key Functions
### parseOCL
- Purpose: Parses object creation lists from INI files.
- Calls: `INI::scanIndexList`, `TheObjectCreationListStore->findObjectCreationList`

### parseAngleFX
- Purpose: Parses angle-based visual effect data from INI files.
- Calls: `INI::parseReal`, `INI::parseFXList`

### beginStructureTopple
- Purpose: Initiates the toppling process for a structure when damaged.
- Calls: `TheGameLogic->getFrame`, `GameLogicRandomValue`, `TheScriptEngine->adjustToppleDirection`, `doToppleStartFX`

### onDie
- Purpose: Handles the death of a structure and begins the toppling process.
- Calls: `getObject()->getBodyModule()->getLastDamageInfo`, `AIUpdateInterface::markAsDead`, `TheGameLogic->deselectObject`, `beginStructureTopple`

### update
- Purpose: Updates the state of the toppling structure each frame.
- Calls: `TheGameLogic->getFrame`, `doAngleFX`, `applyCrushingDamage`, `doPhaseStuff`, `getObject()->setTransformMatrix`

### doToppleDoneStuff
- Purpose: Finalizes the toppling process and applies final effects.
- Calls: `getObject()->findUpdateModule`, `BoneFXUpdate::stopAllBoneFX`, `getObject()->getOrientation`, `getObject()->setTransformMatrix`

### applyCrushingDamage
- Purpose: Applies damage to objects in the area as the structure topples.
- Calls: `TheWeaponStore->createAndFireTempWeapon`, `FXList::doFXPos`

### doToppleStartFX
- Purpose: Triggers visual effects at the start of the toppling process.
- Calls: `FXList::doFXPos`, `doPhaseStuff`

### doToppleDelayBurstFX
- Purpose: Triggers delayed burst effects during the toppling process.
- Calls: `FXList::doFXPos`, `TheParticleSystemManager->createParticleSystem`, `drawable->getPristineBonePositions`, `doPhaseStuff`

## Globals
- `MAX_IDX` (Int): Maximum index for random list generation.

## Dependencies
- Key includes:
  - "Common/Thing.h"
  - "Common/ThingTemplate.h"
  - "Common/INI.h"
  - "Common/RandomValue.h"
  - "Common/Xfer.h"
  - "GameClient/FXList.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Module/BoneFXUpdate.h"
  - "GameLogic/Module/StructureToppleUpdate.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Object.h"
  - "GameLogic/ObjectCreationList.h"
  - "GameLogic/ScriptEngine.h"
  - "GameLogic/Weapon.h"
  - "GameClient/Drawable.h"
  - "GameClient/InGameUI.h"
