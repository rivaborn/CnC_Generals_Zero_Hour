# Generals/Code/GameEngine/Source/GameLogic/Object/Update/BoneFXUpdate.cpp

## Purpose
Handles bone-based effects (FX, OCL, Particle Systems) for game objects in Command & Conquer Generals.

## Responsibilities
- Parses configuration data for bone-based effects.
- Manages timing and execution of FX, OCL, and particle systems based on object damage states.
- Resolves bone positions relative to the object's world position.
- Handles cleanup and stopping of running particle systems.

## Key Types
- **BoneFXUpdateModuleData (Class)**: Stores configuration data for bone-based effects.
- **BoneFXUpdate (Class)**: Manages the execution of bone-based effects on game objects.
- **None**: No other significant types defined in this file.

## Key Functions
### parseFXLocInfo
- Purpose: Parses location information for a named bone.
- Calls: `ini->getNextToken`, `stricmp`

### parseGameClientRandomDelay
- Purpose: Parses random delay settings for game client effects.
- Calls: `INI::parseDurationReal`

### parseGameLogicRandomDelay
- Purpose: Parses random delay settings for game logic effects.
- Calls: `INI::parseDurationReal`

### update
- Purpose: Updates and executes bone-based effects based on current frame and damage state.
- Calls: `doFXListAtBone`, `doOCLAtBone`, `doParticleSystemAtBone`, `computeNextLogicFXTime`, `computeNextClientFXTime`

### initTimes
- Purpose: Initializes timing for bone-based effects.
- Calls: `TheGameLogic->getFrame`, `REAL_TO_INT`

### inList
- Purpose: Checks if a value is in a list of indices.
- Calls: None

### buildNonDupRandomIndexList
- Purpose: Builds a non-duplicate random index list within a specified range.
- Calls: `GameLogicRandomValue`, `inList`

### changeBodyDamageState
- Purpose: Changes the body damage state and reinitializes effect timings.
- Calls: `killRunningParticleSystems`, `initTimes`

### doFXListAtBone
- Purpose: Executes an FX list at a specified bone position.
- Calls: `resolveBoneLocations`, `getObject()->getBodyModule()->getLastDamageInfo`, `convertBonePosToWorldPos`, `FXList::doFXPos`

### doOCLAtBone
- Purpose: Executes an Object Creation List (OCL) at a specified bone position.
- Calls: `resolveBoneLocations`, `getObject()->getBodyModule()->getLastDamageInfo`, `convertBonePosToWorldPos`, `ObjectCreationList::create`

### doParticleSystemAtBone
- Purpose: Executes a particle system at a specified bone position.
- Calls: `resolveBoneLocations`, `getObject()->getBodyModule()->getLastDamageInfo`, `TheParticleSystemManager->createParticleSystem`, `setPosition`, `attachToObject`, `stop`

### computeNextClientFXTime
- Purpose: Computes the next frame for client-based effects.
- Calls: `REAL_TO_INT`

### computeNextLogicFXTime
- Purpose: Computes the next frame for logic-based effects.
- Calls: `REAL_TO_INT`

### killRunningParticleSystems
- Purpose: Stops and destroys all running particle systems.
- Calls: `TheParticleSystemManager->findParticleSystem`, `destroy`

### resolveBoneLocations
- Purpose: Resolves bone positions relative to the object's world position.
- Calls: `getObject()->getDrawable()->getPristineBonePositions`

## Globals
- **MAX_IDX (Int)**: Maximum index value, set to 32.

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/GameState.h"
  - "Common/Thing.h"
  - "Common/ThingTemplate.h"
  - "Common/INI.h"
  - "Common/RandomValue.h"
  - "Common
