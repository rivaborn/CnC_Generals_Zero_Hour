# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Body/ImmortalBody.cpp

## Purpose
Implements an immortal body module that prevents health from dropping below 1, ensuring the object never dies.

## Responsibilities
- Overrides health modification to enforce minimum health of 1
- Extends ActiveBody functionality while preventing death
- Handles serialization (Xfer) and CRC for network synchronization
- Performs post-load initialization

## Key Types
- ImmortalBody (Class): Module that enforces non-lethal damage on objects

## Key Functions
### ImmortalBody::ImmortalBody
- Purpose: Constructs an ImmortalBody instance.
- Calls: ActiveBody constructor

### ImmortalBody::internalChangeHealth
- Purpose: Modifies health while ensuring it never drops below 1.
- Calls: ActiveBody::internalChangeHealth, max()

### ImmortalBody::crc
- Purpose: Generates/verifies CRC checksum for network synchronization.
- Calls: ActiveBody::crc

### ImmortalBody::xfer
- Purpose: Serializes/deserializes the object for network transfer.
- Calls: ActiveBody::xfer, Xfer::xferVersion

### ImmortalBody::loadPostProcess
- Purpose: Performs post-load initialization.
- Calls: ActiveBody::loadPostProcess

## Globals
None

## Dependencies
- PreRTS.h, Common/Xfer.h, GameLogic/Object.h, GameLogic/Damage.h, GameLogic/Module/ImmortalBody.h
- ActiveBody class, Xfer class, Thing class, ModuleData struct
