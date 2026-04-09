# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Helper/SubdualDamageHelper.cpp

## Purpose
Manages subdual damage healing for game objects, handling periodic damage reduction and status updates.

## Responsibilities
- Tracks and reduces subdual damage over time
- Handles healing rate and countdown logic
- Notifies when subdual damage is applied
- Serializes/deserializes helper state

## Key Types
- SubdualDamageHelper (Class): Helper for managing subdual damage healing
- DamageInfo (Struct): Damage information for healing calculations

## Key Functions
### update
- Purpose: Handles periodic subdual damage healing
- Calls: getObject, getBodyModule, getSubdualDamageHealRate, attemptDamage, hasAnySubdualDamage

### notifySubdualDamage
- Purpose: Resets healing timer when new subdual damage is applied
- Calls: getObject, getBodyModule, getSubdualDamageHealRate

### crc
- Purpose: Generates CRC checksum for network synchronization
- Calls: ObjectHelper::crc

### xfer
- Purpose: Serializes/deserializes helper state
- Calls: ObjectHelper::xfer

## Globals
- None

## Dependencies
- PreRTS.h, Common/Xfer.h
- GameLogic/Object.h, GameLogic/Module/BodyModule.h, GameLogic/Module/SubdualDamageHelper.h
- ObjectHelper, BodyModuleInterface, DamageInfo, UpdateSleepTime
