# Generals/Code/GameEngine/Source/GameLogic/Object/Update/EMPUpdate.cpp

## Purpose
This file contains the implementation of the EMPUpdate class, which handles the electromagnetic pulse (EMP) effect in the game. It manages the growth, fading, and disabling effects of EMP fields on objects within a specified radius.

## Responsibilities
- Manages the lifecycle of an EMP field.
- Adjusts the scale and color tint of the EMP field over time.
- Disables nearby vehicles, structures, and aircraft within its radius.
- Creates particle effects to visualize the EMP's impact.

## Key Types
- **EMPUpdate (Class)**: Handles the EMP update logic.
- **RGBColor (Struct)**: Represents RGB color values used for tinting.

## Key Functions
### EMPUpdate::EMPUpdate
- Purpose: Initializes the EMP field with starting parameters such as scale, life duration, and colors.
- Calls:
  - `getEMPUpdateModuleData()`
  - `TheGameLogic->getFrame()`
  - `getObject()->setOrientation()`

### EMPUpdate::update
- Purpose: Updates the EMP field's state each frame, including scaling, color tinting, and disabling nearby objects.
- Calls:
  - `saturateRGB()`
  - `dr->setInstanceScale()`
  - `dr->colorTint()`
  - `dr->colorFlash()`
  - `doDisableAttack()`
  - `obj->kill()`

### EMPUpdate::doDisableAttack
- Purpose: Disables nearby objects within the EMP's radius, including vehicles, structures, and aircraft.
- Calls:
  - `ThePartitionManager->iterateObjectsInRange()`
  - `curVictim->setDisabledUntil()`
  - `drw->setTintStatus()`
  - `TheParticleSystemManager->createParticleSystem()`

## Globals
- None

## Dependencies
- **Includes**:
  - "PreRTS.h"
  - "Common/Thing.h"
  - "Common/ThingTemplate.h"
  - "Common/INI.h"
  - "Common/RandomValue.h"
  - "Common/Player.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Module/EMPUpdate.h"
  - "GameLogic/ObjectIter.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Object.h"
  - "GameClient/Drawable.h"
  - "Common/KindOf.h"
  - "GameClient/ParticleSys.h"
