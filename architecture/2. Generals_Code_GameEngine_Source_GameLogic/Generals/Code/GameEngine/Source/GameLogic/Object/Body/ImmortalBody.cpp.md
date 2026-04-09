# Generals/Code/GameEngine/Source/GameLogic/Object/Body/ImmortalBody.cpp

## Purpose
This file implements the `ImmortalBody` class, which is a variant of `ActiveBody` that prevents an object's health from dropping below 1.

## Responsibilities
- Inherits from `ActiveBody`.
- Ensures health never drops below 1.
- Overrides methods for changing health and handling serialization.

## Key Types
- ImmortalBody (Class): Extends ActiveBody to prevent health drop below 1.

## Key Functions
### ImmortalBody::ImmortalBody
- Purpose: Constructor initializes the `ImmortalBody` object.
- Calls: ActiveBody constructor

### ImmortalBody::~ImmortalBody
- Purpose: Destructor for `ImmortalBody`.
- Calls: None

### ImmortalBody::internalChangeHealth
- Purpose: Adjusts health but ensures it doesn't drop below 1.
- Calls: max, getHealth, ActiveBody::internalChangeHealth, DEBUG_ASSERTCRASH

### ImmortalBody::crc
- Purpose: Handles CRC calculation for the object.
- Calls: ActiveBody::crc

### ImmortalBody::xfer
- Purpose: Handles serialization of the object.
- Calls: xfer->xferVersion, ActiveBody::xfer

### ImmortalBody::loadPostProcess
- Purpose: Post-processing after loading the object.
- Calls: ActiveBody::loadPostProcess

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Xfer.h"
  - "GameLogic/Object.h"
  - "GameLogic/Damage.h"
  - "GameLogic/Module/ImmortalBody.h"
