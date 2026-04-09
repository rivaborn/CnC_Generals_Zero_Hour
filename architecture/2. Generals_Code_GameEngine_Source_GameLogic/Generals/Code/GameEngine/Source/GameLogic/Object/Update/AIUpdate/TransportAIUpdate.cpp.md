# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/TransportAIUpdate.cpp

## Purpose
This file contains the implementation of the `TransportAIUpdate` class, which handles AI logic for transport objects in Command & Conquer Generals. It manages attacks and interactions with contained passengers.

## Responsibilities
- Manages AI state machine creation.
- Handles attack commands for transport objects, including those for passengers.
- Ensures passengers can fire if allowed by the transport's configuration.
- Implements CRC and Xfer methods for data serialization.

## Key Types
- `TransportAIUpdate` (Class): Manages AI updates for transport objects.
- None

## Key Functions
### makeStateMachine
- Purpose: Creates an AI state machine for the transport object.
- Calls: `newInstance(AIStateMachine)`

### privateAttackObject
- Purpose: Handles attack commands on a specific object, including passenger attacks.
- Calls: `getContain`, `isPassengerAllowedToFire`, `aiAttackObject`

### privateForceAttackObject
- Purpose: Forces an attack on a specific object by the transport and its passengers.
- Calls: `getContain`, `isPassengerAllowedToFire`, `aiForceAttackObject`

### privateAttackPosition
- Purpose: Handles attack commands at a specific position, including passenger attacks.
- Calls: `getContain`, `isPassengerAllowedToFire`, `aiAttackPosition`

### getAiFreeToExit
- Purpose: Determines if an object can exit the transport freely.
- Calls: None

### crc
- Purpose: Implements CRC method for data integrity checks.
- Calls: `AIUpdateInterface::crc`

### xfer
- Purpose: Handles data serialization and deserialization.
- Calls: `xferVersion`, `AIUpdateInterface::xfer`

### loadPostProcess
- Purpose: Performs post-processing after loading data.
- Calls: `AIUpdateInterface::loadPostProcess`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/RandomValue.h"
  - "GameLogic/Module/TransportAIUpdate.h"
  - "GameLogic/Module/BehaviorModule.h"
  - "GameLogic/Module/ContainModule.h"
  - "GameLogic/Object.h"

- External symbols used:
  - `newInstance(AIStateMachine)`
  - `CMD_FROM_PLAYER`
  - `CMD_FROM_SCRIPT`
  - `KINDOF_PORTABLE_STRUCTURE`
  - `DISABLED_HACKED`
  - `DISABLED_EMP`
  - `DISABLED_PARALYZED`
  - `FREE_TO_EXIT`
