# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/TransportAIUpdate.cpp

## Purpose
Handles AI logic for transport units, including passenger attack delegation and evacuation behavior.

## Responsibilities
- Manages AI state machine for transport units
- Delegates attack commands to passengers when appropriate
- Handles evacuation logic and exit permissions
- Serializes/deserializes transport-specific AI data

## Key Types
- **TransportAIUpdate (Class)**: AI update module for transport units
- **AIStateMachine (Class)**: State machine for transport AI behavior

## Key Functions
### `makeStateMachine`
- Purpose: Creates and returns the AI state machine for the transport object
- Calls: `newInstance`, `getObject`

### `privateAttackObject`
- Purpose: Attacks a target object, optionally delegating to passengers
- Calls: `getContain`, `isPassengerAllowedToFire`, `getContainedItemsList`, `getAIUpdateInterface`, `aiAttackObject`, `privateAttackObject`

### `privateForceAttackObject`
- Purpose: Forces an attack on a target object, optionally delegating to passengers
- Calls: `getContain`, `isPassengerAllowedToFire`, `getContainedItemsList`, `getAIUpdateInterface`, `aiForceAttackObject`, `privateForceAttackObject`

### `privateAttackPosition`
- Purpose: Attacks a position, optionally delegating to passengers
- Calls: `getContain`, `isPassengerAllowedToFire`, `getContainedItemsList`, `getAIUpdateInterface`, `aiAttackPosition`, `privateAttackPosition`

### `getAiFreeToExit`
- Purpose: Determines if an object is free to exit the transport
- Calls: None

### `crc`
- Purpose: Serializes/deserializes transport AI data for checksum
- Calls: `AIUpdateInterface::crc`

### `xfer`
- Purpose: Serializes/deserializes transport AI data
- Calls: `AIUpdateInterface::xfer`

### `loadPostProcess`
- Purpose: Post-processing after loading transport AI data
- Calls: `AIUpdateInterface::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/RandomValue.h`, `GameLogic/Module/TransportAIUpdate.h`, `GameLogic/Module/BehaviorModule.h`, `GameLogic/Module/ContainModule.h`, `GameLogic/Object.h`
