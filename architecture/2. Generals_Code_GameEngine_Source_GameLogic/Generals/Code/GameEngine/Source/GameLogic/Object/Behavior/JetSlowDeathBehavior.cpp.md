# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/JetSlowDeathBehavior.cpp

## Purpose
This file implements the death sequence for jet objects in Command & Conquer Generals, handling various effects and behaviors such as falling, rolling, and explosions.

## Responsibilities
- Manages the slow death behavior of jet objects.
- Handles different stages of death including initial impact, secondary effects, and final explosion.
- Controls audio and visual effects during the death sequence.
- Updates object state and physics properties to simulate realistic destruction.

## Key Types
- **JetSlowDeathBehaviorModuleData (Struct)**: Stores configuration data for the jet's death behavior, including FX lists, object creation lists, delays, and rates for rolling and pitching.
- **JetSlowDeathBehavior (Class)**: Implements the actual death sequence logic for jet objects, extending from `SlowDeathBehavior`.

## Key Functions
### JetSlowDeathBehaviorModuleData::buildFieldParse
- Purpose: Initializes field parsing for configuration data.
- Calls: `SlowDeathBehaviorModuleData::buildFieldParse`, `INI::parseFXList`, `INI::parseObjectCreationList`, `INI::parseDurationUnsignedInt`, `INI::parseReal`, `INI::parsePercentToReal`.

### JetSlowDeathBehavior::onDie
- Purpose: Handles the initial death event for jet objects.
- Calls: `getObject`, `isSignificantlyAboveTerrain`, `getJetSlowDeathBehaviorModuleData`, `FXList::doFXObj`, `ObjectCreationList::create`, `TheGameLogic->destroyObject`.

### JetSlowDeathBehavior::beginSlowDeath
- Purpose: Initiates the slow death sequence for jet objects.
- Calls: `SlowDeathBehavior::beginSlowDeath`, `getObject`, `getJetSlowDeathBehaviorModuleData`, `FXList::doFXObj`, `ObjectCreationList::create`, `TheAudio->addAudioEvent`, `Locomotor::setMaxLift`, `Locomotor::setMaxTurnRate`.

### JetSlowDeathBehavior::update
- Purpose: Updates the death sequence state, including rolling, pitch adjustments, and effect triggers.
- Calls: `SlowDeathBehavior::update`, `getObject`, `getJetSlowDeathBehaviorModuleData`, `PhysicsBehavior::setRollRate`, `TheAudio->removeAudioEvent`, `FXList::doFXObj`, `ObjectCreationList::create`, `TheGameLogic->destroyObject`.

## Globals
- None

## Dependencies
- **Includes**: "PreRTS.h", "Common/GlobalData.h", "Common/ThingTemplate.h", "Common/Xfer.h", "GameClient/FXList.h", "GameClient/InGameUI.h", "GameLogic/GameLogic.h", "GameLogic/Locomotor.h", "GameLogic/Module/AIUpdate.h", "GameLogic/Module/JetSlowDeathBehavior.h", "GameLogic/Module/PhysicsUpdate.h
