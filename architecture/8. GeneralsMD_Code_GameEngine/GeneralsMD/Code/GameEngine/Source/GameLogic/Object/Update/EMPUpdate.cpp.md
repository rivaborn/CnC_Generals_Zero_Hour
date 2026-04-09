# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/EMPUpdate.cpp

## Purpose
Handles EMP (electromagnetic pulse) effects and leaflet drop behavior in the game, including visual effects, target disabling, and particle systems.

## Responsibilities
- Manages EMP pulse growth, fading, and target disabling
- Handles leaflet drop effects and enemy disabling
- Controls visual effects (tinting, flashing, particle systems)
- Processes object interactions within a radius
- Manages object lifecycle and cleanup

## Key Types
- **EMPUpdate (Class)**: Manages EMP pulse behavior and effects
- **LeafletDropBehavior (Class)**: Handles leaflet drop effects and enemy disabling
- **EMPUpdateModuleData (Struct)**: Configuration data for EMP effects (Not inferable)
- **LeafletDropBehaviorModuleData (Struct)**: Configuration data for leaflet drops (Not inferable)

## Key Functions
### saturateRGB
- Purpose: Adjusts RGB color values with saturation and offset
- Calls: None

### EMPUpdate::update
- Purpose: Updates EMP pulse state and applies effects to targets
- Calls: getObject, getEMPUpdateModuleData, TheGameLogic->getFrame, dr->setInstanceScale, dr->colorTint, dr->colorFlash, doDisableAttack, obj->kill

### EMPUpdate::doDisableAttack
- Purpose: Disables targets within EMP radius and applies visual effects
- Calls: getObject, getEMPUpdateModuleData, TheGameLogic->getFrame, ThePartitionManager->iterateObjectsInRange, curVictim->isKindOf, curVictim->kill, drw->setTintStatus, TheParticleSystemManager->createParticleSystem, sys->attachToObject, sys->setPosition, sys->setSystemLifetime, sys->setInitialDelay

### LeafletDropBehavior::update
- Purpose: Updates leaflet drop behavior and applies effects
- Calls: getLeafletDropBehaviorModuleData, TheParticleSystemManager->createParticleSystem, sys->attachToObject, TheGameLogic->getFrame, doDisableAttack

### LeafletDropBehavior::doDisableAttack
- Purpose: Disables enemy infantry and vehicles within leaflet drop radius
- Calls: getObject, getLeafletDropBehaviorModuleData, TheGameLogic->getFrame, ThePartitionManager->iterateObjectsInRange, curVictim->isKindOf, curVictim->getRelationship, curVictim->setDisabledUntil

## Globals
- **EMPUpdate::s_lastInstanceSpunPositive (Bool)**: Tracks spin direction for EMP pulses (Not inferable)

## Dependencies
- Common/Thing.h, Common/ThingTemplate.h, Common/INI.h, Common/RandomValue.h, Common/Player.h
- GameLogic/GameLogic.h, GameLogic/Module/EMPUpdate.h, GameLogic/ObjectIter.h, GameLogic/PartitionManager.h
- GameLogic/Module/AIUpdate.h, GameLogic/Module/ContainModule.h, GameLogic/Module/PhysicsUpdate.h
- GameLogic/Object.h, GameClient/Drawable.h, Common/KindOf.h, GameClient/ParticleSys.h
