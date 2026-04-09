# Generals/Code/GameEngine/Source/GameLogic/Object/Body/ActiveBody.cpp

## Purpose
This file contains the implementation of the `ActiveBody` class, which manages health, damage states, and particle systems for game objects in Command & Conquer Generals.

## Responsibilities
- Manage health and damage states of game objects.
- Handle damage effects and visual transitions based on health changes.
- Maintain particle systems associated with object damage states.
- Implement serialization and deserialization logic for the `ActiveBody` class.

## Key Types
- **BodyParticleSystem (Class)**: Represents a particle system attached to an object's body, managed during damage state transitions.
- **BodyDamageType (Enum)**: Enumerates different damage states of an object (e.g., pristine, damaged, really damaged, rubble).
- **None**: No other significant types defined in this file.

## Key Functions
### calcDamageState
- **Purpose**: Calculate the current damage state of an object based on its health.
- **Calls**: None

### ActiveBody::ActiveBody
- **Purpose**: Constructor for `ActiveBody`, initializes health and sets up initial damage states.
- **Calls**: validateArmorAndDamageFX, setCorrectDamageState

### ActiveBody::~ActiveBody
- **Purpose**: Destructor for `ActiveBody`.
- **Calls**: None

### ActiveBody::onDelete
- **Purpose**: Clean up resources when the object is deleted.
- **Calls**: deleteAllParticleSystems

### ActiveBody::setCorrectDamageState
- **Purpose**: Update the damage state of the object and handle visual changes.
- **Calls**: calcDamageState, getObject->setGeometryInfoZ, TheAI->pathfinder()->removeObjectFromPathfindMap, TheAI->pathfinder()->addObjectToPathfindMap

### ActiveBody::internalChangeHealth
- **Purpose**: Change the health of the object without triggering additional game logic.
- **Calls**: None

## Globals
- **None**: No global or static variables defined in this file.

## Dependencies
- Key includes:
  - "Common/BitFlagsIO.h"
  - "Common/CRCDebug.h"
  - "Common/DamageFX.h"
  - "Common/Player.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/Armor.h"
  - "GameLogic/Object.h"
  - "GameLogic/TerrainLogic.h"
  - "GameLogic/Module/ActiveBody.h"
- External symbols used:
  - TheGlobalData
  - TheArmorStore
  - TheGameLogic
  - ThePlayerList
  - TheAudio
  - TheInGameUI
  - TheControlBar
