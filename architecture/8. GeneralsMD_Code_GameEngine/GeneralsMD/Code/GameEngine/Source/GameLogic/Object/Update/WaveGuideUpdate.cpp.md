# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/WaveGuideUpdate.cpp

## Purpose
Handles the behavior of water wave objects in the game, including movement, visual effects, and damage to terrain/objects.

## Responsibilities
- Manages wave movement along waypoint paths
- Controls wave shape and particle effects
- Applies water damage to objects and terrain
- Handles bridge destruction and replacement with flooded versions
- Plays audio effects for waves and splashes

## Key Types
- **WaveGuideUpdateModuleData (Class)**: Stores configuration data for wave behavior (spacing, velocity, damage, etc.)
- **WaveGuideUpdate (Class)**: Maintains wave state and handles updates
- **None**: No enums/structs defined

## Key Functions
### `startMoving`
- Purpose: Initiates wave movement along a waypoint path
- Calls: `TheTerrainLogic->getWaypointByName`, `waveGuide->setOrientation`, `ai->aiFollowWaypointPath`

### `initWaveGuide`
- Purpose: Initializes wave effects and movement
- Calls: `startMoving`, `computeWaveShapePoints`, `TheParticleSystemManager->createParticleSystem`

### `doDamage`
- Purpose: Applies water damage to objects in the wave's path
- Calls: `ThePartitionManager->iterateObjectsInRange`, `obj->attemptDamage`, `TheTerrainLogic->deleteBridge`

### `update`
- Purpose: Main update loop for wave behavior
- Calls: `initWaveGuide`, `transformWaveShape`, `doShapeEffects`, `doWaterMotion`, `doShoreEffects`, `doDamage`

## Globals
- **None**: No global/static variables

## Dependencies
- Key includes: `Common/Radar.h`, `GameLogic/TerrainLogic.h`, `GameLogic/Module/WaveGuideUpdate.h`
- External symbols: `TheParticleSystemManager`, `TheTerrainLogic`, `TheGameLogic`, `TheAudio`, `TheRadar`
