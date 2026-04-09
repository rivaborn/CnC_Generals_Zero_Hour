# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/BoneFXUpdate.cpp

## Purpose
Handles bone-based visual effects (FX, OCL, particle systems) for objects based on damage states.

## Responsibilities
- Parses and applies bone-attached effects from INI data
- Manages timing and activation of effects per damage state
- Resolves bone positions for effect placement
- Handles particle system lifecycle (creation/destruction)
- Serializes effect state for networking

## Key Types
- **BoneFXUpdateModuleData (Class)**: Stores effect configurations per damage state
- **BoneFXUpdate (Class)**: Update module managing bone effects
- **BoneLocInfo (Struct)**: Bone name and location info
- **BoneFXListInfo (Struct)**: FX list with timing and placement
- **BoneOCLInfo (Struct)**: OCL with timing and placement
- **BoneParticleSystemInfo (Struct)**: Particle system with timing

## Key Functions
### parseFXLocInfo
- Purpose: Parses bone location info from INI
- Calls: ini->getNextToken

### parseGameClientRandomDelay
- Purpose: Parses client-side random delay values
- Calls: INI::parseDurationReal

### parseGameLogicRandomDelay
- Purpose: Parses logic-side random delay values
- Calls: INI::parseDurationReal

### inList
- Purpose: Checks if value exists in index list
- Calls: None

### buildNonDupRandomIndexList
- Purpose: Generates unique random indices
- Calls: GameLogicRandomValue, inList

### update
- Purpose: Main update loop for bone effects
- Calls: initTimes, doFXListAtBone, doOCLAtBone, doParticleSystemAtBone, computeNextLogicFXTime, computeNextClientFXTime

### resolveBoneLocations
- Purpose: Resolves bone positions for current damage state
- Calls: drawable->getPristineBonePositions

### xfer
- Purpose: Serializes/deserializes effect state
- Calls: UpdateModule::xfer, Xfer methods

## Globals
- **MAX_IDX (Int)**: Maximum index count (32)

## Dependencies
- Common/GameState.h, Common/Thing.h, Common/ThingTemplate.h
- Common/INI.h, Common/RandomValue.h, Common/Xfer.h
- GameClient/FXList.h, GameLogic/GameLogic.h
- GameLogic/Module/AIUpdate.h, GameLogic/Object.h
- GameLogic/Module/BoneFXUpdate.h, GameLogic/Module/BoneFXDamage.h
