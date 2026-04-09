# Generals/Code/GameEngine/Source/GameLogic/Object/Update/WaveGuideUpdate.cpp

## Purpose
This file contains the implementation for the `WaveGuideUpdate` class, which handles the update logic for wave guide objects in the game. These objects simulate water waves that move along a waypoint path, causing damage and visual effects.

## Responsibilities
- Manage the movement of wave guides along waypoints.
- Create and manage particle systems for wave effects.
- Apply damage to objects within the wave's path.
- Update visual effects like shape points and shore effects.
- Handle initialization, cleanup, and serialization of wave guide data.

## Key Types
- **WaveGuideUpdateModuleData (struct)**: Stores configuration data for wave guides, such as delay, size, spacing, and damage parameters.
- **WaveGuideUpdate (class)**: Manages the update logic for wave guide objects, including movement, effects, and interactions with other game objects.

## Key Functions
### startMoving
- Purpose: Starts the wave guide moving along its waypoint path.
- Calls: `TheAudio->addAudioEvent`, `TheTerrainLogic->getWaypointByName`, `waveGuide->setOrientation`, `waveGuide->setPosition`, `ai->aiFollowWaypointPath`.

### initWaveGuide
- Purpose: Initializes the wave guide, computes shape points, and creates particle systems.
- Calls: `startMoving`, `computeWaveShapePoints`, `TheParticleSystemManager->createParticleSystem`.

### computeWaveShapePoints
- Purpose: Computes an array of points representing the wavefront in local object space.
- Calls: None.

### transformWaveShape
- Purpose: Transforms wave shape points to world coordinates based on the current position and orientation of the wave guide.
- Calls: `waveGuide->transformPoint`, `TheTerrainLogic->getGroundHeight`.

### doShapeEffects
- Purpose: Updates particle systems that make up the front shape of the wave, ensuring they maintain a position just above the ground.
- Calls: `TheParticleSystemManager->findParticleSystem`, `particleSys->setPosition`.

### doDamage
- Purpose: Applies damage to objects within the wave's path, including visual effects and toppling logic.
- Calls: `ThePartitionManager->iterateObjectsInRange`, `obj->attemptDamage`, `obj->topple`.

### update
- Purpose: Main update function for the wave guide, handling movement, effects, and interactions.
- Calls: `initWaveGuide`, `transformWaveShape`, `doShapeEffects`, `doWaterMotion`, `doShoreEffects`, `doDamage`.

## Globals
- None

## Dependencies
- **Includes**:
  - "Common/Radar.h"
  - "Common/ThingFactory.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameClient/ParticleSys.h"
  - "GameClient/TerrainVisual.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/TerrainLogic.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Module/PhysicsUpdate.h"
  - "GameLogic/Module/WaveGuideUpdate.h"
  - "GameLogic/Module/ToppleUpdate.h"
