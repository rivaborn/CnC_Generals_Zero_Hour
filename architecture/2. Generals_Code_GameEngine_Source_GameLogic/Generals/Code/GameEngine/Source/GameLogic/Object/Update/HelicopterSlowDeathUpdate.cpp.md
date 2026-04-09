# Generals/Code/GameEngine/Source/GameLogic/Object/Update/HelicopterSlowDeathUpdate.cpp

## Purpose
This file implements the `HelicopterSlowDeathBehavior` class, which handles the slow death animation and effects for helicopter objects in the game.

## Responsibilities
- Manage the slow death sequence of helicopter objects.
- Handle audio, visual effects, and physics updates during the death process.
- Control the movement and orientation changes of the helicopter as it spirals down and explodes.

## Key Types
- `HelicopterSlowDeathBehaviorModuleData (struct)`: Stores configuration data for the slow death behavior.
- `HelicopterSlowDeathBehavior (class)`: Implements the logic for the slow death sequence.

## Key Functions
### beginSlowDeath
- Purpose: Initializes the slow death process, including setting up audio, visual effects, and physics parameters.
- Calls:
  - `getObject()->getDrawable()->stopAmbientSound()`
  - `TheAudio->addAudioEvent(&m_deathSound)`
  - `GameLogicRandomValueReal`
  - `Locomotor::setMaxLift`
  - `Locomotor::setMaxBraking`
  - `TheParticleSystemManager->createParticleSystem`
  - `Drawable::getPristineBonePositions`
  - `Drawable::convertBonePosToWorldPos`
  - `FXList::doFXPos`
  - `ObjectCreationList::create`
  - `EjectPilotDie::ejectPilot`

### update
- Purpose: Updates the slow death sequence, including movement, orientation changes, and effect triggers.
- Calls:
  - `SlowDeathBehavior::update()`
  - `getObject()->getTransformMatrix()`
  - `Matrix3D::In_Place_Pre_Rotate_Z`
  - `getObject()->setTransformMatrix()`
  - `TheGameLogic->getFrame()`
  - `PhysicsBehavior::applyMotiveForce`
  - `Drawable::getPristineBonePositions`
  - `Drawable::convertBonePosToWorldPos`
  - `FXList::doFXPos`
  - `ObjectCreationList::create`
  - `EjectPilotDie::ejectPilot`
  - `TheTerrainLogic->getHighestLayerForDestination`
  - `TheTerrainLogic->getLayerHeight`
  - `Drawable::setModelConditionState`
  - `TheAudio->removeAudioEvent`
  - `FXList::doFXObj`
  - `TheThingFactory->newObject`
  - `TheGameLogic->destroyObject`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/GameAudio.h"
  - "Common/GlobalData.h"
  - "Common/RandomValue.h"
  - "Common/ThingFactory.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameClient/FXList.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Locomotor.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/Module/EjectPilotDie.h"
  - "GameLogic/Module/HelicopterSlowDeathUpdate.h"
  - "GameLogic/Module/PhysicsUpdate.h"
