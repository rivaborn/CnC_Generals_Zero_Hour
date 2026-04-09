# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/JetSlowDeathBehavior.cpp

## Purpose
Implements the death sequence behavior for jet objects in the game, handling both in-air and ground impacts with timed effects.

## Responsibilities
- Manages multi-stage death animations for jets
- Handles timed effects and object creation lists during death
- Controls jet physics during death (rolling, pitching, falling)
- Manages audio loops for death sequences
- Coordinates ground impact detection and final explosion

## Key Types
- **JetSlowDeathBehaviorModuleData (struct)**: Contains configuration for death effects, timings, and physics parameters
- **JetSlowDeathBehavior (class)**: Implements the jet death behavior logic

## Key Functions
### JetSlowDeathBehavior::onDie
- Purpose: Initiates death sequence based on whether jet is airborne or on ground
- Calls: SlowDeathBehavior::onDie, FXList::doFXObj, ObjectCreationList::create, TheGameLogic->destroyObject

### JetSlowDeathBehavior::beginSlowDeath
- Purpose: Starts the slow death animation sequence for airborne jets
- Calls: SlowDeathBehavior::beginSlowDeath, FXList::doFXObj, ObjectCreationList::create, TheAudio->addAudioEvent

### JetSlowDeathBehavior::update
- Purpose: Handles frame-by-frame death animation updates and effect timing
- Calls: SlowDeathBehavior::update, FXList::doFXObj, ObjectCreationList::create, TheAudio->removeAudioEvent, TheGameLogic->destroyObject

## Globals
- None

## Dependencies
- PreRTS.h, Common/GlobalData.h, Common/ThingTemplate.h, Common/Xfer.h
- GameClient/FXList.h, GameClient/InGameUI.h
- GameLogic/GameLogic.h, GameLogic/Locomotor.h
- GameLogic/Module/AIUpdate.h, GameLogic/Module/JetSlowDeathBehavior.h
- GameLogic/Module/PhysicsUpdate.h, GameLogic/Object.h
- GameLogic/ObjectCreationList.h
